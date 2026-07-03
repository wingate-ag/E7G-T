# E7G-T Application Atlas — Entry 001

# AI Output as Projection

**Atlas ID:** APP-001  
**Kernel compatibility:** E7G-T v0.9 draft  
**Status:** pilot-ready application entry  
**Date:** 2026-06-29  
**Bridge mode:** operational / modelling; empirical claims require source verification  
**Primary use:** AI-output review, claim linting, source-return discipline, hallucination-risk reduction

---

## 1. Entry Purpose

This Application Atlas entry applies E7G-T v0.9 to AI-generated answers.

The basic claim is simple:

> An AI answer should be treated as a projected textual view, not as direct evidence, direct source access, formal proof, or empirical confirmation.

This entry gives a reusable method for inspecting AI outputs before relying on them.

It is designed for:

- everyday ChatGPT / LLM use;
- research assistance;
- legal or administrative drafting;
- translation and QA support;
- business analysis;
- software reasoning;
- proof-assistant support;
- speculative or philosophical modelling;
- source-backed writing.

---

## 2. Entity of Concern

**Entity:** AI-generated answer.

The entity of concern is not “the truth of the matter” directly. It is the **answer-as-output**: a visible text, code block, summary, explanation, recommendation, translation, proof sketch, or reasoning artefact produced by an AI system.

E7G-T treats this output as a projection.

---

## 3. Source / View Distinction

| Layer | Description |
|---|---|
| **Source domain** | User prompt, training distribution, retrieved sources if browsing/search is used, uploaded documents, tool outputs, model-internal pattern generation, conversation context, and any explicit files or data available. |
| **View** | The generated answer visible to the user. |
| **Projection context** | The user request, conversation state, model behaviour, system constraints, available tools, retrieval status, safety rules, and output format. |
| **Risk** | The view may appear coherent even when the source is absent, weak, ambiguous, outdated, or unverified. |

### Core E7G-T repair

Do not ask first:

> “Does this sound right?”

Ask first:

> “What kind of projection is this, and what can it responsibly support?”

---

## 4. Placement

### Compact placement

```text
AIAnswer : D2/D7 @ TR1 / UserQueryContext
```

### Meaning

The AI answer is treated as:

- **D2** because it appears as a surface-level text/interface output;
- **D7** because it is shaped by context, prompt, system rules, user intent, and admissible-use constraints;
- **TR1** because it is produced as a local conversational sequence;
- **UserQueryContext** because its meaning and usefulness depend on the user’s request.

### Expanded placement

```text
SourceSet? : D4/D5/D6/D7 @ TR0-TR6 / ModelAndRetrievalContext
   --π_UserQuery^{?→2}-->
AIAnswer : D2/D7 @ TR1 / UserQueryContext
[preserves: selected linguistic, semantic, procedural, or source-derived structure;
 loses: full source trace, uncertainty, rival explanations, hidden assumptions, training provenance;
 use: provisional answer, draft, explanation, prompt for verification]
```

The source set is marked with `?` because the user often cannot fully inspect the internal source basis of the generated answer.

---

## 5. Projection Account

An AI answer may preserve:

- relevant wording from uploaded or retrieved sources;
- general domain patterns;
- structural relationships;
- reasoning steps;
- summary-level meaning;
- user-provided constraints;
- formatting instructions;
- plausible next actions;
- code or template structure;
- translation equivalents;
- proof strategy fragments.

An AI answer may lose:

- exact source provenance;
- uncertainty level;
- edge cases;
- dissenting sources;
- legal or regulatory currency;
- assumptions hidden in the prompt;
- failed reasoning paths;
- model confidence calibration;
- source limitations;
- temporal freshness;
- formal validity;
- empirical support.

An AI answer may distort:

- source emphasis;
- causal strength;
- legal certainty;
- scientific consensus;
- numerical precision;
- proof status;
- translation nuance;
- user intent;
- domain boundaries;
- claim strength.

---

## 6. Preservation / Loss Ledger

| Question | Review instruction |
|---|---|
| What is preserved? | Identify what the answer reliably carries from the prompt, source, tool output, or known domain structure. |
| What is lost? | Identify what is hidden, compressed, absent, uncertain, or not independently checked. |
| What is distorted? | Identify whether the answer upgrades weak support into confident wording. |
| What needs source return? | Identify claims requiring citation, file reference, empirical data, legal authority, formal proof, or expert review. |
| What use is admissible? | Decide whether the output can be used as draft, summary, suggestion, proof sketch, decision support, or verified result. |

---

## 7. Reconstruction Status

Most AI answers should be treated as **not fully reconstructive**.

### Default reconstruction status

```text
ρ_C(AIAnswer) ⇒ {possible source patterns, prompt constraints, retrieved snippets, model-internal generalisations}
```

