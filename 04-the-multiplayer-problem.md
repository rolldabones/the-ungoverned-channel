# 04 · The Multiplayer Problem

**Status:** [✓ final] · v1.0.0 · 11 July 2026

This is the center of the case study. The question is what changes, as a matter of governance, when many humans share one agent, rather than each human having one.

## A. Two levels of attribution, and which one fails

Request-level attribution exists. The audit console records which user initiated each request and which tools the agent used. If User A tags @Claude and the agent deletes the wrong branch, the log shows A asked.

Output-level accountability does not exist, and cannot be reconstructed from request-level logs. A finished work product in a multiplayer channel is a function of at least five inputs: (1) the initiating instruction, (2) mid-thread corrections and additions from other members, (3) connected data sources the agent consulted, (4) the agent's accumulated channel memory, which no one can enumerate, and (5) the model's own non-deterministic generation. The mapping from output back to responsible human contribution is therefore not merely unlogged; it is not well defined. Ask "who is accountable for this deliverable as shipped" and the honest answer is a weighted set of people plus a memory state that no longer exists.

The counterargument must be met squarely: human teams also produce composite outputs, and organizations handle this with document ownership, review gates and sign-off. True. But three things distinguish the agentic case. The human contributor whose input was decisive can be identified, questioned and deposed; the agent's decisive "contribution" (its memory state at generation time) cannot be. Human contribution is bounded by what each person actually knew; the agent's contribution draws on a context pool no participant possesses. And the human composite is assembled through checkpoints an organization designed; the agentic composite is assembled inside the model, between checkpoints. Document-ownership discipline is the right instinct, which is why `09-compensating-controls.md` rebuilds it by policy as a named owner per channel. The point is that the product does not supply it and the audit trail cannot substitute for it.

## B. External liability survives; internal accountability collapses

The v1 memo's line "a channel is not a legal person" invited a misreading. When an agent-produced output causes harm, liability does not disappear into the channel. It pools at the enterprise: vicarious liability for employees acting in the scope of employment, organizational fault for deploying the system, contractual liability to counterparties. The external allocation question mostly answers itself, and it answers "the company."

What collapses is everything internal that depends on granular attribution: quality management (whose error, corrected how), discipline and incentives (responsibility that cannot be located cannot be enforced), and litigation defensibility (an enterprise that cannot reconstruct how a harmful output was produced cannot mount a due-diligence defense, demonstrate the reasonableness of its oversight or apportion fault with its vendor). The enterprise becomes strictly liable in practice while losing the internal machinery that keeps such liability rare. **Final Liability** is not defeated by the product; it is defaulted to the entity's most senior officers, silently, without their informed consent. That silent default, not the disappearance of liability, is the doctrine's complaint.

## C. Responsibility diffusion

The social-psychological finding that responsibility diffuses with the number of bystanders maps directly onto the shared agent. In the per-user model, the person who prompted is unambiguously the person who must verify. In a channel of twelve, an agent output is everyone's to check and therefore no one's. Each member can rationally assume another member, closer to the subject matter, has verified. The product's own marketing sharpens the hazard: work "in public view" implies review by the public in the channel, and implied review is the absence of review. Verification is a cost each member individually avoids while assuming it is collectively borne. Nothing in the product assigns it.

## D. Authority ambiguity

A shared agent serves principals whose instructions conflict. User A sets a direction; User B, three hours later, modifies it; the agent proceeds on B's modification. Whose intent governs? The product resolves the question by recency, which is not an authority model: in human organizations, whether B may countermand A depends on role, seniority and mandate, none of which the agent can see. The channel flattens hierarchy that the organization's accountability structure depends on. This also creates a quiet override surface: any channel member can redirect work that another member believes is proceeding under their instruction, and the redirect looks like collaboration.

## E. Consensus laundering

In group deliberation, an agent's output acquires an authority it has not earned. A contested position, once phrased fluently by the agent and posted into the thread, becomes the anchor text; dissent must now argue against a document rather than a colleague. Members with a position to advance learn quickly that the agent is a persuasion instrument: feed it framing in a side exchange, then tag it publicly and receive the framing back as neutral synthesis. "Claude said" functions in the channel the way "the data says" functions in a bad meeting: a laundering of authorship. The multiplayer setting is what makes this potent; in a private chat there is no audience to launder for.

## F. What is genuinely new here

Enterprises have governed shared instruments before: service accounts, RPA bots, Slackbot workflows, shared mailboxes. Most of the identity-governance playbook transfers, and `09` uses it. Five properties do not transfer:

1. **Persistent, non-enumerable memory.** A service account has credentials, not a worldview.
2. **Initiative.** RPA executes defined triggers; ambient mode invents its own.
3. **Natural language as the control plane.** Every message in the channel is potentially an instruction, which makes every channel member, and every document they paste, part of the attack surface (`06`).
4. **Non-determinism.** The same instruction does not reproduce the same output, which breaks replay-based audit.
5. **Cross-context synthesis.** The agent's core value is connecting information the organization separated on purpose; its value proposition and the organization's information barriers are the same object with opposite signs.

The governance problem is the compound of old (shared identity) and new (memory, initiative, language, non-determinism, synthesis). Treating it as either alone understates it.

Final Liability rests with the Human.
