# 03 · Product Architecture and Control Surfaces

**Status:** [✓ final] · v1.1.0 · 12 July 2026

## What the product is

Claude Tag is a persistent agent that joins Slack channels as a team member under a single organizational identity. The identity model inverts the legacy app's: where the per-user app acted under the tagging user's own permissions and billing, Tag acts under an organization-scoped agent identity with admin-defined tool access, and channel work is billed to the organization. Any channel member can tag @Claude to delegate a task; the agent decomposes the task into stages and executes them asynchronously, sometimes over hours or days, using whatever tools have been scoped to it, posting progress and results back into the thread. It retains memory of the channels it inhabits and, where granted permission, gathers context from other channels and connected data sources (Anthropic states it does not report from private channels). With ambient mode enabled it monitors its channels continuously, flags what it judges relevant and follows up on stalled threads without being asked. It runs on Opus 4.8 and, per independent technical analysis, executes tasks in per-session sandboxed microVMs.

Three properties define the governance object:

1. **Shared identity.** One Claude per channel serves every member. There is no per-user agent instance in the channel context.
2. **Persistent memory.** Context accumulates across sessions and users. The agent's behavior at time T is a function of everything it has read up to T, which no one can enumerate.
3. **Initiative.** In ambient mode, the trigger for action is the agent's own judgment of relevance, not a human instruction.

## Control surfaces the vendor provides

Recording these accurately matters, because the study's thesis is not that controls are absent but that they are misaligned with the product's risk.

| Control | What it does | What it does not do |
|---|---|---|
| Admin app approval | Workspace admins must approve the app; org-wide or per-workspace deployment | Does not govern per-channel risk once approved |
| Channel scoping | Admins choose which channels the agent joins and which connectors each channel gets | The channel is the unit; no per-user entitlement within a channel |
| Connector scoping | Tool access (repos, docs, email, SaaS) is admin-granted | Scopes are static grants, not task-scoped or time-boxed |
| Spend limits | Token spend caps set at organization and channel level; work that would exceed a cap is declined | A budget control, not a conduct control: it bounds the cost of misuse, not its occurrence |
| Private channel exclusion | Cross-channel learning does not report from private channels (vendor statement) | Public channel content, including pasted confidential material, is in scope |
| Ambient mode toggle | Off/on per configuration; vendor launch guidance reportedly recommends starting with ambient disabled | Default posture and per-channel granularity: see `12-open-questions.md` |
| Draft-privately review (legacy app) | Public-thread drafts shown to the requester before posting | Applies to the per-user flow; the agentic multi-stage flow posts work products directly |
| Centralized audit console | Logs which user initiated each request and what tools the agent used | Does not capture memory state, does not make outputs reproducible, retention unverified |
| Data handling | Commercial Slack data handled per Anthropic's DPA; not used for training by default | Vendor-held memory remains non-enumerable by the deployer |

## The architectural observation that organizes everything else

Slack's permission model is channel-based. Enterprise entitlement models, and every accountability framework worth the name, are person-based. The product inherits Slack's model: the relevant question inside the product is "what can this channel's members collectively ask the agent to do," not "what may this person do." Every governance failure analyzed in this study (`04` through `08`) is a downstream consequence of that single substitution of the channel for the person as the unit of control.

Final Liability rests with the Human.