This means the answer may constrain possible sources, but it does not automatically reconstruct them.

### Safe wording

The answer is **compatible with** certain source structures.

### Unsafe wording

The answer **proves**, **confirms**, **shows**, or **establishes** the source unless a suitable bridge, citation, formal proof, or empirical check is present.

---

## 8. Bridge Mode

AI outputs can appear under different bridge modes.

| Bridge mode | Use | Example |
|---|---|---|
| **none** | No cross-domain claim is made. | “Rewrite this paragraph.” |
| **contemplative-what-if** | Reflective or fictional exploration. | “Imagine time as projection.” |
| **philosophical-interpretation** | Conceptual interpretation without empirical force. | “Interpret this metaphor.” |
| **formal-analogy** | Structural analogy between domains. | “Treat measurement as projection.” |
| **formal-compatibility** | Mapping toward a formal substrate. | “Express this as a typed schema.” |
| **empirical-testable** | Claims requiring observation/evidence. | “This medicine causes X.” |
| **operational** | Workflow, linting, QA, or decision-support use. | “Check this contract summary against the source.” |

### Bridge rule

An AI answer does not raise bridge mode by sounding confident.

---

## 9. Claim-Strength Lint

When reviewing an AI answer, classify each important claim.

| Claim type | Required support |
|---|---|
| Definition | Stable domain source or accepted convention. |
| Summary | Source text or declared source scope. |
| Translation | Source text, purpose, terminology, QA. |
| Legal/administrative claim | Current legal source or qualified review. |
| Medical claim | Current medical source and professional caution. |
| Scientific claim | Reliable source, date, evidence status. |
| Mathematical proof claim | Formal or rigorous proof substrate. |
| Software claim | Code, tests, specification, runtime context. |
| Business claim | Data source, metric definition, assumptions. |
| Speculative bridge | Declared bridge mode and stop condition. |

### Upgrade test

Before relying on the AI answer, ask:

> What would have to be true for this claim strength to be justified?

---

## 10. Failure Modes

AI outputs are especially vulnerable to the following E7G-T failure modes:

### 10.1 Fluency mistaken for evidence

The answer is well-written, but source support is absent or weak.

**Blocked overread:** fluency is not evidence.

### 10.2 Summary mistaken for source

The answer summarises a document, but the summary is treated as the document itself.

**Blocked overread:** summary is not source identity.

### 10.3 Analogy mistaken for proof

The answer gives a useful analogy, but the user treats it as formal or empirical support.

**Blocked overread:** analogy is not proof.

### 10.4 Outdated knowledge mistaken for current fact

The answer relies on stale knowledge where current status matters.

**Blocked overread:** memory is not current verification.

### 10.5 Draft mistaken for final

The answer provides a useful draft, but it is treated as deliverable without review.

**Blocked overread:** draft is not QA.

### 10.6 Proof sketch mistaken for proof

The answer outlines a proof strategy but does not discharge formal obligations.

**Blocked overread:** proof sketch is not proof object.

### 10.7 Tool output mistaken for interpretation

A tool returns data, but interpretation still requires context and domain judgment.

**Blocked overread:** retrieved data is not completed reasoning.

### 10.8 Context drift

The AI answer silently changes the user’s boundary, question, or assumptions.

**Blocked overread:** changed boundary means changed claim.

---

## 11. OneLine Template

```text
E7-OneLine: [AI output] is treated as a D2/D7 textual projection under [prompt/source/tool context]; admissible move: [verify / downgrade / source-return / use as draft / stop]; blocked overread: [fluency is not evidence / summary is not source / analogy is not proof / draft is not final].
```

### Generic OneLine

```text
E7-OneLine: An AI answer is treated as a D2/D7 textual projection under user-query context; admissible move: verify source and bridge mode; blocked overread: fluency is not evidence.
```

---

## 12. MiniCard Template

```yaml
id: APP-001-AI-output-review
entity: AI-generated answer
plainMeaning: Visible text produced by an AI system in response to a user prompt.
placement: AIAnswer : D2/D7 @ TR1 / UserQueryContext
boundary:
  includes:
    - visible answer
    - user prompt
    - declared sources or tools
    - stated assumptions
  excludes:
    - uninspectable model internals
    - unstated source provenance
    - unverified external reality
projectionAccount:
  source: prompt + conversation + available tools + retrieved/uploaded sources if any + model-generated patterns
  view: visible answer
preserved:
  - selected semantic structure
  - formatting and task constraints
  - retrieved or uploaded source content where explicitly grounded
lost:
  - full provenance
  - uncertainty
  - rival explanations
  - hidden assumptions
  - real-time verification unless tools were used
distortionRisk:
  - overconfidence
  - source blending
  - outdated facts
  - unsupported causal or legal claims
reconstructionStatus: underdetermined unless source-linked
bridgeMode: depends on claim; default operational/modelling
admissibleUse:
  - draft
  - explanation
  - checklist
  - hypothesis
  - source-return prompt
nonAdmissibleUse:
  - final factual reliance without verification
  - legal/medical/financial reliance without expert/current source
  - formal proof without substrate
nextMove: classify claims and verify high-risk statements
blockedOverread: AI fluency is not evidence
```

