# The Ungoverned Channel

**A living case study of agentic AI in multiplayer workflows: Claude in Slack and Claude Tag**

**Version:** 1.0.0 · **Status:** [✓ final baseline · living document, updated as new information arises] · **Last updated:** 11 July 2026 (Asia/Seoul)
**Author:** Son-U Michael Paik · **License:** CC BY-SA 4.0

---

## What this is

This repository is a case study in progress. Its subject is the deployment of a persistent, multiplayer AI agent inside an enterprise messaging platform: Anthropic's Claude in Slack, and specifically Claude Tag, launched in beta on 23 June 2026. Its question is whether such a deployment can be governed to the standard that mature AI governance, risk management and compliance frameworks require, and if so at what cost.

The working thesis, stated so it can be attacked:

> **Multiplayer agentic AI is not ungovernable. It is ungoverned by default and governance-degrading by design. Every feature that makes the product marketable is purchased with the removal of a control, and the deployer must rebuild each removed control outside the product, at its own expense, while declining the features that carry the sales pitch.**

The case study exists because this product family is a natural experiment. For the first time at scale, an AI agent holds a shared identity among many human principals, accumulates persistent memory of their work, connects contexts an organization deliberately kept apart and acts on its own initiative. Whatever happens here will happen again, in other platforms, with other vendors. Recording the governance questions now, before the incident reports arrive, is the point.

The questions raised here are important for agentic AI generally, not for one vendor's product. File `14-enterprise-question-set.md` makes this explicit: a jurisdiction-agnostic, product-agnostic set of pre-deployment questions with possible resolutions, usable by any enterprise assessing any persistent multi-user agent. If a reader takes one file from this repository, it should be that one.

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

## Doctrinal frame

The analysis applies three doctrines developed in the author's broader work: **Slow AI** (governed, explainable, auditable AI adopted at the deployer's pace, not the vendor's), **Final Liability** (ultimate accountability for an AI-assisted outcome attaches to a named human) and **Informed Intent** (a named human authorizes a specified task, with understood tolerances, before the system acts). The case study tests whether this product family can satisfy them. Readers who reject the doctrines can still use the feature-control ledger and the predictions register, which stand on their own.

---

Final Liability rests with the Human.
