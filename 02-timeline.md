# 02 · Timeline

**Status:** [↻ living record, append-only] · v1.1.0 · 12 July 2026

Entries are dated, sourced (see `13-sources.md`) and never edited after entry; corrections are appended (see Corrections, below).

| Date | Event | Governance significance |
|---|---|---|
| 1 Aug 2024 | EU AI Act enters into force; staggered application begins | Baseline regulatory clock |
| 20 Aug 2024 | PromptArmor demonstrates prompt injection against Slack AI (Salesforce's native assistant), exfiltrating data from private channels via crafted public channel content; Slack deploys a patch after initially describing the behavior as intended | Establishes, pre-Claude, that channel content is instruction to a channel-reading agent |
| 2 Feb 2025 | EU AI Act Article 4 (AI literacy) and Article 5 (prohibited practices) apply | Deployer-side duties begin |
| 2 Aug 2025 | EU AI Act GPAI provider obligations apply | Provider-side; Anthropic's problem, not the deployer's |
| Oct 2025 | Anthropic launches Claude app for Slack: DMs, assistant panel, thread mentions. Admin approval required; Slack connector for Team and Enterprise lets Claude search content the individual user can access; public-thread drafts shown privately for review before posting | Per-user model. Attribution intact: one prompt, one person, one reviewed output |
| 19 Nov 2025 | European Commission proposes Digital Omnibus on AI | Regulatory timeline put in motion |
| Dec 2025 | Claude Code in Slack (beta): coding tasks routed from threads to Claude Code sessions, progress posted back | First step from conversation to delegated execution |
| 22 Jan 2026 | Korea AI Framework Act takes effect | High-impact AI duties, generative AI transparency, MSIT enforcement |
| 7 May 2026 | Provisional EU trilogue agreement on Digital Omnibus | Annex III high-risk deferral to 2 Dec 2027 signaled |
| 12–20 May 2026 | Mitiga Labs publishes security research on the Claude Code and Slack MCP integration: interception of MCP OAuth tokens via a rewritten local configuration file (12 May) and a demonstration that channel messages are treated as instructions by a Claude agent reading Slack, with detection guidance (20 May) | Injection and token theft move from analogous precedent to demonstrated against this product family's integration path, weeks before the multiplayer launch |
| 16 Jun 2026 | European Parliament formally endorses the Omnibus | |
| 23 Jun 2026 | Anthropic launches **Claude Tag** in beta for Enterprise and Team: one Claude per channel, persistent channel memory, cross-channel learning where permitted, ambient mode, admin-scoped connectors, organization- and channel-level spend limits, centralized audit console identifying initiating user and tools used. Runs on Opus 4.8. Replaces Claude in Slack; 30-day admin opt-in; forced switchover 3 Aug 2026 | The multiplayer pivot. Unit of deployment becomes the channel |
| 23–27 Jun 2026 | Post-launch independent analyses (MAESTRO threat model; trade-press security coverage) observe that the channel, not the user, is the effective security boundary and that ambient mode enlarges the reading surface | The security framing of the multiplayer pivot is set within its first week |
| 29 Jun 2026 | Council of the EU gives final approval to the Digital Omnibus on AI; publication in the Official Journal expected July 2026, entry into force three days after | Annex III high-risk: 2 Dec 2027. Annex I embedded: 2 Aug 2028. Article 50 transparency: still 2 Aug 2026 (Art 50(2) machine-readable marking: from 2 Aug 2026 for systems newly placed on the market, grace period to 2 Dec 2026 for systems on the market before that date). NCII/CSAM prohibition: 2 Dec 2026 |
| 3 Aug 2026 | **Scheduled:** forced migration of legacy Claude in Slack app to Claude Tag | Vendor-paced deployment; organizations that have not assessed will run the multiplayer architecture by default |

## Corrections

- **v1.1.0 (12 July 2026).** The v1.0.0 entry dated 23–27 Jun 2026 attributed the Mitiga research to that window and to "the Claude and Slack MCP integration" generically. Primary sources establish publication on 12 and 20 May 2026, against the Claude Code and Slack MCP integration specifically, with trade-press reporting on 5 and 27 June 2026. That entry is superseded by the 12–20 May and 23–27 Jun entries above. The v1.0.0 table also placed the PromptArmor demonstration before the EU AI Act's entry into force; the rows are now in date order and the PromptArmor entry is dated precisely (20 Aug 2024). The v1.0.0 phrasing "provider watermarking under Art 50(2): 2 Dec 2026" implied a blanket deferral; the corrected 29 Jun entry records the grace-period structure.

Final Liability rests with the Human.