---

## 13. FullCard Template

```yaml
id:
claim:
entityOfConcern: AI-generated answer
userPurpose:
sourceStatus:
  promptProvided:
  filesProvided:
  toolsUsed:
  citationsProvided:
  currentWebNeeded:
placement:
boundary:
temporalRegime:
projectionPath:
preservedStructure:
lostStructure:
distortionRisk:
claimTypes:
  - factual
  - interpretive
  - formal
  - empirical
  - legal
  - medical
  - financial
  - speculative
  - operational
bridgeMode:
reconstructionStatus:
requiredVerification:
weakestLink:
admissibleUse:
nonAdmissibleUse:
stopCondition:
nextMove:
reviewerNotes:
```

---

## 14. AI Output Linter

### 14.1 Fast linter

Ask:

1. What is the answer claiming?
2. What is the entity of concern?
3. Is the output a source, summary, draft, proof sketch, interpretation, or recommendation?
4. What source or tool output supports it?
5. What is preserved from the source?
6. What is lost or hidden?
7. What bridge mode is active?
8. What claims require current verification?
9. What claims require domain expertise?
10. What overread must be blocked?
11. What is the next admissible move?

### 14.2 Claim labels

Use these labels inline when reviewing AI answers:

```text
[SOURCE-LINKED]
[UNSOURCED]
[DRAFT-ONLY]
[INTERPRETATION]
[FORMAL-ANALOGY]
[NEEDS-CURRENT-CHECK]
[NEEDS-DOMAIN-EXPERT]
[PROOF-SKETCH]
[EMPIRICAL-CLAIM]
[STOP]
```

### 14.3 Output status labels

| Label | Meaning |
|---|---|
| **Safe as draft** | Can be used as editable text, not final authority. |
| **Safe as summary with source return** | Usable if checked against source. |
| **Safe as analogy** | Useful for thinking but not proof. |
| **Needs citation** | Source-backed claim required. |
| **Needs current check** | Fact may have changed. |
| **Needs expert review** | Domain risk is high. |
| **Needs formal substrate** | Mathematical/proof/program claim requires formal check. |
| **Stop** | Reliance is not justified. |

---

## 15. Worked Examples

### 15.1 Current factual claim

AI answer:

> “The CEO of Company X is Person Y.”

E7G-T review:

```text
Entity: AI factual claim
Placement: Claim : D2 @ TR1 / UserQueryContext
Bridge mode: empirical/current factual
Risk: current role may have changed
Required move: current source verification
Blocked overread: model memory is not current authority
Stop condition: no current source
```

Admissible use:

Use as a prompt to verify, not as final fact.

---

### 15.2 Legal or immigration claim

AI answer:

> “You can apply for this residence permit with income level X.”

E7G-T review:

```text
Entity: legal/administrative claim
Bridge mode: empirical/legal-operational
Required substrate: current law, official guidance, competent legal/administrative review
Risk: outdated threshold, jurisdictional exception, family composition mismatch
Blocked overread: plausible legal summary is not legal authority
```

Admissible use:

Use as orientation only until current official sources and/or expert review confirm it.

---

### 15.3 Translation QA claim

AI answer:

> “This translation is accurate.”

E7G-T review:

```text
Entity: translation QA judgement
Placement: TranslationReview : D2/D7 @ TR1 / PurposeContext
Required boundary: source text, target text, intended recipient, legal/administrative purpose
Preserved: must identify specific invariants
Lost: cannot be assumed absent
Blocked overread: fluent target text is not adequacy
```

Admissible use:

Use only after source-target comparison and purpose-specific invariant check.

---

### 15.4 Mathematical proof claim

AI answer:

> “This proves the theorem.”

E7G-T review:

```text
Entity: proof claim
Bridge mode: formal proof required
Required substrate: accepted definitions, assumptions, proof rules, theorem statement, checker or rigorous proof review
Risk: proof sketch mistaken for proof
Blocked overread: explanatory plausibility is not proof
```

Admissible use:

Use as proof sketch unless formal obligations are discharged.

---

### 15.5 Speculative physics analogy

AI answer:

> “Quantum measurement is projection.”

E7G-T review:

