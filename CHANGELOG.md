# Changelog

All notable changes to this case study are documented here. Superseded claims are marked in place, never deleted. The update protocol in the README defines what triggers an entry.

## [1.5.2] · 2026-10-20 · License text corrected against the Creative Commons legal code

- LICENSE: two defects against the Creative Commons legal code corrected (the space in 'ShareAlike. In'; the CC0 sentence of the closing notice). Operative terms unchanged.
- README masthead, How to Cite and `CITATION.cff` to v1.5.2. Outside the update protocol's five triggers; no finding of the study changes.

## [1.5.1] · 2026-10-17 · Editorial patch: doctrine short forms and house style

Session T3 of the whole-account review of 15 October 2026 (KST); review doc sections 1 and 8, reviewer report 15. An editorial patch outside the update protocol's five triggers, made under the account's review: no claim, prediction, score, control or question changes, and nothing is superseded.

- **README, Doctrinal frame.** The three doctrine glosses now carry the short forms of DOCTRINE.md v1.2.0 section 8. The Slow AI gloss had read "adopted at the deployer's pace, not the vendor's", a tempo rule the canon does not state (DOCTRINE.md section 1: "not a speed limit"); the case study's own question about the timing of vendor change is kept, stated as a question about whether the three tests can be met. The Informed Intent gloss ("a named human authorizes a specified task, with understood tolerances") now names the four elements and the authorizer conditions; the Final Liability gloss names the three attributes.
- **README, Part of the ecosystem** names the-ai-generalist, which names this repository (ECOSYSTEM.md protocol item 9).
- **`07-regulatory-mapping.md` to v1.1.5**: "behaviour" and "categorisation" in US spelling; the GDPR Article 35(1) test, bold inside a bold sentence and so rendered broken, is set in italics; the Art 50(3) gloss is put in parentheses so the sentence carries no serial comma; "catalogue" reads "catalog".
- **`08-privilege-discovery-legal-process.md` to v1.1.1** and **`09-compensating-controls.md` to v1.1.1**: three serial commas removed and "catalogue" reads "catalog".
- Recorded and not edited: the Article 50 row's struck "arguably discharges" sentence (doc section 1) was already re-rowed to "evidences" in v1.5.0, and the struck text stays visible under the protocol; the raw-pipe tables in `05` and `11` and the How to Cite title (reviewer report 15, items B3 and A-series) were already correct in v1.5.0; "harmonised" in `13-sources.md` is the Regulation's own title and stays.
- README version line and How to Cite to 1.5.1 and `CITATION.cff` to 1.5.1 in lockstep. The closing line is added, last, to this changelog.

## [1.5.0] · 2026-10-15 · Vendor re-run under update protocol trigger 1

Session T1 of the whole-account review of 15 October 2026 (KST). Three vendor pages read that day settle four open questions, score two predictions early and supersede the v1.4.0 account of the Legacy cutover. Fifteen files move, twelve of them content files; every superseded claim is marked in place and nothing is deleted. The v1.4.4 scope note, which declined to touch the removal-as-erasure wording at ledger row 2 and E11 without vendor confirmation, is discharged: the confirmation exists and says removal erases nothing.

