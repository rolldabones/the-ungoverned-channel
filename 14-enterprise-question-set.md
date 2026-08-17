# 14 · The Enterprise Question Set: Pre-Deployment Questions for Agentic AI, with Possible Resolutions

**Status:** [↻ living record, work in progress by design] · v1.0.1 · 17 August 2026 (KST)

## How to use this file

This file generalizes the case study. The questions below are deliberately **jurisdiction agnostic and product agnostic**: they apply to any persistent, multi-user, tool-connected AI agent deployed into a shared workspace, whatever the vendor and wherever the enterprise operates. Claude Tag is the occasion for the list, not its limit. Where a question touches law, it is framed against "the regimes applicable to you" rather than any named statute; map it to your jurisdictions with counsel.

Each entry gives the question, why it matters in one or two sentences, and possible resolutions. Resolutions are **options with tradeoffs, not recommendations**; the right choice depends on the organization's risk appetite, sector and use case. Where several options are listed, they are ordered roughly from most restrictive to most permissive. A question answered "we have not decided" is a finding; a question that cannot be answered even in principle with the product as shipped is a blocking finding or a documented risk acceptance at the level of authority that owns the consequence.

This is a living list. Questions will be added, refined and marked superseded as the field's experience accumulates. Contributions of questions from deployment experience are the most valuable kind.

Numbering: E-series (enterprise decision questions), distinct from the Q-series in `12-open-questions.md` (product-specific factual unknowns).

---

## A. Accountability and ownership

**E1. Who is the named accountable human for each agent instance and for its outputs?**
*Why:* Shared agents dissolve output-level accountability by default (`04.A`); liability then pools at the entity while the internal machinery of quality and discipline collapses (`04.B`).
*Possible resolutions:*
1. **Instance owner model.** One named human per channel, space or workflow owns every agent output there, regardless of who invoked it. Cheap, restores accountability by policy; nominal unless paired with real verification capacity (E15).
2. **Output sign-off model.** Consequential output classes (external communications, decision memos, code merged to protected branches) require a named human to adopt the output as their own before it takes effect. Stronger, slower; requires defining "consequential."
3. **Hybrid.** Instance owner for ambient accountability plus sign-off gates for defined output classes. The usual right answer for mixed-use spaces.
A useful framing test for any resolution: in a responsibility matrix, the agent may hold responsibility for execution but never accountability; if a workflow chart shows the agent as the accountable party, the workflow is misdesigned.

**E2. What happens to accountability when the owner leaves, moves or is absent?**
*Why:* Ownership assigned once and never maintained is ownership in a spreadsheet, not in fact.
*Possible resolutions:* (1) Fold agent ownership into the joiner-mover-leaver process, with transfer as a required offboarding step. (2) Automatic suspension: an agent whose owner record is vacant is removed from its spaces until ownership is reassigned. (3) Deputy ownership for planned absence. Option 2 is the only one that fails safe.

**E3. When two users give the agent conflicting instructions, whose governs?**
*Why:* Products typically resolve by recency, which is not an authority model; any member can silently redirect work another member believes is proceeding under their instruction (`04.D`).
*Possible resolutions:* (1) Policy: mid-task redirection of another person's delegated work requires the original requester's confirmation, enforced socially and by owner review. (2) Configuration, where the product allows: instruct the agent to confirm redirects with the original requester before proceeding. (3) Structural: one-delegator-per-task norm; others contribute through the delegator. (4) Accept recency resolution for low-stakes spaces and prohibit the agent from high-stakes multi-principal work. Most organizations will need (1) plus (4).

## B. Authorization and initiative

**E4. What tasks is the agent authorized to perform, and how will out-of-scope use be detected?**
*Why:* A general-purpose agent in a workspace is a continuously renegotiated deployment; actual uses are decided daily by whoever is present, and drift into higher-risk uses produces no deployment event anyone reviews (`07.D`).
*Possible resolutions:* (1) A written task taxonomy per space: permitted classes, prohibited classes, escalation for the unclassified. (2) A standing classification function that periodically samples what the agent is actually asked to do and compares it against the taxonomy and against whatever high-risk categories the applicable regimes define. (3) Prohibited-use detection through log review keyed to sensitive verbs (rank candidates, assess performance, score, approve). (2) is the study's principal original recommendation (C9) and generalizes to every agentic deployment.

