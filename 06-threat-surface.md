# 06 · Threat Surface

**Status:** [✓ final] · v1.1.1 · 12 July 2026

This file records the security dimension only to the depth governance requires: what can go wrong, how it is demonstrated and what the multiplayer setting adds. Full technical treatments exist elsewhere (see MAESTRO analysis and Mitiga research, `13-sources.md`).

## A. Prompt injection: demonstrated, not hypothetical

The lineage matters. In August 2024, PromptArmor demonstrated injection against Slack AI itself: crafted content in a public channel caused the assistant to exfiltrate data from private channels the attacker could not read. In May and June 2026, Mitiga published research on the Claude Code and Slack MCP integration: malicious instructions embedded in channel content can cause a Claude agent with channel access to follow the attacker's commands rather than the user's. Two independent demonstrations, less than two years apart, against two vendors, through the same architectural feature: an agent that reads the channel treats the channel as instruction. The vendor's own documentation for the Claude Code in Slack integration concedes the posture, cautioning that Claude "may follow directions from other messages in the context" and should be used only in trusted Slack conversations.

The multiplayer setting multiplies the injectors. In the per-user model the trust question is "do I trust my own inputs." In the channel it is "do I trust every member, every document any member pastes, every message synced from an externally shared channel and every connected data source." The agent has no intent hierarchy among these; an attacker needs to be, or to compromise, or merely to get a document in front of, any one of them. Ambient mode then removes the last gate: the agent reads everything continuously, so the injection does not even need to be adjacent to a tag.

## B. Permission laundering

Not a breach but a bypass. The agent lawfully reads channel X, then restates X's content in channel Y, or to a member of X who lacks access to the underlying connected source, or summarizes a discussion into a thread whose membership differs from the source conversation's. Every individual access was authorized; the aggregate flow defeats the entitlement design. Cross-channel learning generalizes the mechanism into a product feature. For organizations running information barriers (MNPI, conflicts, deal teams, HR investigations) this is the single most consequential row of the ledger, because the failure produces no log entry that looks like a failure.

## C. Memory as attack surface and liability surface

Persistent memory is dual-use against the deployer. As attack surface: an injected instruction can be designed to persist ("whenever asked about X, do Y"), making the memory a beachhead that outlives the injecting message. Whether Claude Tag's memory is susceptible to durable instruction-planting is unverified (`12-open-questions.md`), but the attack class is established in the agent literature. As liability surface: the memory is a vendor-held, non-enumerable record of organizational knowledge, which makes it simultaneously a discovery target, a GDPR object and a privilege hazard (`08`).

## D. The blast radius equation

The impact of any single successful manipulation equals the union of the connectors scoped to that channel. A channel with repo write access, email and a SaaS admin connector converts one crafted message into code changes, external communications and record modifications. This is why `09` treats connector minimalism as a first-order control rather than hygiene: scope is the only variable in the blast radius equation the deployer fully controls.

## E. What monitoring can and cannot do

The audit console supports detection of anomalous activity patterns. It does not support reconstruction, for two structural reasons: the memory state that conditioned a given action drifts continuously and is not exportable, and generation is non-deterministic, so replaying the same inputs does not reproduce the output. Incident response should therefore be planned around containment and scope-revocation speed rather than root-cause replay. The tested time-to-remove (agent out of channel, connectors revoked, integration terminated) is the metric that matters, and it should be measured before deployment, not during an incident.

Final Liability rests with the Human.
