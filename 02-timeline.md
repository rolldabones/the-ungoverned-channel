# 02 · Timeline

**Status:** [↻ living record, append-only] · v1.0.0 · 11 July 2026

Entries are dated, sourced (see `13-sources.md`) and never edited after entry; corrections are appended.

| Date | Event | Governance significance |
|---|---|---|
| Aug 2024 | PromptArmor demonstrates prompt injection against Slack AI (Salesforce's native assistant), exfiltrating data from private channels via crafted public channel content | Establishes, pre-Claude, that channel content is instruction to a channel-reading agent |
| 1 Aug 2024 | EU AI Act enters into force; staggered application begins | Baseline regulatory clock |
| 2 Feb 2025 | EU AI Act Article 4 (AI literacy) and Article 5 (prohibited practices) apply | Deployer-side duties begin |
| 2 Aug 2025 | EU AI Act GPAI provider obligations apply | Provider-side; Anthropic's problem, not the deployer's |
| Oct 2025 | Anthropic launches Claude app for Slack: DMs, assistant panel, thread mentions. Admin approval required; Slack connector for Team and Enterprise lets Claude search content the individual user can access; public-thread drafts shown privately for review before posting | Per-user model. Attribution intact: one prompt, one person, one reviewed output |
| 19 Nov 2025 | European Commission proposes Digital Omnibus on AI | Regulatory timeline put in motion |
| Dec 2025 | Claude Code in Slack (beta): coding tasks routed from threads to Claude Code sessions, progress posted back | First step from conversation to delegated execution |
| 22 Jan 2026 | Korea AI Framework Act takes effect | High-impact AI duties, generative AI transparency, MSIT enforcement |
| 7 May 2026 | Provisional EU trilogue agreement on Digital Omnibus | Annex III high-risk deferral to 2 Dec 2027 signaled |
| 16 Jun 2026 | European Parliament formally endorses the Omnibus | |
| 23 Jun 2026 | Anthropic launches **Claude Tag** in beta for Enterprise and Team: one Claude per channel, persistent channel memory, cross-channel learning where permitted, ambient mode, admin-scoped connectors, centralized audit console identifying initiating user and tools used. Runs on Opus 4.8. Replaces Claude in Slack; 30-day admin opt-in; forced switchover 3 Aug 2026 | The multiplayer pivot. Unit of deployment becomes the channel |
| 23–27 Jun 2026 | Mitiga publishes prompt injection research specific to the Claude and Slack MCP integration; independent analyses note the channel, not the user, is the effective security boundary and ambient mode enlarges the reading surface | Injection moves from analogous precedent to demonstrated against this product |
| 29 Jun 2026 | Council of the EU gives final approval to the Digital Omnibus on AI; publication in the Official Journal expected July 2026, entry into force three days after | Annex III high-risk: 2 Dec 2027. Annex I embedded: 2 Aug 2028. Article 50 transparency: still 2 Aug 2026 (provider watermarking under Art 50(2): 2 Dec 2026). NCII/CSAM prohibition: 2 Dec 2026 |
| 3 Aug 2026 | **Scheduled:** forced migration of legacy Claude in Slack app to Claude Tag | Vendor-paced deployment; organizations that have not assessed will run the multiplayer architecture by default |

Final Liability rests with the Human.