**E5. Is unprompted action permitted at all, and under what conditions?**
*Why:* Proactive or ambient behavior inverts authorization: the agent selects its own tasks, so pre-authorization of specified work is impossible by construction (ledger row 4).
*Possible resolutions:* (1) Off, categorically. (2) Off by default, enabled per space on a documented risk assessment signed by the space owner. (3) Notify-only proactivity: the agent may flag and suggest but never execute unprompted. (4) Full proactivity in designated low-stakes spaces only. Option 3 is underused and preserves much of the feature's value at a fraction of its risk; vendors should be pressed to support it as a distinct mode.

**E6. Which actions require human confirmation, and where does the confirmation occur?**
*Why:* An agent manipulated or mistaken mid-task will carry the error across every stage unless a gate interrupts it; a gate inside the same compromised channel can itself be spoofed or socially engineered.
*Possible resolutions:* (1) A high-impact action list (external sends, record modification, financial movement, merges to protected code, permission changes) each requiring confirmation through a surface outside the agent's workspace. (2) Two-person confirmation for irreversible actions. (3) Value and volume thresholds below which actions proceed unconfirmed, reviewed quarterly. Note the structural caveat: gates implemented as instructions to the agent are policies the model is asked to honor, not architecture; prefer gates enforced by the connected system (branch protection, payment approval workflows) over gates enforced by prompt.

## C. Identity and access