```text
Entity: physics-facing analogy
Bridge mode: formal-analogy unless empirical-testable bridge is declared
Preserved: structural resemblance between measurement contextuality and projection
Lost: physical formalism, empirical prediction, mathematical equivalence
Blocked overread: analogy is not new physics
Stop condition: no empirical-testable bridge
```

Admissible use:

Use as philosophical or formal-analogy language only.

---

### 15.6 Business dashboard recommendation

AI answer:

> “Sales dropped because customers dislike the product.”

E7G-T review:

```text
Entity: causal business claim
Source view: dashboard or sales metric
Risk: metric slice mistaken for cause
Required move: inspect time window, stock, ads, price, traffic, seasonality, reviews, distribution, data quality
Blocked overread: chart movement is not causal diagnosis
```

Admissible use:

Use as hypothesis, not as conclusion.

---

## 16. Operational Review Workflow

### Step 1 — Place the output

```text
AIAnswer : D2/D7 @ TR1 / UserQueryContext
```

### Step 2 — Classify claim types

Mark factual, interpretive, legal, medical, financial, formal, empirical, operational, or speculative claims.

### Step 3 — Identify source status

Ask whether the answer is based on:

- user-provided text;
- uploaded file;
- live web/search;
- cited source;
- tool output;
- model memory;
- generated synthesis;
- analogy;
- speculation.

### Step 4 — Record preservation/loss

Name what the answer carries and what it hides.

### Step 5 — Assign bridge mode

Use the weakest applicable bridge mode.

### Step 6 — Decide admissible use

Draft, explanation, summary, hypothesis, checklist, source-return prompt, verified answer, or stop.

### Step 7 — State next move

Possible next moves:

- accept as low-risk draft;
- verify source;
- browse/check current data;
- compare with uploaded file;
- request expert review;
- run tests;
- formalise proof;
- downgrade claim;
- stop.

---

## 17. Minimal JSON-Like Schema

```json
{
  "entity": "AI-generated answer",
  "placement": "AIAnswer : D2/D7 @ TR1 / UserQueryContext",
  "claim_types": [],
  "source_status": {
    "user_prompt": true,
    "uploaded_files": false,
    "retrieved_sources": false,
    "tool_outputs": false,
    "citations": false,
    "model_memory": true
  },
  "preserved": [],
  "lost": [],
  "distortion_risk": [],
  "bridge_mode": "operational/modelling",
  "reconstruction_status": "underdetermined unless source-linked",
  "admissible_use": [],
  "non_admissible_use": [],
  "weakest_link": "",
  "next_move": "",
  "stop_condition": ""
}
```

---

## 18. Pilot Test Design

### Pilot question

Does E7G-T linting improve the reliability of AI-output review?

### Test set

Use 30 AI answers across:

- current factual claims;
- legal/administrative explanations;
- translation QA;
- scientific explanation;
- mathematical proof sketch;
- business analysis;
- software debugging;
- speculative analogy.

### Baseline

Review outputs without E7G-T.

### Intervention

Review outputs using the AI Output as Projection MiniCard or linter.

### Measures

Track whether reviewers better identify:

- unsupported claims;
- missing sources;
- outdated facts;
- overconfident wording;
- analogy/proof confusion;
- draft/final confusion;
- legal or expert-review need;
- formal proof obligations;
- empirical bridge gaps.

### Success criterion

The linter is useful if it reduces unsupported reliance and produces clearer next actions without excessive overhead.

---

## 19. Relation to Kernel v0.9

This Application Atlas entry operationalises the following kernel elements:

- D2/D7 placement;
- projection loss;
- reconstruction status;
- bridge modes;
- claim-strength ladder;
- Proof-of-Path caution;
- Reality Bridge Discipline;
- failure-mode checklist;
- anti-replacement rule;
- next admissible move.

It is a practical projection of the kernel, not a replacement for the kernel.

---

## 20. Stop Conditions

Stop or downgrade the AI output when:

- no source is available for a strong factual claim;
- the claim may be current and no current check was performed;
- the claim is legal, medical, financial, or safety-relevant without domain support;
- a proof sketch is presented as proof;
- an analogy is presented as evidence;
- a model is presented as reality;
- the answer changes the user’s boundary without saying so;
- the answer hides uncertainty;
- the answer gives operational instructions beyond its support;
- the user may suffer harm from unsupported reliance.

---

## 21. Productisation Possibilities

This entry can become:

- a prompt pack;
- an AI-output review checklist;
- a browser extension concept;
- a QA worksheet;
- a research assistant linter;
- a translation QA add-on;
- a proof-sketch review layer;
- a business dashboard interpretation checklist;
- a training module for responsible AI use.

The most realistic first product is a lightweight checklist or prompt pack.

---

## 22. Closing Rule

Treat AI output as a view.

Return to source when reliance matters.

Declare bridge mode before claim strength rises.

Stop when the projection cannot carry the use.
