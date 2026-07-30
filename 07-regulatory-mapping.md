# 07 · Regulatory Mapping

**Status:** [✓ final] · v1.1.1 · 30 July 2026 · Verified against the Digital Omnibus as adopted and published, Regulation (EU) 2026/1744, and against Colorado SB 26-189 as signed 14 May 2026

⚠ This file maps exposure; it is not advice. Jurisdiction-specific questions flagged below require external counsel in the relevant jurisdiction.

## A. European Union (post-Omnibus)

The Digital Omnibus on AI was adopted as Regulation (EU) 2026/1744 of 8 July 2026, published in the Official Journal on 24 July 2026 (OJ L, 2026/1744, 24.7.2026) and in force since 27 July 2026, the third day after publication. The deferrals below are binding law. The AI Act's general application date of 2 August 2026 is unchanged. The operative timeline for a Slack-agent deployer:

> **Superseded (v1.1.0, 12 July 2026).** This section stated that the Omnibus had received Parliament endorsement and Council approval, with Official Journal publication expected in July 2026 and entry into force three days after publication. That was accurate as written and the expectation held: publication landed on 24 July 2026 and entry into force followed on 27 July 2026. The claim is superseded only in that the deferrals are no longer adopted text awaiting publication.

> **Open, pending substantive review.** The published text does more than defer. The Article 50 marking grace period is cut from six months to three, with a 2 December 2026 deadline, and two new Article 5 prohibitions are added (non-consensual intimate material and child sexual abuse material), both applying from 2 December 2026. Whether either bears on a Slack-agent deployer, and in particular whether the 2 August 2026 row below remains correct in stating that deployer-side Article 50 obligations are unaffected by the Omnibus, is not resolved in this release. It is scoped to the substantive pass that also covers the two appendix instruments in the book repository. ⚠

| Date | Obligation | Relevance to this deployment |
|---|---|---|
| Since 2 Feb 2025 | Art 4 AI literacy; Art 5 prohibited practices | Deployers must ensure staff AI literacy. Directly relevant: a workforce interacting casually with an agent in Slack is the literacy obligation's hardest case |
| 2 Aug 2026 | Art 50 transparency obligations (deployer-side unaffected by the Omnibus) | Users must be informed they are interacting with an AI system. Inside the channel, the @Claude handle arguably discharges this. The live question is downstream: agent-generated text copied out of Slack into external communications carries no marker |
| 2 Dec 2026 | End of the Art 50(2) marking grace period for systems on the market before 2 Aug 2026 (systems newly placed on the market comply from 2 Aug 2026); new Art 5 NCII/CSAM prohibition | Provider-side; deployer relevance limited |
| 2 Dec 2027 | Annex III high-risk obligations (deferred from 2 Aug 2026) | See classification drift, below |
| 2 Aug 2028 | Annex I embedded high-risk obligations | Not relevant to this deployment class |

**The classification-drift problem.** A general-purpose assistant in Slack is not, as deployed, an Annex III high-risk system. But channels are where work actually happens, and some of that work is Annex III work: recruitment screening in an HR channel, worker performance evaluation, credit decisions in a lending team's channel. Nothing in the product classifies use; the same agent that summarizes standups can be asked to rank candidates. The exposure is not present breach but unclassified migration into high-risk use, invisible precisely because no deployment decision was ever taken. The deferral to December 2027 is time to build the classification mechanism, not permission to skip it. The Omnibus's grandfathering logic (systems placed on the market before the deadline avoid full obligations until substantially modified) adds a perverse incentive worth naming: rapid pre-deadline deployment is rewarded, which is the opposite of **Slow AI**.

**GDPR.** Channel memory is a processing operation over personal data of employees and third parties mentioned in channels. Friction points: minimization (memory accumulates by design), erasure (an Art 17 request against a non-enumerable memory is difficult to discharge and to evidence), and transparency (employees whose messages feed the memory are data subjects owed information). A DPIA is warranted before any deployment at scale; the Omnibus's parallel GDPR amendments do not remove this. ⚠

## B. Korea

The AI Framework Act (framework act on the development of artificial intelligence and establishment of trust) took effect 22 January 2026, with the Ministry of Science and ICT as principal enforcer. Deployer-relevant elements: heightened duties for high-impact AI (domains affecting life, safety and fundamental rights), transparency obligations for generative AI including notification that content is AI-generated, and a domestic-representative requirement for foreign providers above thresholds. The mapping question mirrors the EU's: a Slack agent is not high-impact as deployed, but channel use can drift into high-impact domains without a classification event. Korean subsidiaries of multinationals deploying via global Slack instances should confirm whether MSIT guidance treats the local use as a domestic deployment. Statutory fines are modest (administrative fines up to KRW 30 million) but enforcement posture in the Act's first years is being set now, and PIPC's parallel jurisdiction over the personal-data dimension of channel memory is the sharper exposure. ⚠

## C. United States

No horizontal federal AI statute governs this deployment. The exposure is composed of existing law hitting new facts: sectoral regulators (FINRA and SEC books-and-records and supervision duties are acutely relevant, since channel-agent output in a broker-dealer's Slack is likely a record subject to retention and supervision), state laws (Colorado, the bellwether, repealed and replaced its 2024 AI Act before it ever took effect: SB 26-189, signed 14 May 2026 and effective 1 January 2027, replaces the duty-of-care, risk-management and impact-assessment framework with disclosure duties around automated decision-making technology that materially influences consequential decisions, so drifted HR uses remain captured but through notice obligations rather than governance mandates, and the drift determination still requires knowing what channels actually do; Illinois BIPA-style statutes if any biometric-adjacent processing occurs), FTC Section 5 for deceptive or unfair practices, and common-law negligence with the internal-accountability collapse of `04` degrading the defensibility of any reasonable-supervision defense. The most immediate US exposure is not an AI statute at all: it is discovery and records law meeting a non-enumerable vendor-held memory (`08`).

## D. Cross-cutting observation

All three regimes share an assumption the product breaks: that a deployment is a discrete, classifiable event undertaken by an identifiable deployer for a specified purpose. A multiplayer agent in a channel is a continuous, purpose-unspecified deployment whose actual uses are determined daily by whoever is in the room. Regulatory mapping therefore cannot be done once at procurement; it must be an ongoing classification function watching what channels actually do. That function does not exist in any framework's standard control catalogue yet. It should.

Final Liability rests with the Human.
