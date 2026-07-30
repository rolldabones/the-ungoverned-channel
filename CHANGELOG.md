# Changelog

All notable changes to this case study are documented here. Superseded claims are marked in place, never deleted. The update protocol in the README defines what triggers an entry.

## [1.3.2] · 2026-07-30 · Regulatory-currency update

Update protocol trigger 3, a regulatory event: adopted text. Currency only. No finding, verdict, prediction or open question is revised.

### Changed
- 07-regulatory-mapping.md re-dated to v1.1.1 and 30 July 2026. The Digital Omnibus on AI is no longer awaiting Official Journal publication. It was adopted as Regulation (EU) 2026/1744 of 8 July 2026, published on 24 July 2026 (OJ L, 2026/1744, 24.7.2026) and in force since 27 July 2026. The prior claim is marked superseded in the file rather than deleted, per the update protocol. The file status line now records verification against the published regulation.
- README version and last-updated line moved in lockstep.

### Open
- Whether the Article 50 marking grace period cut (six months to three, 2 December 2026) and the two new Article 5 prohibitions added by the published text bear on a Slack-agent deployer is flagged in 07-regulatory-mapping.md and not resolved here. It is scoped to a substantive review pass. The 2 August 2026 row in that file, which states that deployer-side Article 50 obligations are unaffected by the Omnibus, is explicitly marked as pending confirmation.

## [1.3.1] · 2026-07-15 · Link-hygiene patch

Repository-metadata patch outside the five substantive update triggers, like v1.3.0.

### Changed
- Removed the claude-cowork-legal-onboarding entry from the README's Part of the ecosystem section; that repository was retired and deleted by the maintainer on 15 July 2026. Three nearest neighbors remain.

### Unchanged
- The analysis itself. No claim, control, prediction or open question is altered by this release. Files 01 through 14 are untouched.

## [1.3.0] · 2026-07-15 · Ecosystem integration

Repository-metadata release under the repository improvement program. This release sits outside the five substantive update triggers in the README's update protocol, which govern the analysis; it changes repository plumbing only.

### Added
- README section "Part of the ecosystem" linking the canonical ECOSYSTEM.md in the profile repository plus four nearest neighbors (claude-cowork-legal-onboarding, ai-governance-for-boards, AI-Impact-Assessment-Tool, slow-ai-kitchen), placed after Doctrinal frame.

### Changed
- README header version and last-updated date.

### Unchanged
- The analysis itself. No claim, control, prediction or open question is altered by this release. Files 01 through 14 are untouched.

## [1.2.0] · 2026-07-12 · Positioning and engagement posture

### Added
- README section "In what capacity": the study is personal work by a concerned user of these tools; not an audit, an assurance engagement or legal advice; written on behalf of no organization, client or employer; meant to be useful to enterprises deciding whether and how to deploy Claude Tag and, where the observations hold up, to the vendor.

### Changed (prior posture superseded)
- The README engagement section is retitled "Corrections and contributions" and rewritten. v1.1.0 committed to logging vendor answers "with attribution and date"; that framing read as putting respondents on the record and is withdrawn. The study now asks nothing of the vendor and updates against the public record; corrections are attributed only with the contributor's consent, and informal pointers are never quoted or cited. `CONTRIBUTING.md` and the `12-open-questions.md` preamble are aligned.

### Unchanged
- The analysis itself. No claim, control, prediction or open question is altered by this release.

## [1.1.1] · 2026-07-12 · Link verification patch

### Corrected (prior claims superseded, marked in place)
- **Mitiga day-level dates.** v1.1.0 claimed 12 and 20 May 2026 from a cached blog listing. The vendor's listing re-dates posts between accesses (22 June and 7 July 2026 as of 12 July); trade press fixes the token-theft chain no later than 5 June 2026 and the Slack demonstration no later than 27 June 2026. `02` now claims the May–June window with day-level dates held as Unknown / Insufficient data; `06` §A adjusted to match; correction appended in `02`.
- **Item 28 re-attributed.** The "Security Boulevard" piece is a Grip Security vendor blog post syndicated through Security Boulevard; now labeled as such and cited only for the service-account framing.

### Added
- New Tier 3 source: Anthropic's Claude Code in Slack documentation, whose caution that Claude "may follow directions from other messages in the context" is added to `06` §A as vendor corroboration of the untrusted-input posture.
- Verified direct links added for the Mitiga token-theft post, the Ken Huang MAESTRO analysis, the Deriv teardown (exact title) and the Tessl item (exact title). Every entry in `13-sources.md` now carries a verified link or an explicit dating caveat.

### Unchanged
- All other files retain their prior stamps. No open question resolved; no prediction affected.

