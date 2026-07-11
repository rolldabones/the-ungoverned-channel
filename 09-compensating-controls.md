# 09 · Compensating Controls: Conditions of Governability

**Status:** [✓ final] · v1.0.0 · 11 July 2026

Each control is stated with its test, because a control that cannot be tested is a wish. Together these are the conditions under which the study's verdict (`10`) concedes governability. They correspond to ledger rows in `05`.

**C1. Named owner per channel** (ledger row 1). One accountable human is designated for each channel the agent joins; that person owns every agent output in the channel regardless of who tagged it, and ownership is recorded where the organization records accountability, not in a wiki no one reads. *Test:* for any sampled agent output, the responsible human can be named within one business day. Restores **Final Liability** by policy where the product does not supply it.

**C2. Ambient mode off** (row 4) at deployment, enabled only channel by channel on a documented risk assessment signed by the channel owner. *Test:* configuration audit shows ambient disabled everywhere an assessment does not exist. Restores **Informed Intent** in the only way currently possible: by declining the feature that negates it.

**C3. Channel admission screening** (rows 2, 3, 7). Before the agent joins any channel: no counsel communications (see `08`), no externally shared (Slack Connect) channels, no channels carrying regulated personal data, MNPI or active-investigation material. *Test:* admission checklist on file for every channel where the agent is present.

**C4. Connector minimalism** (row 5). Narrowest scopes supporting the approved use case; no email connector in shared channels; scope additions require the same approval as initial grant. *Test:* quarterly diff of granted scopes against approved use cases produces no unexplained entries.

**C5. Service-account treatment** (rows 1, 5). The agent identity is registered in the identity governance program: explicit owner, scoped permissions, quarterly access recertification, review of channel memberships in every joiner-mover-leaver cycle. *Test:* the agent appears in the same recertification reports as privileged human accounts.

**C6. Rehearsed Exit** (rows 2, 8). Before deployment, execute and time the full removal procedure: agent out of a channel, connectors revoked, integration terminated, and confirmation of what happens to channel memory at each step. If memory disposition on exit cannot be confirmed, this is a blocking finding, not a risk acceptance. *Test:* a dated runbook with measured elapsed times exists and is re-run semiannually. This is the **Exits** primitive doing its only job: an exit that has never been rehearsed is a diagram.

**C7. Memory hygiene by reset** (row 2). Until enumeration and expiry tooling exists, time-bound accumulated context: periodic agent removal and re-admission on a schedule set per channel sensitivity. The cost is the product's convenience; convenience is the correct thing to spend. *Test:* reset log per channel.

**C8. Untrusted-input posture** (rows 6, 7). All channel content is treated as untrusted input to the agent. High-impact actions (merges to protected branches, external sends, record modifications, financial transactions) require human confirmation through a surface outside Slack. *Test:* attempt each high-impact action class in a controlled channel; confirm the out-of-band gate fires.

**C9. Ongoing classification function** (regulatory file `07`). A standing review, quarterly at minimum, of what channels actually use the agent for, mapped against EU Annex III categories, Korea's high-impact domains and applicable sectoral rules, with authority to remove the agent from drifted channels. *Test:* the review's output is a dated register naming channels, uses and classifications. This control has no vendor equivalent and no standard-catalogue equivalent yet; it is the study's principal original recommendation.

**C10. Deployer-side log custody** (row 9). Audit console output exported and retained under the deployer's retention schedule, with the reconstruction gap (memory state and non-determinism) documented in the risk register rather than discovered during an incident. *Test:* logs are producible for a sampled 90-day-old event.

## The honest cost accounting

C2, C3, C4 and C7 collectively decline most of what the product's launch materials sell. That is not a defect of the controls; it is the measurement of the governance discount defined in `01`. An organization unwilling to pay it should not deploy; an organization told the discount is zero is being sold to.

Final Liability rests with the Human.
