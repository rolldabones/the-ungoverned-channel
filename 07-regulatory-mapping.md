# 07 · Regulatory Mapping

**Status:** [✓ final] · v1.0.0 · 11 July 2026 · Verified against the Digital Omnibus as approved by the Council on 29 June 2026

⚠ This file maps exposure; it is not advice. Jurisdiction-specific questions flagged below require external counsel in the relevant jurisdiction.

## A. European Union (post-Omnibus)

The Digital Omnibus on AI received the European Parliament's endorsement on 16 June 2026 and the Council's final approval on 29 June 2026, with publication in the Official Journal expected in July 2026 and entry into force three days after publication. The operative timeline for a Slack-agent deployer:

| Date | Obligation | Relevance to this deployment |
|---|---|---|
| Since 2 Feb 2025 | Art 4 AI literacy; Art 5 prohibited practices | Deployers must ensure staff AI literacy. Directly relevant: a workforce interacting casually with an agent in Slack is the literacy obligation's hardest case |
| 2 Aug 2026 | Art 50 transparency obligations (deployer-side unaffected by the Omnibus) | Users must be informed they are interacting with an AI system. Inside the channel, the @Claude handle arguably discharges this. The live question is downstream: agent-generated text copied out of Slack into external communications carries no marker |
| 2 Dec 2026 | Art 50(2) provider watermarking (deferred); new Art 5 NCII/CSAM prohibition | Provider-side; deployer relevance limited |
| 2 Dec 2027 | Annex III high-risk obligations (deferred from 2 Aug 2026) | See classification drift, below |
| 2 Aug 2028 | Annex I embedded high-risk obligations | Not relevant to this deployment class |

**The classification-drift problem.** A general-purpose assistant in Slack is not, as deployed, an Annex III high-risk system. But channels are where work actually happens, and some of that work is Annex III work: recruitment screening in an HR channel, worker performance evaluation, credit decisions in a lending team's channel. Nothing in the product classifies use; the same agent that summarizes standups can be asked to rank candidates. The exposure is not present breach but unclassified migration into high-risk use, invisible precisely because no deployment decision was ever taken. The deferral to December 2027 is time to build the classification mechanism, not permission to skip it. The Omnibus's grandfathering logic (systems placed on the market before the deadline avoid full obligations until substantially modified) adds a perverse incentive worth naming: rapid pre-deadline deployment is rewarded, which is the opposite of **Slow AI**.

**GDPR.** Channel memory is a processing operation over personal data of employees and third parties mentioned in channels. Friction points: minimization (memory accumulates by design), erasure (an Art 17 request against a non-enumerable memory is difficult to discharge and to evidence), and transparency (employees whose messages feed the memory are data subjects owed information). A DPIA is warranted before any deployment at scale; the Omnibus's parallel GDPR amendments do not remove this. ⚠

## B. Korea

The AI Framework Act (framework act on the development of artificial intelligence and establishment of trust) took effect 22 January 2026, with the Ministry of Science and ICT as principal enforcer. Deployer-relevant elements: heightened duties for high-impact AI (domains affecting life, safety and fundamental rights), transparency obligations for generative AI including notification that content is AI-generated, and a domestic-representative requirement for foreign providers above thresholds. The mapping question mirrors the EU's: a Slack agent is not high-impact as deployed, but channel use can drift into high-impact domains without a classification event. Korean subsidiaries of multinationals deploying via global Slack instances should confirm whether MSIT guidance treats the local use as a domestic deployment. Statutory fines are modest (administrative fines up to KRW 30 million) but enforcement posture in the Act's first years is being set now, and PIPC's parallel jurisdiction over the personal-data dimension of channel memory is the sharper exposure. ⚠

## C. United States

No horizontal federal AI statute governs this deployment. The exposure is composed of existing law hitting new facts: sectoral regulators (FINRA and SEC books-and-records and supervision duties are acutely relevant, since channel-agent output in a broker-dealer's Slack is likely a record subject to retention and supervision), state laws (Colorado's AI Act, as amended and delayed to mid-2026, targets consequential decisions and would capture drifted HR uses; Illinois BIPA-style statutes if any biometric-adjacent processing occurs), FTC Section 5 for deceptive or unfair practices, and common-law negligence with the internal-accountability collapse of `04` degrading the defensibility of any reasonable-supervision defense. The most immediate US exposure is not an AI statute at all: it is discovery and records law meeting a non-enumerable vendor-held memory (`08`).

## D. Cross-cutting observation

All three regimes share an assumption the product breaks: that a deployment is a discrete, classifiable event undertaken by an identifiable deployer for a specified purpose. A multiplayer agent in a channel is a continuous, purpose-unspecified deployment whose actual uses are determined daily by whoever is in the room. Regulatory mapping therefore cannot be done once at procurement; it must be an ongoing classification function watching what channels actually do. That function does not exist in any framework's standard control catalogue yet. It should.

Final Liability rests with the Human.