## [1.1.0] · 2026-07-12 · Verification pass and correction release

### Corrected (prior claims superseded, marked in place)
- **Mitiga dating and scope.** v1.0.0 dated the Mitiga research 23–27 June 2026 and named "the Claude and Slack MCP integration" generically. Primary sources establish publication on 12 and 20 May 2026, against the Claude Code and Slack MCP integration specifically, with trade-press reporting on 5 and 27 June 2026. Timeline split into a May research entry and a June post-launch-analysis entry, with a corrections note appended in `02`; `06-threat-surface.md` §A corrected accordingly ("two years apart" narrowed to "less than two years apart").
- **Colorado.** v1.0.0 described the 2024 Colorado AI Act as "amended and delayed to mid-2026." The Act never took effect: enforcement was stayed in litigation in April 2026 and SB 26-189 (signed 14 May 2026, effective 1 January 2027) repealed and replaced it with a disclosure-based framework for automated decision-making technology in consequential decisions. `07-regulatory-mapping.md` §C rewritten; SB 26-189 added to Tier 1 sources with Tier 2 analysis.
- **Article 50(2).** The 2 December 2026 date is a grace period for systems on the market before 2 August 2026, not a blanket deferral; systems newly placed on the market comply from 2 August 2026. Corrected in `02` and `07`.
- **Timeline chronology.** PromptArmor entry dated precisely (20 August 2024) and ordered after the EU AI Act entry-into-force row; Slack's subsequent patch noted.

### Resolved source placeholders (all three from v1.0.0)
- Vendor switchover page: Anthropic Help Center article cited directly. Mitiga primary posts cited directly (12 and 20 May 2026), with CSO Online (5 June 2026) added as reporting. PromptArmor primary disclosure cited directly (previously reached only through Chen et al., SecAlign), with The Register's contemporaneous report of Slack's patch added. Reuters placeholder replaced by The Register launch coverage (23 June 2026), with Reuters quotes noted as carried in TechRepublic (24 June 2026). Sources renumbered 1–29; a "Superseded citation routes" section records the prior routes.

### Added
- `03`: spend-limits control row (organization- and channel-level token caps; recorded as a budget control, not a conduct control); identity-model contrast between the legacy per-user app and Tag's organization-scoped agent identity; note that vendor launch guidance reportedly recommends starting with ambient mode disabled. The 23 June timeline entry now lists spend limits among launch controls.
- README: reading paths by audience; a "Corrections, contributions and the vendor" section including a standing invitation to the vendor to resolve Q1–Q10 on the record.
- `CONTRIBUTING.md` (what is accepted, mechanism, logging, single-author accountability) and `CITATION.cff` (citation metadata).

### Unchanged
- Files 01, 04, 05, 08, 09, 10, 11, 12, 14 and LICENSE.md carry no changes and retain their v1.0.0 stamps. No open question is resolved by this release; no prediction is affected.

## [1.0.0] · 2026-07-11 · Initial public release

### Contents
- README with thesis, structure, update protocol, provenance and bias disclosure, doctrinal frame.
- Files 01 through 14: abstract and method; append-only timeline; product architecture and control surfaces; the multiplayer problem; the feature-control ledger (central artifact, with the governance discount defined); threat surface; regulatory mapping verified against the Digital Omnibus as approved by the Council on 29 June 2026; privilege, discovery and legal process across divergent regimes; ten testable compensating controls C1 to C10; the verdict stress-tested against five counterarguments; predictions register P1 to P7 with confidence levels and review dates, two entries registered against the thesis; open questions register Q1 to Q10, all held as Unknown / Insufficient data; tiered sources with one exclusion logged; and the enterprise question set E1 to E25, jurisdiction agnostic and product agnostic, with possible resolutions.

### Drafting provenance (pre-release, summarized)
- v0.1 (internal): built from and superseding a same-day memorandum. Principal corrections relative to the memo, documented in full in `01-abstract-and-method.md`: attribution claim narrowed to output-level accountability; regulatory mapping rebuilt on the post-Omnibus timeline (Annex III high-risk deferred to 2 December 2027; Article 50 deployer transparency live 2 August 2026); privilege analysis made jurisdiction-aware; external-liability / internal-accountability distinction replacing rhetoric; multiplayer social dynamics and comparison class added.
- v0.2 (internal): enterprise question set added; Q-series (factual unknowns) and E-series (decision questions) registers formally distinguished.
- Finalization: superseded memo removed from the repository; version stamps unified at 1.0.0; source entry for the EU AI Act corrected to reflect that Official Journal publication of the Omnibus is pending as of this date.

### Next scheduled events
- 3 August 2026: forced migration date (timeline entry pending outcome).
- 3 February 2027: first prediction review (P6).
