# 13 · Sources

**Status:** [↻ living record] · v1.1.3 · 17 August 2026 (KST)

Tiered per the authority hierarchy in `01`. Sources are cited in the tier they occupy, not the tier their confidence implies. Accessed 11–12 July 2026 unless noted.

## Tier 1 · Statute, adopted regulation, institutional acts

1. Regulation (EU) 2024/1689 (EU AI Act); **Regulation (EU) 2026/1744** of the European Parliament and of the Council of 8 July 2026 amending Regulations (EU) 2024/1689, (EU) 2018/1139 and (EU) 2023/1230 as regards the simplification of the implementation of harmonised rules on artificial intelligence (Digital Omnibus on AI), **OJ L, 2026/1744, 24.7.2026**, ELI http://data.europa.eu/eli/reg/2026/1744/oj, **in force 27 July 2026**.
2. Council of the EU, "Artificial Intelligence: Council gives final green light to simplify and streamline rules," press release, 29 June 2026. consilium.europa.eu. (Final approval; new high-risk dates 2 Dec 2027 / 2 Aug 2028; Art 50(2) grace period to 2 Dec 2026 for systems on the market before 2 Aug 2026; NCII/CSAM prohibition.)
3. Council of the EU, press release on provisional agreement, 7 May 2026 (updated 18 May 2026). consilium.europa.eu.
4. Korea, Framework Act on the Development of Artificial Intelligence and Establishment of Trust, effective 22 January 2026.
5. Colorado, SB 26-189 (Automated Decision-Making Technology Act), signed 14 May 2026, effective 1 January 2027; repeals and replaces SB 24-205 (Colorado AI Act, 2024), which never took effect.

## Tier 2 · Official guidance and reputable legal analysis of Tier 1 acts

6. Gibson Dunn, "EU AI Act Omnibus Agreement — Postponed High-Risk Deadlines and Other Key Changes," May 2026.
7. Covington, Inside Privacy, "EU AI Act Update: Timeline Relief, Targeted Simplification, and New Prohibitions," 18 May 2026.
8. White & Case, "EU agrees Digital Omnibus deal to simplify AI rules," 14 May 2026.
9. DLA Piper GENIE, Digital AI Omnibus update (employment-context deferral analysis), June 2026.
10. Court of Justice of the EU, Akzo Nobel Chemicals Ltd v Commission, C-550/07 P (2010) (in-house counsel and legal professional privilege).
11. Norton Rose Fulbright, "Colorado enacts revised AI law," May 2026 (SB 26-189 analysis; ADMT framework, disclosure duties, 1 January 2027 effective date).

## Tier 3 · Vendor documentation and announcements

12. Anthropic, "Introducing Claude Tag," 23 June 2026. anthropic.com/news/introducing-claude-tag. (Multiplayer identity, channel memory, cross-channel learning, ambient mode, private-channel exclusion, migration and 30-day opt-in, Opus 4.8.)
13. Anthropic, "Claude and Slack," October 2025. anthropic.com/news/claude-and-slack. (Per-user model, admin approval, connector scoping, private draft review.)
14. Slack Marketplace, Claude app listing: security and data-handling disclosures, DPA reference, retention pointers. slack.com/marketplace/A08SF47R6P4-claude.
15. Anthropic Help Center, "Get started with Claude in Slack." support.claude.com/en/articles/11506255-get-started-with-claude-in-slack. (Describes the 3 August 2026 transition of Claude in Slack to Claude Tag. Read on 13 August 2026 (KST), the documented mechanism is in-place replacement with an account-specific Legacy deprecation cutover, not a blanket forced migration on that date; the annotation previously characterised it as a switchover and is corrected. Also covers legacy app surfaces and admin approval.)
16. Anthropic, Claude Code documentation, "Claude Code in Slack." code.claude.com/docs/en/slack. (Vendor caution that Claude "may follow directions from other messages in the context" and should be used only in trusted Slack conversations; Claude Tag replacement notice.)

## Tier 4 · Security research