- **Legacy retired 5 October 2026.** `02-timeline.md` to v1.3.0: a 5 Oct 2026 row appended from *Migrate from the earlier Claude in Slack* ("Since October 5, 2026 ... no longer answers in channels of a workspace paired with your Claude organization"; "You also can't switch a workspace or channel to Legacy anymore"), the 13 Aug 2026 row's "account-specific cutover date" marked superseded in place and the 23 Jun 2026 row's "forced switchover 3 Aug 2026" carrying the inline strike mark the README promised. The same wording is marked superseded in `01-abstract-and-method.md` (v1.0.2), `10-verdict.md` (v1.0.2), `14-enterprise-question-set.md` E24 (v1.0.2, where E11's resolution (2), reset as the instrument of erasure, is also struck against the same page) and `README.md`. A currency update, not a correction of substance: the v1.4.0 account was accurate when read.
- **`05-feature-control-ledger.md` to v1.2.0.** Row 2 rebuilt: ~~periodic memory reset via agent removal and re-admission~~ struck, because *Data lifecycle and deletion* states that `/remove @Claude` deletes nothing; the control is an Owner's **Remove this scope** plus memory-file entry deletion. Row 4 narrowed: **Respond automatically** on by default, per channel, no estate-wide switch; **Channel member edits: Block** added. Row 8 recast: ~~pin scopes to Legacy~~ struck as unexecutable; the "private deadline" residual superseded. Row 11 narrowed: Claude is off by default in guest and Slack Connect channels. Rows 10 and 11 rejoined to the table (they followed a blank line and rendered as raw pipes).
- **`09-compensating-controls.md` to v1.1.0.** C7 rebuilt on scope removal with a preservation check first, its 8 September 2026 condition discharged; C2 gains the Block companion; C3's Slack Connect limb recast as keep-the-default-and-audit-overrides and mapped to row 11; C11 added for rows 10 and 11. Every ledger row now has a control.
- **`11-predictions-register.md` to v1.1.0.** P2 confirmed early (enumeration and per-channel reset shipped; expiry not); P4 confirmed early (default-on, per channel). Outcomes dated and sourced; the predictions themselves are untouched. A second P6 premise note records the closed population. P7 moved into its own table below the P6 notes so that it renders.
- **`12-open-questions.md` to v1.3.0.** Q1, Q2, Q4 and Q5 resolved, Q7 narrowed, each with the answer in the row and the resolving source in `13`. Q2 resolved adversely: no retention period during the beta, transcripts and memory outside the organization's data exports and the Compliance API.
- **`08-privilege-discovery-legal-process.md` to v1.1.0.** ~~The novel object is the memory, not the transcript~~ struck: the vendor-held session transcript, which holds edited and deleted messages and connected-tool data, outlives the Slack record and cannot be deleted per thread, is recorded as a second discovery and GDPR object, and the three operational questions in section B are answered against the page.
- **`07-regulatory-mapping.md` to v1.1.4.** The 2 Aug 2026 row re-rowed: Art 50(1) is a provider design duty; the deployer duty that could bite is Art 50(4), second subparagraph; "the @Claude handle arguably discharges this" struck for "evidences". "new Art 5 NCII/CSAM prohibition" reads as the two prohibitions, points (ba) and (bb). ~~The Omnibus's parallel GDPR amendments~~ corrected: the GDPR Omnibus is a separate proposal, adoption status Unknown.
- **`06-threat-surface.md` to v1.1.2.** Skills repositories added to the injection surface from the vendor's migration page.
- **`13-sources.md` to v1.2.0.** Items 31 to 33 (the three vendor pages) added to Tier 3 out of sequence so nothing renumbers; item 15 marked superseded for the cutover mechanism; "item 18" corrected to item 19 in Superseded citation routes.
- **`README.md`.** How to Cite read "*None*" for the title since v1.4.2; it now carries the CITATION.cff title. "the last sentence of `10`" reads "the bold sentence closing `10`". Why a living document names the 5 October 2026 retirement.
- **Not changed, recorded.** The US privilege paragraph in `08.A` cites no authority (reviewer report 15, item B5: *Upjohn*, *Hickman*, FRE 502(b)); E1 to E25 as a row-form register (B2); Mitiga's 29 September 2026 update to item 17 (A11, not re-read here); the "Opus 4.8" quotation at item 12 and the 23 Jun 2026 row is the launch announcement's own wording and stands as quotation. All wait for a later release.
- **Version occurrences.** `README.md` masthead and How to Cite block, and `CITATION.cff` `version` and `date-released`, to 1.5.0 and 2026-10-15.

## [1.4.4] · 2026-09-08 · C7 conditioned on the C6 confirmation

Standing item 15 of `account-maintenance/RUNBOOK.md` §8, registered 7 September 2026 on a reading of the instruments and remediated here. One sentence added to one control. No other file in this repository is changed, and no claim about what removal achieves in law is made or implied anywhere in this release.

- **`09-compensating-controls.md` to v1.0.1. C7 is now conditional on the C6 confirmation.** ~~C7 as published prescribed periodic agent removal and re-admission as memory hygiene on its own terms, and so stood as a control a deployer could record as in place without holding the confirmation C6 requires.~~ **STRUCK.** C6 makes unconfirmed memory disposition on exit a blocking finding rather than a risk acceptance, and `12-open-questions.md` records both the disposition question (Q1) and admin enumerability (Q5) as Unknown / Insufficient data against vendor documentation. A reset schedule run without that confirmation is a schedule of an operation whose effect on memory is unknown. The added sentence states the condition, states that C7 achieves nothing while the condition is unmet, and states that C7 must not be recorded as a control in place in that state. The C7 control text, its rationale and its test are otherwise unchanged.
- **Status line re-dated** on `09-compensating-controls.md`, whose body this release changes. A status line that predates its own body is a currency defect in its own right.
- **Version occurrences.** `README.md` masthead and How to Cite block, and `CITATION.cff` `version` and `date-released`, to 1.4.4 and 2026-09-08.
- **Scope, stated because it was considered and declined.** Removal-as-erasure wording exists in this repository at `05-feature-control-ledger.md` row 2 and `14-enterprise-question-set.md` E11 resolution (2). Neither is touched here. ⚠ Any wording offered as a route to a data subject's erasure right is a representation about a third party's processing and needs vendor confirmation and counsel review before it stands; that is a separate question from whether C7 carries its condition, and widening this release to answer it would have made the representation rather than examined it. `08-privilege-discovery-legal-process.md` was read on 7 September and again on 8 September 2026 and carries no such wording: its only removal reference, at line 19, runs the other way, asking whether routine removal destroys what a preservation duty required be kept. No defect is registered against `08`.
- **This release rides ahead of standing item 4.** If Claude Tag reaches general availability the study is re-run under that item, and C7 is revisited then: the condition added here is drawn against a product whose memory disposition is undocumented, and a general-availability release that documents it changes the input to this control rather than the control's logic.

## [1.4.3] · 2026-09-06 · Citation infrastructure and doctrine citation line

Citation infrastructure, doctrine citation line and lockstep maintenance. Session C of the September 2026 improvement pack, one patch release per repository across all 21 public repositories.

- **`CITATION.cff` added** in the house form settled at D-C1: no `type` field, `version` and `date-released` in lockstep with the README, `license` as the SPDX identifier for this repository's licence, `abstract` taken from this repository's ECOSYSTEM.md role line rather than newly written.
- **How to Cite block** aligned to this release and pointing at `CITATION.cff`.
- **Doctrine citation line added** to the Part of the ecosystem section. This repository restates a doctrine and cited DOCTRINE.md nowhere, which is the Class E2 finding the new guards report.
- **CITATION.cff lockstep lag corrected.** The file carried `version: 1.1.0` and `date-released: 2026-07-12` against a README of `1.4.2`, three minor releases behind. One of the three lags the new Class E3 guard was proved against on the unrepaired tree before this release.
- All other files in this repository are unchanged byte for byte.

## [1.4.2] · 2026-08-17 · Propagation of the v1.4.0 correction

The v1.4.0 correction of substance did not reach every file it contradicted. This release completes it. No new research; nothing here was found by re-reading the product.

- **01-abstract-and-method.md to v1.0.1.** The abstract still read "The legacy app is force-migrated on 3 August 2026". **Struck.** That is the assertion v1.4.0 corrected on 13 August 2026 against the vendor's own migration documentation. A dated correction note is carried at the head of the file and the sentence is recast. This was the study's most exposed instance of the claim: the abstract is the first thing read and the last thing quoted.
- **10-verdict.md to v1.0.1.** The verdict rested part of its population-level claim on "a 3 August 2026 clock the deployer does not control". **Struck and recast.** The deadline pressure the verdict describes is real but differently shaped: the Legacy deprecation cutover is account-specific rather than public, which is worse for the deployer, not better, and the recast sentence says so. The verdict itself is unchanged and is not re-scored.
- **07-regulatory-mapping.md to v1.1.3.** Two defects. Its status line read v1.1.2 · 30 July 2026 although v1.4.0 rewrote the DPIA passage beneath it on 13 August; the v1.4.1 per-file re-dating pass covered 02, 11 and 13 and missed this file. Separately, the file recorded the application date of the new Article 5 prohibitions as **Unknown**. That Unknown is now **resolved**: 2 December 2026, per Article 113, third paragraph, point (a), as amended by Article 1, point (40) of Regulation (EU) 2026/1744. The resolution was obtained on 13 August 2026 and was not carried into this file at the time.

- **README.md and 13-sources.md.** Two further survivals of the same struck claim. The README's rationale for versioning cited "the vendor's migration deadline (3 August 2026)" as a driver; recast to the account-specific Legacy deprecation cutover, which is the actual mechanism and a better argument for versioning, since a private deadline cannot be tracked from outside. `13-sources.md` to v1.1.3: source 15 was annotated as stating a "switchover" on 3 August 2026; the annotation is corrected to what the documentation describes.

- **14-enterprise-question-set.md to v1.0.1.** Found by the new class D supersession check, not by reading. E24 rested on "forced migrations" as the vendor-pressure mechanism, which is the framing v1.4.0 recast at ledger row 8. Recast to deprecation cutovers and the account-specific cutover date, which is the actual and worse mechanism. The question and its three resolutions are otherwise unchanged.

**Method note.** All three defects are propagation failures of corrections already made, not new findings. Two of the three sit in files marked [✓ final] at v1.0.0, which is precisely why they were not re-read. A correction that changes a claim must be applied wherever that claim appears, and "final" is not evidence that a file is clean.

## [1.4.1] · 2026-08-13 · Maintenance sweep

Found by the class A to C maintenance sweep, not by reading.

- **13-sources.md:** the Digital Omnibus entry still recorded Official Journal publication as pending. Replaced with the full citation: Regulation (EU) 2026/1744 of 8 July 2026, OJ L, 2026/1744, 24.7.2026, in force 27 July 2026. This was the last "publication pending" claim in the account.
- **Per-file status lines re-dated** where v1.4.0 changed the file beneath them: 02-timeline to v1.2.0, 11-predictions-register to v1.0.1, 13-sources to v1.1.2. A status line that predates its own body is a currency defect in its own right.

## [1.4.0] · 2026-08-13 · Living update, with a correction of substance

**Correction, not a currency update.** The study recorded a forced migration of the legacy Claude in Slack app to Claude Tag as scheduled for 3 August 2026, following third-party coverage. **That framing is struck.** Read against the vendor's own migration documentation on 13 August 2026 (KST), Claude Tag replaces the earlier app *in place*: the same Slack app and `@Claude` handle remain, no data migrates, pairing the workspace defaults every scope to New, and Legacy is deprecated on an account-specific cutover date after which Legacy scopes stop responding. There was no blanket automatic conversion on 3 August. The study asserted an event that did not occur in the form described.

- **02-timeline.md.** The 3 Aug entry is recast as reported-but-not-borne-out, a verified 13 Aug entry is added setting out the actual mechanism, and a dated correction is recorded in the Corrections block.
- **05-feature-control-ledger.md to v1.1.0.** Rows 1 to 7 and row 9 stand. Row 8 recast: the vendor-paced pressure is real but differently shaped, and worse in one respect, because the deprecation deadline is private to the account rather than public. Two rows added from facts the original ledger did not capture. **Row 10:** the organization-provisioned agent identity improves least privilege and degrades attribution at the same time, since the channel agent starts with no access of its own and code work is authored by the Claude GitHub App rather than the requesting person; the ledger should not net those against each other. **Row 11:** a user who never linked a claude.ai account can task the organizational agent in a channel by default, which is the clearest instance in the study of the channel rather than the user being the security boundary.
- **07-regulatory-mapping.md.** The DPIA sentence is rewritten from "warranted before any deployment at scale" to the Article 35(1) likelihood-of-high-risk trigger, with this deployment's factors named: systematic processing of employee communications, accumulating shared and private-channel memory, standing work through routines and channel watching, an employment context in which objection is not meaningful, third parties discussed but never interacting, and a novel technology in public beta. Records that Article 35(3) is non-exhaustive and Article 35(4) lists apply in addition, and that an undocumented conclusion is indistinguishable from an unconsidered one.
- **11-predictions-register.md.** P6 carries a dated premise note. The prediction is not resolved, withdrawn or re-scored and its 3 February 2027 review date stands; the note records that the referent population is wider than the wording implies and that an Unresolvable outcome is correspondingly more likely.
- Claude Tag remains in public beta and the vendor states behaviour may change before general availability. This study is re-checkable and should be re-run at general availability.

## [1.3.4] · 2026-08-13

License metadata sweep. An `SPDX-License-Identifier: CC-BY-SA-4.0` line and the canonical Creative Commons legal code are now carried inside the existing license file. The filename is unchanged and the human-readable summary is retained above the legal code. This repository stays on ShareAlike as a deliberate openness choice rather than a compatibility requirement.

- The primary audience is automated intake and provenance tooling, which reads the SPDX tag rather than prose. Automated license detection previously reported nothing across all twenty-one repositories in this account.
- No change to the licence in force. The identifier records what was already true.

## [1.3.3] · 2026-07-30 · Open question resolved

Update protocol trigger 3, a regulatory event: substantive review of the adopted text. One open block is closed. No verdict or prediction is revised.

### Changed
- 07-regulatory-mapping.md to v1.1.2. The open block carried at v1.1.1 is resolved and the prior characterization is marked superseded in place rather than deleted. Two corrections and two answers. Correction: the Article 50 marking transitional period is four months, not a cut from six to three; no six-month grace exists anywhere in Regulation (EU) 2026/1744. The 2 December 2026 deadline was correct. Answer one: the 2 August 2026 row is correct as written, because the Article 50(2) transitional period runs to providers only and only for systems placed on the market before 2 August 2026 (Recital 38), so deployer-side Article 50 obligations are unaffected. Answer two: the new Article 5(1)(ba) and (bb) prohibitions do not bite on a governance-and-summarization deployment, the deployer limb at Article 5(1a)(b) requiring use for the purpose of generating the prohibited material. The residual edge case, whether a deployer offering a general-purpose interface falls within that purpose test where its own users generate such material, is flagged for external counsel and recorded as Unknown. The application date of the prohibitions is recorded as Unknown rather than stated, having not been confirmed against the operative amendment to Article 113.
- README version and last-updated line moved in lockstep.

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

---

Final Liability rests with the Human.
