# 12 · Open Questions

**Status:** [↻ living record] · v1.2.0 · 12 July 2026

Everything here is **Unknown / Insufficient data** as of this version. Nothing in the study's analysis is permitted to rest on an assumed answer to any item below. Items resolve only against vendor documentation, direct vendor response or authoritative reporting; resolution is logged in the changelog and the resolving source is added to `13-sources.md`. Where a resolution reaches the study through a person rather than a public source, it is attributed only with that person's consent.

This register holds **product-specific factual unknowns** (Q-series): questions with a true answer that this study does not yet possess. It is distinct from `14-enterprise-question-set.md` (E-series), which holds **enterprise decision questions**: questions with no single true answer, only resolutions each organization must choose. A deployer needs both registers answered, in different senses of "answered," before deployment.

| ID | Question | Why it matters | Resolves against |
|---|---|---|---|
| Q1 | What happens to channel memory when the agent is removed from a channel, and when the integration is terminated? Deleted, retained, retained-with-TTL? | C6 (rehearsed Exit) is blocking without this; discovery and GDPR analysis in `07`/`08` both hinge on it | Vendor documentation or DPA terms |
| Q2 | What is the retention period and export capability for the centralized audit console? | C10; regulated-records deployers cannot rely on logs they cannot produce | Vendor documentation |
| Q3 | Do externally shared (Slack Connect) channels interact with channel memory or cross-channel learning in any way, even when the agent is not a member of the shared channel? | Determines whether C3's Slack Connect exclusion is sufficient or merely necessary | Vendor documentation or security research |
| Q4 | Is ambient mode off by default at the organization level, and is the toggle per-channel or global? | C2's cost depends on granularity; a global-only toggle forces all-or-nothing | Vendor documentation |
| Q5 | Can channel memory be enumerated, inspected or selectively corrected by an admin? | Rows 2 of the ledger; GDPR rectification and erasure; P2 | Vendor documentation |
| Q6 | Is the agent's memory susceptible to durable instruction-planting (an injected instruction persisting across sessions)? | Escalates `06.C` from established attack class to demonstrated vulnerability | Security research |
| Q7 | Does a legal-hold mechanism exist for channel memory (suspension of expiry or modification for identified channels)? | `08.B`; Rule 37(e) exposure | Vendor documentation or counsel inquiry |
| Q8 | Do Slack archiving and eDiscovery connectors capture agent-initiated (ambient) messages identically to human messages? | `08.C`; supervision and record-keeping regimes | Deployment-specific verification |
| Q9 | Current status of Korean attorney-client privilege legislation | `08.A` Korea analysis carries a verification flag | National Assembly record; Korean counsel |
| Q10 | Whether and how the agent distinguishes instruction authority among channel members (any role-awareness at all) | `04.D` assumes recency-only resolution; if role-awareness exists, that section weakens and is revised | Vendor documentation or testing |

Final Liability rests with the Human.