17. Mitiga Labs, "Claude Code + Slack: How an AI Agent Integration Becomes a Compromise Path" (earlier listing title: "Slack Compromise via Claude Code: Managing AI Agent Security Risks"), published by 27 June 2026; the vendor's listing re-dates posts between accesses (20 May 2026 at one access, 22 June 2026 as of 12 July 2026). mitiga.io/blog/007-license-to-skill-p-2-slack-compromise-through-claude-code. (Channel messages treated as instructions by a Claude agent reading Slack; scope and detection guidance.)
18. Mitiga Labs, "MCP Token Theft in Claude Code: A Man-in-the-Middle Attack Chain" (earlier listing title: "Claude Code MCP Token Theft: MitM Attack Explained"), May 2026, reported 5 June 2026 (item 24); site listing shows 7 July 2026 as of access. mitiga.io/blog/claude-code-mcp-token-theft-mitm. (MCP OAuth token interception via rewritten local configuration file.)
19. PromptArmor, "Data Exfiltration from Slack AI via Indirect Prompt Injection," 20 August 2024. promptarmor.com/resources/data-exfiltration-from-slack-ai-via-indirect-prompt-injection. (Also documented in Chen et al., "SecAlign," arXiv:2410.05451.)
20. Ken Huang, "MAESTRO Threat Analysis of Claude Tag: The Attack Surface Is the Whole Chain," June 2026. kenhuangus.substack.com/p/maestro-threat-analysis-of-claude. (Layered threat model; channel as injection ingress.)
21. Deriv (derivai.substack.com), "Inside Claude Tag for Slack: The root shell behind the friendly @Claude mention," July 2026. derivai.substack.com/p/inside-claude-tag-slack-root-shell-microvm. (Technical teardown: Firecracker microVM sandboxing, connector credential handling, channel as security boundary.)

## Tier 5 · Credible trade press

22. TechCrunch, "Anthropic's Claude Tag is learning your company, one Slack message at a time," 23 June 2026.
23. Tech Times, "Claude Tag Brings Ambient AI to Slack: Admins Have Until August 3 to Migrate," 27 June 2026. (Audit console detail; Mitiga reporting; vendor launch guidance reportedly recommending ambient mode start disabled.)
24. CSO Online, "Claude Code has an MCP security problem — and your developers are already using it," 5 June 2026. (Reports the Mitiga disclosures; Check Point CVE context.)
25. The Register, "Anthropic reimagines Claude in Slack as nosy, always-on agentic AI coworker," 23 June 2026. (Launch coverage; migration credits and 3 August retirement per the vendor's support page. Reuters launch reporting, including Slack and Anthropic executive quotes, is carried in TechRepublic, 24 June 2026.)
26. The Register, "Slack AI can leak private data via prompt injection," 21 August 2024. (Contemporaneous report including Slack's patch statement.)
27. Tessl, "Claude Code comes to Slack as team chat and coding converge," 16 December 2025. tessl.io/blog/claude-code-comes-to-slack-as-team-chat-and-coding-converge.
28. Grip Security, "Claude Tag Security: Governing AI Identities in Slack," 30 June 2026, security-vendor blog, syndicated via Security Boulevard. grip.security/blog/claude-tag-security. (Cited for the service-account framing of agent identities only, not for product-fact claims.)

## Tier 6 · Vendor marketing and self-reports (no evidentiary weight)

29. Anthropic statement that 65 percent of its product team's code is created through its internal Claude Tag (launch materials, 23 June 2026).
30. Salesforce/Slack executive statements on "multiplayer AI" (launch coverage, June 2026).

## Excluded

Windowsnews.ai coverage of Claude Tag was reviewed and excluded: quoted expert could not be verified and the outlet's provenance is unclear. Aggregator restatements (letsdatascience.com and similar) are used only as pointers to primary reporting, never as sources.

## Superseded citation routes

- v1.0.0 cited the PromptArmor demonstration only through Chen et al. (SecAlign); the primary disclosure is now cited directly (item 18).
- v1.0.0 carried three placeholders ("direct page to be added"): the vendor switchover page (resolved, item 15), the Mitiga primary (resolved, items 17 and 18) and a Reuters item (replaced by items 23 and 25; Reuters quotes reachable through TechRepublic as noted).
- v1.1.0 dated the Mitiga posts 12 and 20 May 2026 from a cached listing and attributed item 28 to Security Boulevard as trade press; v1.1.1 records the dating instability on the Mitiga listing and re-attributes item 28 as a security-vendor blog syndicated through Security Boulevard.

Final Liability rests with the Human.