**E7. Is the agent an identity in your identity governance program?**
*Why:* Agents authenticate, hold scopes, inherit permissions and act; an actor invisible to identity governance is a privileged account no one recertifies.
*Possible resolutions:* (1) Register each agent instance as a service-account-class identity: named owner, documented scopes, quarterly recertification, inclusion in access reviews and in joiner-mover-leaver logic (an owner's departure triggers E2). (2) For fleets of agents, an agent registry with the same fields, feeding the identity program. There is no permissive option here worth listing; unregistered agents are the finding.

**E8. How are tool scopes granted, bounded and revoked?**
*Why:* Blast radius equals the union of connected scopes (`06.D`); scope is the one blast-radius variable the deployer fully controls.
*Possible resolutions:* (1) Scope-per-approved-use-case, granted at deployment, with additions requiring the same approval as the initial grant. (2) Time-boxed grants that expire and must be renewed. (3) Environment separation: the agent reaches staging or read-replicas, never production or systems of record, with human promotion of its work. (4) Quarterly diff of granted scopes against approved use cases, with unexplained entries revoked by default. Combine (1) with (4) at minimum.

**E9. Who may admit the agent to a new space, and against what screening?**
*Why:* Every admission is a deployment decision; distributed, unscreened admission means the organization's real deployment footprint is unknown to it.
*Possible resolutions:* (1) Centralized admission through the owner-and-checklist process (no counsel spaces, no externally shared spaces, no regulated-data spaces without assessment; see C3). (2) Delegated admission by space owners against the same checklist, with audit sampling. (3) Free admission with periodic sweep and removal. Option 3 is listed only to be named as the default most organizations will drift into if they do not choose otherwise.

## D. Memory and data lifecycle

**E10. What does the agent retain, where, for how long, and can you enumerate it?**
*Why:* Persistent memory is a vendor-held, potentially non-enumerable record of organizational knowledge; behavior conditioned on it cannot be reconstructed, and obligations cannot be discharged against contents that cannot be listed (ledger row 2).
*Possible resolutions:* (1) Vendor diligence before deployment: retention terms, enumeration and inspection tooling, expiry controls, disposition on removal (the Q1 and Q5 questions, generalized to any vendor). (2) Where enumeration does not exist: periodic reset by removal and re-admission, on a schedule set by space sensitivity, accepting the loss of the feature's value. (3) Data classification gates: the agent is simply never admitted where the most sensitive classes live. In practice (1) determines whether (2) and (3) are supplements or the entire program.

**E11. How will data-subject-rights style obligations (access, rectification, erasure, whatever your applicable regimes call them) be discharged against agent memory?**
*Why:* Workspace content is personal data of employees and third parties in most regimes; a memory that cannot be enumerated cannot evidence its own compliance.
*Possible resolutions:* (1) Contractual: vendor commitments to honor deletion and rectification requests against memory, with evidence. (2) Operational: reset as the blunt instrument that discharges erasure at the cost of everything else retained. (3) Preventive: exclude spaces dense in third-party personal data from agent reach. (4) An impact assessment (whatever your regime names it) before deployment at scale, treating agent memory as its own processing operation rather than an incident of the workspace.

**E12. Can memory be preserved on demand when a dispute or investigation requires it?**
*Why:* Preservation duties in most legal systems attach on reasonable anticipation of a dispute; a memory system with no hold mechanism makes routine operation (expiry, reset, removal) indistinguishable from spoliation.
*Possible resolutions:* (1) Vendor hold mechanism, contractually required and tested. (2) Snapshot-by-export where any export capability exists, on a defined trigger. (3) Where neither exists: document the gap formally, suspend resets for affected spaces on hold triggers, and keep the agent out of dispute-prone spaces (active claims, investigations, contentious counterparties). The formal documentation matters: a gap identified before the dispute is a limitation; one discovered during it is negligence.

**E13. Does the agent cross contexts your organization deliberately keeps apart?**
*Why:* Cross-context synthesis is the product's value and the organization's information barriers with the sign flipped (`04.F`); the failure produces no log entry that looks like a failure (`06.B`).
*Possible resolutions:* (1) Deny cross-context learning wherever the product makes it optional. (2) Barrier-aware admission: the agent's space memberships are reviewed against the same wall logic applied to humans. (3) Separate agent instances per barrier zone, never bridged. (4) For organizations without formal barriers: ask the question anyway, since every organization separates something (personnel matters, deal negotiations, disciplinary processes) even without calling it a wall.

## E. Oversight, verification and audit

**E14. What is logged, is it sufficient to reconstruct an incident, and who holds the logs?**
*Why:* Activity logs (who invoked, what tools fired) support monitoring but not reconstruction where memory state drifts and generation is non-deterministic (`06.E`); vendor-held logs on vendor retention schedules may be gone when needed.
*Possible resolutions:* (1) Deployer-side export and retention of all available logs under the deployer's schedule. (2) A written statement of the reconstruction gap in the risk register, accepted at the right level, so incident response plans around containment speed rather than root-cause replay. (3) Vendor engagement for richer telemetry (memory snapshots at action time would close most of the gap; no vendor is known to offer this, which is itself worth recording).

**E15. Who verifies agent outputs, and how is verification an assigned duty rather than a diffused assumption?**
*Why:* In a shared space an output is everyone's to check and therefore no one's; implied collective review is the absence of review (`04.C`).
*Possible resolutions:* (1) Verification attaches to the accountability resolution chosen in E1: the instance owner or the sign-off human verifies, by name. (2) Verification checklists per output class, so "verified" has content. (3) Sampling QA by a function outside the space, at a published rate, so verification is occasionally itself verified.

**E16. How will you detect verification decay?**
*Why:* Verification erodes predictably as trust accumulates; the erosion is invisible until the first consequential miss, and the skills needed to verify atrophy in proportion to delegation.
*Possible resolutions:* (1) Seeded-error testing: known-flawed outputs introduced periodically, with detection rates tracked. (2) Correction-rate metrics: a space whose members never correct the agent is either blessed or asleep, and the metric cannot tell which without (1). (3) Rotation of verification duty to distribute the skill and the burden. (4) Skill-retention design: deliberately reserving certain work for humans not because the agent cannot do it but because verifiers who never do the work lose the ability to check it.

## F. Security posture

**E17. Is every message, document and participant treated as untrusted input to the agent?**
*Why:* Natural language is the agent's control plane, so the attack surface is everyone and everything the agent can read, including pasted third-party documents and content synced from externally shared spaces; injection against this product class is demonstrated, not theoretical (`06.A`).
*Possible resolutions:* (1) No agent in externally shared or federated spaces, categorically. (2) Provenance rules for content the agent is asked to process (third-party documents handled in designated spaces with heightened gating). (3) High-impact action gating (E6) as the backstop that assumes some injection will succeed. (4) Standing red-team exercises against your own deployment, since the vendor's defenses are a moving and unverifiable target.

**E18. What is the measured containment time?**
*Why:* Where reconstruction is impossible (E14), incident response is containment; an exit that has never been rehearsed is a diagram (C6).
*Possible resolutions:* (1) Pre-deployment rehearsal of the full removal chain (agent out of space, scopes revoked, integration terminated) with elapsed times recorded and re-measured semiannually. (2) Defined severity triggers that authorize any of a named set of people to execute the chain without further approval. (3) Tabletop exercises that include the scenario "the agent is the incident," which most existing playbooks do not contemplate.

## G. Legal process readiness (regime agnostic)

**E19. Are legally sensitive communications excluded from the agent's reach?**
*Why:* Whatever protection your jurisdictions give legal communications (strong privilege, qualified confidentiality or none), an agent that reads, remembers and independently redeploys content weakens every version of it: where privilege exists the agent's restatement can waive it, and where it does not the memory becomes an organized, searchable compilation available to lawful process (`08.A`).
*Possible resolutions:* (1) Categorical exclusion: no agent in any space where legal advice, investigations, disciplinary processes or board deliberations occur. Cheapest control in the study and the least adopted, because these are exactly the spaces that most want summarization. (2) Counsel sign-off as a mandatory step in the admission screening (E9) for any borderline space. (3) Jurisdiction mapping with counsel as a scheduled diligence item where operations span regimes with divergent protection.

**E20. Are agent-generated communications captured by your records, retention and supervision systems identically to human ones?**
*Why:* Regulated deployers already treat workspace messages as records; an agent multiplies record volume, and a proactive agent creates records no human decided to make. Archiving tooling built for human messages may not capture agent-initiated ones identically, and the gap will surface during an examination, not before.
*Possible resolutions:* (1) Parity testing before deployment: confirm archiving, retention and supervision tooling captures agent messages, agent-initiated messages and agent-modified artifacts. (2) Disable the agent in regulated-record spaces until parity is verified. (3) Supervision sampling extended to agent output explicitly.

## H. Human factors and decision hygiene

**E21. How do you prevent agent output acquiring unearned authority in group decisions?**
*Why:* A contested position, phrased fluently by the agent and posted into the group, becomes the anchor text; members learn to launder their framing through the agent and receive it back as neutral synthesis (`04.E`).
*Possible resolutions:* (1) Author-of-record rule: any document that carries a decision has a named human author who has adopted every sentence; the agent's draft is an input, never the document. (2) Framing transparency norm: when the agent's output was produced from one member's side instruction, that instruction is disclosed to the group. (3) Deliberation hygiene: for consequential decisions, positions are gathered before the agent is asked to synthesize, not after.

**E22. Do users understand what the agent retains, connects and can be made to do?**
*Why:* Most failure modes in this study are activated by ordinary users acting in good faith: pasting a confidential document into a public space the agent reads, asking a casual question that constitutes a high-risk use, trusting a synthesis that laundered a colleague's framing. Whatever AI-literacy duties your regimes impose, the operational need exceeds them.
*Possible resolutions:* (1) Space-level onboarding: joining a space where the agent is present triggers a short, concrete notice (what it retains, who owns its outputs here, what not to paste). (2) Just-in-time friction for known hazards (a prompt before the agent processes an uploaded third-party document). (3) Literacy content built from this study's failure modes rather than generic AI training.

## I. Vendor relationship and exit

**E23. What is the rehearsed, contractual exit, and what does the vendor keep?**
*Why:* Memory and accumulated context are typically not portable; the switching cost of an agentic deployment grows daily in a way conventional SaaS does not, and an unrehearsed exit is not an exit (`05` row 8, C6).
*Possible resolutions:* (1) Contract: data disposition on termination specified, evidenced and tested; export rights over anything exportable. (2) Operational: the E18 removal chain doubles as the exit rehearsal. (3) Strategic: organizational knowledge the agent accumulates is deliberately duplicated in systems the organization owns (documentation the agent helps produce belongs in your repositories, not only in its memory), so the memory is a convenience rather than the single copy.

**E24. What happens when the vendor changes the product faster than you can assess it?**
*Why:* Deprecation cutovers, default changes and beta cadence put deployment timing on the vendor's roadmap; the organization that has not assessed by the cutover runs the new architecture by default (ledger row 8). Note the shape of the pressure as recast at v1.4.0: the Legacy deprecation date is set per account rather than published, so the deadline cannot be tracked from outside and a standing owner is the only way to see it coming.
*Possible resolutions:* (1) Contractual change notice with a defined assessment window, where negotiable. (2) A pre-committed posture, decided in advance and in writing: on any forced change not yet assessed, the deployment is suspended pending assessment rather than continued pending objection. (3) A standing owner for vendor-change monitoring, since changes announced in blog posts do not route themselves to risk functions.

## J. Value accounting

**E25. What is the governance discount, and does the business case survive it?**
*Why:* The controls above collectively decline a substantial fraction of what the product's launch materials sell (`09`); a business case built on the ungoverned configuration is a case for a product the organization cannot responsibly run.
*Possible resolutions:* (1) Run the business case exclusively on the governed configuration: features declined, controls staffed, review functions funded. (2) Present the delta between marketed and governed value to the approving authority as a named number, the governance discount, so the decision to deploy is informed about what is actually being bought. (3) Revisit annually: if vendor tooling closes ledger rows (see the predictions register), the discount shrinks and the case improves on the record.

---

## Closing note

These questions outlive this product. Shared identity, persistent memory, tool reach, initiative and natural language as a control plane are the defining properties of the coming class of workplace agents, whoever ships them. An enterprise that can answer E1 through E25 for one vendor's agent has built the assessment capability for all of them, which is a better return than any single deployment decision. The list is a work in progress and is expected to be wrong in places; the changelog will show where.

Final Liability rests with the Human.
