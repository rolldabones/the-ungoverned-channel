# 01 · Abstract and Method

**Status:** [✓ final] · v1.0.1 · 17 August 2026 (KST)

> **Correction, 17 August 2026 (KST).** This file carried the claim that the legacy Claude in Slack app was force-migrated on 3 August 2026. **That claim is struck.** It was struck in v1.4.0 on 13 August 2026 against the vendor's own migration documentation, and the correction reached `02-timeline.md` and `05-feature-control-ledger.md` but not this file. Claude Tag replaces the earlier app *in place*: the same Slack app and `@Claude` handle remain, no data migrates, pairing the workspace defaults every scope to New, and Legacy is deprecated on an **account-specific** cutover date after which Legacy scopes stop responding. There was no blanket automatic conversion on 3 August 2026.

## Abstract

Between October 2025 and June 2026, Anthropic moved Claude from a per-user assistant inside Slack to a persistent multiplayer agent (Claude Tag) that holds one identity per channel, remembers what it reads, learns across channels where permitted, reaches connected enterprise systems and, in its ambient mode, acts without being asked. The legacy app was reported as force-migrated on 3 August 2026; that framing is struck and the actual mechanism is set out in the correction above. This study examines the deployment as a governance object: not whether the model is safe, but whether an organization deploying it can satisfy the accountability, oversight, auditability and data governance expectations of prevailing frameworks (NIST AI RMF, ISO/IEC 42001, EU AI Act deployer duties as amended by the Digital Omnibus, Korea's AI Framework Act). The finding is that the product is governable only conditionally, through compensating controls the vendor does not require and that negate much of the product's marketed value. The interesting object is the gap between those two states, which this study names the governance discount: the portion of an agentic product's value proposition that a governed deployer must decline.

## Scope

In scope: the deployment layer (identity, access, memory, audit, oversight, exit) and the multiplayer dynamics specific to shared channels. Out of scope: model-level alignment and safety, which sit below the deployment layer; and vendor-side provider obligations under the EU AI Act, which belong to Anthropic, not the deployer this study addresses.

## Method

1. **Authority hierarchy.** Statute and adopted regulation > official guidance and institutional press releases > vendor documentation > peer-reviewed and reproducible security research > credible trade press > vendor marketing > inference. Claims are tiered in `13-sources.md`. Vendor self-reports (for example the claim that 65 percent of Anthropic's product team code is created through its internal Claude Tag) are recorded as context and given no evidentiary weight.
2. **Unknowns held as unknowns.** Where a fact cannot be verified (memory disposition on agent removal, audit log retention, Slack Connect interaction with cross-channel learning) it is logged in `12-open-questions.md` as Unknown / Insufficient data. Nothing is filled by inference.
3. **Falsifiability.** The study registers predictions with confidence levels and review dates (`11-predictions-register.md`). A case study that cannot be wrong is marketing.
4. **Version discipline.** Every change is logged. Superseded claims are marked, not deleted.

## Critique of the v1 memo (superseded)

This study replaces a memorandum dated 11 July 2026, superseded in full and not reproduced here. The memo was directionally sound. Its defects, which this study corrects, were the following.

1. **Attribution collapse was overstated by one level.** The memo said the audit log "records who tagged the agent, not whose accumulated context shaped what it did," implying attribution does not exist. In fact request-level attribution exists: the audit console identifies the initiating user per request. What does not exist is output-level accountability: a mapping from a finished work product to the set of human contributions (instructions, corrections, connected data, channel memory) that produced it. The corrected claim is narrower and stronger, and it is developed in `04-the-multiplayer-problem.md`.
2. **The regulatory framing was stale.** The memo invoked EU AI Act high-risk deployer duties without accounting for the Digital Omnibus, which received final Council approval on 29 June 2026 and defers Annex III high-risk obligations to 2 December 2027. The live 2 August 2026 obligations are the Article 50 transparency duties, which the memo did not mention. `07-regulatory-mapping.md` is rebuilt on the post-Omnibus timeline, and reframes the high-risk question as one of classification drift rather than present breach.
3. **The privilege point was jurisdictionally naive.** One paragraph treated privilege as a single doctrine. In fact the analysis diverges sharply across the US, the EU (where Akzo Nobel denies legal professional privilege to in-house counsel in Commission competition proceedings) and Korea (where no general attorney-client privilege shields communications in the US sense at all). `08-privilege-discovery-legal-process.md` does this properly.
4. **"A channel is not a legal person" was rhetoric doing the work of analysis.** Enterprise liability does not vanish when attribution fails; it pools at the employer through vicarious liability and organizational fault. The real casualty is internal: the disciplinary, quality and defensibility mechanisms that depend on knowing who did what. The corrected analysis distinguishes external liability (which survives) from internal accountability (which collapses).
5. **The social dynamics of multiplayer use were missing.** Responsibility diffusion, authority ambiguity among competing principals and the laundering of contested positions through "Claude said" are at least as corrosive as the technical failures, and the memo did not treat them. They are now the center of `04-the-multiplayer-problem.md`.
6. **No comparison class.** The memo asserted novelty without earning it. Enterprises have governed shared service accounts, RPA bots and workflow automations for decades. `04` and `10` now identify precisely which properties are genuinely new (persistent memory, unprompted initiative, natural language as attack surface, non-determinism, cross-context synthesis) and which are old problems wearing new clothes.
7. **Static form, moving target.** A memo freezes; this subject does not. Hence the living format, the update protocol and the predictions register.

Final Liability rests with the Human.
