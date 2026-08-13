# The Ungoverned Channel

**A living case study of agentic AI in multiplayer workflows: Claude in Slack and Claude Tag**

**Version:** 1.4.0 · **Status:** [✓ final baseline · living document, updated as new information arises] · **Last updated:** 13 August 2026 (Asia/Seoul)
**Author:** Son-U Michael Paik · **License:** CC BY-SA 4.0

---

## What this is

This repository is a case study in progress. Its subject is the deployment of a persistent, multiplayer AI agent inside an enterprise messaging platform: Anthropic's Claude in Slack, and specifically Claude Tag, launched in beta on 23 June 2026. Its question is whether such a deployment can be governed to the standard that mature AI governance, risk management and compliance frameworks require, and if so at what cost.

The working thesis, stated so it can be attacked:

> **Multiplayer agentic AI is not ungovernable. It is ungoverned by default and governance-degrading by design. Every feature that makes the product marketable is purchased with the removal of a control, and the deployer must rebuild each removed control outside the product, at its own expense, while declining the features that carry the sales pitch.**

The case study exists because this product family is a natural experiment. For the first time at scale, an AI agent holds a shared identity among many human principals, accumulates persistent memory of their work, connects contexts an organization deliberately kept apart and acts on its own initiative. Whatever happens here will happen again, in other platforms, with other vendors. Recording the governance questions now, before the incident reports arrive, is the point.

The questions raised here are important for agentic AI generally, not for one vendor's product. File `14-enterprise-question-set.md` makes this explicit: a jurisdiction-agnostic, product-agnostic set of pre-deployment questions with possible resolutions, usable by any enterprise assessing any persistent multi-user agent. If a reader takes one file from this repository, it should be that one.

## In what capacity

This is personal work. The author writes as a concerned user of these tools and a student of their governance, not as anyone's counsel, auditor or representative: the study is not an audit or assurance engagement, it is not legal advice and it is written on behalf of no organization, client or employer. It is meant to be useful to enterprises deciding whether and how to deploy Claude Tag and, where the observations hold up, to the vendor building it. The tone is critical because the method requires it, not because the intent is adversarial; a case study that cannot find fault cannot find anything.

## Why a living document

A static memo on a beta product is stale on publication. The vendor's migration deadline (3 August 2026), the EU Digital Omnibus (final Council approval 29 June 2026), the security research cadence and the product's own roadmap all move faster than a publication cycle. This repository therefore versions its claims, registers falsifiable predictions with review dates and logs every change. When the analysis is wrong, the record will show where and when.

## Structure

| File | Contents |
|---|---|
| `01-abstract-and-method.md` | Scope, method, authority hierarchy, critique of the v1 memo this study replaces |
| `02-timeline.md` | Verified product timeline, updated as events occur |
| `03-product-architecture.md` | What the product is and what control surfaces it exposes |
| `04-the-multiplayer-problem.md` | Core analysis: attribution, responsibility diffusion, authority ambiguity, consensus laundering |
| `05-feature-control-ledger.md` | The central artifact: each feature mapped to the control it displaces |
| `06-threat-surface.md` | Injection, permission laundering, memory as attack and liability surface |
| `07-regulatory-mapping.md` | EU (post-Omnibus), Korea, US; the classification-drift problem |
| `08-privilege-discovery-legal-process.md` | Privilege, legal hold and discovery, by jurisdiction |
| `09-compensating-controls.md` | Conditions of governability, stated as testable controls |
| `10-verdict.md` | The thesis stress-tested against its best counterarguments |
| `11-predictions-register.md` | Falsifiable predictions with confidence levels and review dates |
| `12-open-questions.md` | Unknowns, held as unknowns, not filled by inference |
| `13-sources.md` | Sources tiered by authority |
| `14-enterprise-question-set.md` | **Jurisdiction-agnostic, product-agnostic pre-deployment questions (E1–E25) with possible resolutions, for any enterprise assessing agentic AI** |
| `CHANGELOG.md` | Every change, logged |

Not every reader needs every file. A board member or approving executive: `05`, `10` and `14`. A deploying risk or compliance function: `09`, `12` and `14`. A security team: `03`, `06` and `09`. Counsel: `07` and `08`. A reader with ten minutes: `05`, then the last sentence of `10`.

## Update protocol

An update is triggered by any of the following, and only by the following:

1. A product change (feature, control, default, pricing tier, migration date) documented by the vendor.
2. Published security research or a publicly reported incident involving this product class.
3. A regulatory event: adopted text, official guidance, enforcement action or formal inquiry.
4. Resolution of any item in `12-open-questions.md`.
5. A prediction in `11-predictions-register.md` reaching its review date.

Each update bumps the version, logs the change and, where a prior claim is revised, marks the prior claim superseded rather than deleting it. Errors stay visible.

## Provenance and bias disclosure

This case study was drafted with Claude, an Anthropic model, analyzing an Anthropic product. That is a structural conflict and it is not waved away. Mitigations: the analysis privileges independent security research and adversarial framings over vendor statements; vendor self-reports are labeled as such and given no evidentiary weight; and the predictions register creates accountability the drafting process cannot retract. Readers should nonetheless apply independent judgment.

## Corrections and contributions

This study is written to be corrected. Factual errors, superseding sources and contributed enterprise questions are welcome through GitHub Issues; `CONTRIBUTING.md` sets out what is accepted and how changes are logged. Every accepted change is versioned and changelogged, and any claim it supersedes is marked as superseded rather than silently replaced. Citation metadata is in `CITATION.cff`.

Several of the open questions in `12-open-questions.md` can only ever be resolved by vendor documentation. The study asks nothing of anyone on that front: it updates when the public record does. Anyone closer to the facts than the public record, at the vendor or anywhere else, is welcome to point out where the study is wrong, formally or informally. Disagreement is equally useful: counterarguments that survive contact improve `10-verdict.md`, and vendor tooling that breaks a ledger row is exactly what the predictions register exists to record. Corrections are attributed only with the contributor's consent, and nothing shared informally is quoted or cited without it; the goal is a more accurate document, not a record of who said what.

## Doctrinal frame

The analysis applies three doctrines developed in the author's broader work: **Slow AI** (governed, explainable, auditable AI adopted at the deployer's pace, not the vendor's), **Final Liability** (ultimate accountability for an AI-assisted outcome attaches to a named human) and **Informed Intent** (a named human authorizes a specified task, with understood tolerances, before the system acts). The case study tests whether this product family can satisfy them. Readers who reject the doctrines can still use the feature-control ledger and the predictions register, which stand on their own.

## Part of the ecosystem

This case study is the field-study layer of a larger body of AI governance, risk management and compliance work. The canonical map of all repositories is [ECOSYSTEM.md](https://github.com/rolldabones/rolldabones/blob/main/ECOSYSTEM.md) in the profile repository.

Nearest neighbors:
- [ai-governance-for-boards](https://github.com/rolldabones/ai-governance-for-boards): the jurisdiction guides and board question bank behind file 07 and the approving-executive audience of the enterprise question set
- [AI-Impact-Assessment-Tool](https://github.com/rolldabones/AI-Impact-Assessment-Tool): the pre-deployment assessment gate whose absence this case study documents in the wild
- [slow-ai-kitchen](https://github.com/rolldabones/slow-ai-kitchen): the method for adopting AI at the deployer's pace rather than the vendor's, which the working thesis puts to the test

---

Final Liability rests with the Human.
