# E7G-T v0.9 Public Landing Page Draft

**Document type:** public-facing landing page draft  
**Version:** v0.9 RC1-aligned  
**Date:** 2026-07-01  
**Status:** draft for website / Notion / GitHub README / reviewer hand-off  
**Public posture:** modelling language, not established mathematics or physics

---

# E7G-T

## A Geometry-First Modelling Language for Seeing What Representations Hide

E7G-T is a practical modelling language for inspecting representations before relying on them.

It helps users ask:

> What is this answer, chart, translation, proof text, model, summary, or dashboard a projection of — and what does it lose?

E7G-T is built around a simple discipline:

- name the entity;
- name the boundary;
- identify the projection;
- record what is preserved;
- record what is lost;
- declare the bridge mode;
- limit the claim strength;
- state the next responsible move.

---

## The Short Definition

> E7G-T is a geometry-first modelling language and practical calculus for making projection, loss, reconstruction, bridge mode, and admissible use visible.

Expanded:

> E7G-T helps people inspect representations before relying on them. It asks what a chart, AI answer, proof text, translation, model, legal summary, or dashboard preserves, what it loses, what source it points to, what claim strength it can support, and what the next responsible move should be.

---

## What Problem Does It Solve?

Modern work depends on representations:

- AI answers;
- charts;
- dashboards;
- summaries;
- translations;
- legal and administrative notes;
- proof sketches;
- scientific models;
- code outputs;
- interface states;
- reports.

These representations are useful because they compress reality.

They are dangerous because compression hides structure.

A chart is not the business.  
An AI answer is not the source.  
A translation is not the original document.  
A proof sketch is not proof.  
A legal summary is not the authority.  
A model is not reality.

E7G-T gives users a structured way to notice these differences before making decisions.

---

## What E7G-T Is Not

E7G-T is not established mathematics.

It is not empirical physics.

It is not a proof system.

It is not a Theory of Everything.

It is not a replacement for legal, medical, financial, engineering, translation, statistical, scientific, or formal-methods expertise.

It is a modelling and review discipline.

Its role is to help users avoid overreading representations.

---

## The Core Idea

Every representation is a view.

Every view preserves something.

Every view loses something.

Every responsible use depends on knowing the difference.

E7G-T calls this **projection-loss discipline**.

---

## Practical Examples

### AI answers

An AI answer may be useful, fluent, and well structured.

But it is not automatically evidence.

E7G-T asks:

- What source did the answer use?
- Is the source visible?
- Is the source current?
- What claims need verification?
- Is this a draft, summary, hypothesis, or verified answer?

Blocked overread:

> AI answer is not the source.

---

### Business dashboards

A dashboard may show that sales dropped.

But it does not automatically show why.

E7G-T asks:

- What metric is shown?
- What source produced it?
- What time window is active?
- What causes are hidden?
- What decision can this chart actually support?

Blocked overread:

> Chart movement is not causal diagnosis.

---

### Translation

A translation may be fluent.

But fluency is not the same as source preservation.

E7G-T asks:

- Are names preserved?
- Are dates preserved?
- Are numbers preserved?
- Are stamps, seals, signatures, and handwritten notes represented?
- Is uncertainty marked?
- Does the translation preserve the documentary function?

Blocked overread:

> Translation is not source identity.

---

### Proof assistants

A proof assistant may accept a proof script.

But accepted status and human explanation are not identical.

E7G-T asks:

- What is the theorem statement?
- What assumptions are active?
- What proof state is visible?
- What tactic transformed the state?
- What obligations were discharged?
- Is the proof accepted, explained, both, or neither?

Blocked overread:

> Proof script is not the whole proof object.

---

### Legal and administrative summaries

A legal or administrative summary may be helpful.

But it is not the authority.

E7G-T asks:

- What law, guidance, form, letter, or decision is the source?
- Are the facts current and complete?
- Are the documents sufficient?
- What procedure applies?
- Is this orientation, checklist, source-linked summary, reviewed memo, or authority decision?

Blocked overread:

> Summary is not authority.

---

## The E7G-T Review Pattern

Use this pattern for any representation:

```text
Entity:
Context:
Boundary:
Source / candidate source:
Projection:
Preserved:
Lost:
Distortion risk:
Bridge mode:
Claim strength:
Admissible use:
Non-admissible use:
Next move:
Stop condition:
```

A compact version:

```text
E7-OneLine: X is treated as [order/role] under [context]; admissible move: [next move]; blocked overread: [one phrase].
```

Example:

```text
E7-OneLine: An AI answer is treated as a D2/D7 textual projection under user-query context; admissible move: verify source and bridge mode; blocked overread: AI answer is not the source.
```

---

## Current v0.9 Artifact Set

The current v0.9 release candidate includes:

### Kernel

- **E7G-T Kernel v0.9 RC1 — Public Reference Specification**

The compact rule-set defining orders, temporal regimes, primitive moves, bridge modes, claim strength, Proof-of-Path, Reality Bridge, failure modes, and public-use cautions.

### Application Atlas

- **APP-001 — AI Output as Projection**
- **APP-002 — Translation as Invariant-Preserving Projection**
- **APP-003 — Legal / Administrative Summary as Projection**

These show how the kernel works in specific domains.

### Practical Guide

- **PG-001 — The Chart Is Not the Business**
- **PG-001 Worksheet — Dashboard Projection-Loss Review**
- **PG-002 — The AI Answer Is Not the Source**
- **PG-002 Worksheet — AI Answer Source-Return Review**

These make the framework accessible to ordinary users.

### Proof-of-Path

- **POP-001 — Proof Assistant Session as Accountable Path**
- **POP-002 — Tiny Theorem Worked Example**

These apply E7G-T to proof-assistant workflows and formal-status tracking.

### Pilot Protocols

- **PILOT-001 — AI Output Review Protocol**
- **PILOT-002 — Translation QA Protocol**

These test whether E7G-T actually improves review quality.

---

## Who Is E7G-T For?

E7G-T may be useful for:

- AI users who need source-return discipline;
- translators and translation QA reviewers;
- business operators reading dashboards;
- analysts reviewing summaries and reports;
- educators teaching reasoning and modelling;
- software developers reviewing traces, tests, and outputs;
- proof-assistant learners;
- legal/admin support teams preparing source-linked checklists;
- researchers working across analogy, formalisation, and evidence boundaries.

---

## What Can You Test First?

The easiest first tests are:

### 1. AI-answer review

Take a real AI answer.

Ask:

- What claims does it make?
- Which claims are sourced?
- Which claims are current-sensitive?
- Which claims need expert review?
- What is the strongest admissible use?

Use:

- APP-001
- PG-002 Worksheet
- PILOT-001

---

### 2. Translation QA

Take a real source document and translation.

Ask:

- Are names preserved?
- Are dates preserved?
- Are numbers preserved?
- Are stamps, signatures, seals, and notes represented?
- Is uncertainty marked?
- Is the translation fit for its declared purpose?

Use:

- APP-002
- PILOT-002

---

### 3. Dashboard review

Take a real chart.

Ask:

- What does the chart preserve?
- What does it lose?
- What causal claims are unsupported?
- What source return is needed?
- What decision tier is admissible?

Use:

- PG-001
- PG-001 Worksheet

---

## How to Evaluate E7G-T

Do not evaluate E7G-T by asking:

> Has it solved reality?

Ask instead:

> Does it help users avoid overreading representations?

More specific evaluation questions:

1. Does it make hidden assumptions visible?
2. Does it separate source from view?
3. Does it catch projection loss?
4. Does it prevent claim-strength inflation?
5. Does it produce clearer next moves?
6. Does it improve review quality without excessive overhead?

---

## Current Status

E7G-T v0.9 is a release-candidate modelling framework.

It is ready for:

- small pilot tests;
- collaborator review;
- practical worksheet use;
- public positioning review;
- application refinement.

It is not ready for:

- claims of established mathematics;
- claims of new physics;
- empirical claims;
- replacement of domain expertise;
- v1.0 public stability.

---

## The v1.0 Gate

E7G-T should not move to v1.0 until:

- the kernel terms are stable;
- notation is stable;
- bridge modes are consistently enforced;
- at least three Application Atlas entries are tested;
- at least two worksheets are tested on real examples;
- at least one Proof-of-Path worked example is checked in a real proof assistant or clearly labelled illustrative;
- public language is simplified;
- overclaim risks are reduced.

---

## Suggested Reviewer Task

Give a reviewer three files first:

1. **E7G-T Kernel v0.9 RC1**
2. **PG-002 Worksheet — AI Answer Source-Return Review**
3. **PILOT-001 — AI Output Review Protocol**

Ask the reviewer to test the worksheet on five real AI answers and report:

- what risks were caught;
- what risks were missed;
- which fields were useful;
- which fields were too heavy;
- whether E7G-T improved the next responsible move.

---

## Closing Line

E7G-T does not ask you to distrust every representation.

It asks you to see the representation as a representation.

The source is richer than the view.

The view preserves.

The view loses.

Reliance begins when you know the difference.
