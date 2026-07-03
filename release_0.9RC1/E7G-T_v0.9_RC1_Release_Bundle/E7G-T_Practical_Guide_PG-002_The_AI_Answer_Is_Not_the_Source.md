# E7G-T Practical Guide — Chapter 2

# The AI Answer Is Not the Source

**Guide ID:** PG-002  
**Kernel compatibility:** E7G-T v0.9 draft  
**Related atlas entry:** APP-001 — AI Output as Projection  
**Related worksheet:** future PG-002-W — AI Answer Source-Return Review  
**Status:** practical-guide chapter draft  
**Date:** 2026-06-30  
**Primary use:** responsible AI use, AI-assisted writing, research support, translation QA, business analysis, decision hygiene

---

## 1. The Everyday Mistake

An AI answer can sound complete.

It may be fluent.  
It may be confident.  
It may be well structured.  
It may include examples.  
It may use technical terms.  
It may sound like an expert.  
It may even be correct.

The temptation is immediate:

> “The AI said it, so now I know.”

But this is too strong.

An AI answer is not the source.

It is a **projection**: a generated, user-facing textual view shaped by the prompt, model behaviour, available tools, uploaded files, retrieved sources, conversation context, and hidden constraints.

Sometimes that projection is grounded in source text.  
Sometimes it is based on model memory.  
Sometimes it is a synthesis.  
Sometimes it is a draft.  
Sometimes it is a plausible pattern.  
Sometimes it is wrong.

The first practical rule is therefore:

> Do not let the AI answer become the source.

---

## 2. The E7G-T Repair

E7G-T changes the first question.

Do not begin with:

> “Does this sound right?”

Begin with:

> “What kind of projection is this?”

Then ask:

- What did the AI answer project from?
- Was there a source?
- Was the source visible?
- Was the source current?
- Was the source quoted or cited?
- Was the answer based on a file, a tool, memory, or inference?
- What did it preserve?
- What did it lose?
- What did it possibly distort?
- What claim strength does it support?
- What use should be blocked?

This turns AI use into source-return discipline.

---

## 3. Simple OneLine

```text
E7-OneLine: The AI answer is treated as a D2/D7 textual projection under user-query context; admissible move: verify source, bridge mode, and claim strength before reliance; blocked overread: AI answer is not the source.
```

Plain meaning:

The answer is a visible text output.  
It is shaped by context.  
It may preserve useful structure.  
It may lose provenance, uncertainty, freshness, and rival explanations.  
It must not be treated as source identity.

---

## 4. Placement

### Compact placement

```text
AIAnswer : D2/D7 @ TR1 / UserQueryContext
```

### Meaning

The AI answer is treated as:

- **D2** because it appears as visible text, code, table, explanation, translation, or summary;
- **D7** because it is governed by context: prompt, user need, system rules, tools, files, and admissible use;
- **TR1** because it is produced in a local conversational sequence;
- **UserQueryContext** because its usefulness depends on what the user asked.

### Source uncertainty

Often the source side is uncertain:

```text
SourceSet? : D4/D5/D6/D7 @ TR0-TR6 / ModelAndRetrievalContext
  --π_UserQuery^{?→2}-->
AIAnswer : D2/D7 @ TR1 / UserQueryContext
```

The question mark matters.

The AI output may be compatible with source knowledge, but compatibility is not the same as source return.

---

## 5. Projection Pattern

```text
Prompt + Context + Sources? + Tools? + ModelPatterns
  --π_AIResponse-->
AIAnswer
[preserves: selected structure;
 loses: full provenance, uncertainty, hidden assumptions, failed alternatives;
 use: draft, explanation, checklist, hypothesis, source-return prompt]
```

This is the basic grammar of AI use.

The answer preserves something.

The answer loses something.

The responsible user asks both.

---

## 6. What the AI Answer May Preserve

An AI answer may preserve:

- user instructions;
- structure from the prompt;
- wording from uploaded text;
- facts from retrieved sources;
- general domain patterns;
- useful distinctions;
- formatting;
- possible next steps;
- translation equivalents;
- code structure;
- argument structure;
- summary-level meaning;
- conventional definitions;
- reasoning outlines;
- checklists;
- examples.

This is why AI is useful.

Without preservation, AI output would be noise.

---

## 7. What the AI Answer May Lose

An AI answer may lose:

- exact provenance;
- source boundaries;
- current date sensitivity;
- uncertainty level;
- rival interpretations;
- minority views;
- legal exceptions;
- local jurisdiction details;
- medical risk;
- financial assumptions;
- source wording;
- document layout;
- OCR uncertainty;
- mathematical proof obligations;
- software runtime context;
- data quality limits;
- hidden prompt assumptions;
- reasons why an answer may fail.

This is why AI can be dangerous.

A fluent answer can hide the very things needed for reliance.

---

## 8. Projection-Loss Ledger

Use this before relying on an AI answer.

| Question | Answer |
|---|---|
| What did I ask? | Name the actual prompt or task. |
| What did the AI produce? | Draft, summary, claim, translation, proof sketch, code, recommendation, analysis. |
| What source did it use? | Uploaded file, cited source, live web, tool output, model memory, user prompt, unknown. |
| What is preserved? | Structure, wording, facts, style, possible reasoning, checklist, source content. |
| What is lost? | Provenance, uncertainty, freshness, hidden assumptions, excluded sources, domain exceptions. |
| What claim type appears? | Factual, legal, medical, financial, formal, interpretive, speculative, operational. |
| What claim strength is justified? | Draft, hypothesis, source-linked summary, verified fact, proof sketch, formal proof, stop. |
| What source return is needed? | Citation, file comparison, official source, current check, expert review, test, proof checker. |
| What use is admissible? | Draft, brainstorm, checklist, explanation, verified result, or stop. |
| What overread is blocked? | AI answer is not the source. |

---

## 9. Common AI Overreads

### 9.1 Fluency equals evidence

Bad reading:

> “It sounds professional, so it must be true.”

E7G-T repair:

Fluency is a surface quality. Evidence is a source relation.

Blocked overread:

```text
Fluency is not evidence.
```

---

### 9.2 Summary equals source

Bad reading:

> “I read the AI summary, so I know the document.”

E7G-T repair:

A summary is a projection of a source, not the source itself.

It may omit:

- exceptions;
- footnotes;
- dates;
- definitions;
- qualifications;
- formatting;
- signatures;
- tables;
- attachments;
- contradictions.

Blocked overread:

```text
Summary is not source identity.
```

---

### 9.3 Draft equals final

Bad reading:

> “The AI wrote the email/translation/report, so it is ready.”

E7G-T repair:

A draft may be useful, but final use requires purpose-specific review.

Blocked overread:

```text
Draft is not QA.
```

---

### 9.4 Current fact equals memory

Bad reading:

> “The AI knows who the CEO is / what the law says / what the price is.”

E7G-T repair:

Current facts require current checking.

Blocked overread:

```text
Model memory is not current verification.
```

---

### 9.5 Analogy equals proof

Bad reading:

> “The AI gave a powerful analogy, so the theory is proved.”

E7G-T repair:

Analogy can support thinking. It does not prove identity, formal equivalence, or empirical truth.

Blocked overread:

```text
Analogy is not proof.
```

---

### 9.6 Proof sketch equals proof

Bad reading:

> “The AI showed the proof.”

E7G-T repair:

A proof sketch may guide formal work. It must not be treated as discharged proof obligations.

Blocked overread:

```text
Proof sketch is not proof.
```

---

### 9.7 AI interpretation equals expert review

Bad reading:

> “The AI reviewed this contract / medical report / immigration path, so I am safe.”

E7G-T repair:

High-stakes domains require current sources and qualified review.

Blocked overread:

```text
AI interpretation is not expert authority.
```

---

## 10. The AI Answer MiniCard

```yaml
id: PG-002-ai-answer-review
entity: AI-generated answer
plainMeaning: A visible generated text output produced in response to a prompt.
placement: AIAnswer : D2/D7 @ TR1 / UserQueryContext
boundary:
  includes:
    - visible answer
    - user prompt
    - declared sources
    - uploaded files if actually used
    - tool outputs if actually used
  excludes:
    - uninspectable model internals
    - unstated source provenance
    - unverified external reality
projectionAccount:
  source: prompt + context + tools/sources if available + model-generated patterns
  view: visible answer
preserved:
  - selected semantic structure
  - user constraints
  - formatting
  - source content if grounded
lost:
  - full provenance
  - uncertainty
  - freshness
  - rival explanations
  - hidden assumptions
distortionRisk:
  - overconfidence
  - source blending
  - outdated facts
  - unsupported causal claims
  - unsupported legal/medical/financial certainty
reconstructionStatus: underdetermined unless source-linked
bridgeMode: depends on claim type
admissibleUse:
  - draft
  - explanation
  - checklist
  - hypothesis
  - source-return prompt
nonAdmissibleUse:
  - final reliance without verification
  - expert-domain reliance without expert/current source
  - formal proof without formal substrate
nextMove: classify claims and verify high-risk statements
blockedOverread: AI answer is not the source
```

---

## 11. The 5-Minute AI Answer Review

Use this before relying on an AI answer.

### Minute 1 — Name the output

What is it?

- draft;
- summary;
- factual claim;
- recommendation;
- translation;
- code;
- proof sketch;
- legal/medical/financial explanation;
- speculative analogy;
- checklist.

### Minute 2 — Name the source status

Was it based on:

- uploaded file?
- pasted text?
- live web?
- tool output?
- cited source?
- user prompt only?
- model memory?
- unknown source?

### Minute 3 — Name the claim type

Is the answer making:

- current factual claims?
- legal claims?
- medical claims?
- financial claims?
- formal proof claims?
- software claims?
- translation QA claims?
- causal claims?
- speculative claims?

### Minute 4 — Name the loss

What is missing?

- source;
- date;
- uncertainty;
- jurisdiction;
- assumptions;
- calculations;
- tests;
- citations;
- proof obligations;
- expert review.

### Minute 5 — Name the next move

Choose one:

- use as draft;
- verify source;
- browse/current-check;
- compare against file;
- ask for citations;
- run code/tests;
- formalise proof;
- request expert review;
- downgrade claim;
- stop.

---

## 12. Worked Example: Current Fact

AI answer:

> “The CEO of Company X is Person Y.”

E7G-T review:

```text
Entity: current factual claim
Placement: Claim : D2 @ TR1 / UserQueryContext
Bridge mode: empirical/current factual
Risk: role may have changed
Required move: current source verification
Blocked overread: model memory is not current authority
Stop condition: no current source
```

Safer conclusion:

> “This may be correct, but it requires current verification before reliance.”

---

## 13. Worked Example: Legal Explanation

AI answer:

> “You qualify for this residence permit.”

E7G-T review:

```text
Entity: legal/administrative claim
Bridge mode: empirical/legal-operational
Required substrate: current law, official guidance, facts of applicant, qualified review if needed
Risk: jurisdiction, dates, income thresholds, family composition, exceptions
Blocked overread: plausible legal summary is not legal authority
```

Safer conclusion:

> “This is an orientation claim. It must be checked against current official rules and the actual facts.”

---

## 14. Worked Example: Translation Draft

AI answer:

> “Here is the certified translation.”

E7G-T review:

```text
Entity: translation output
Placement: Translation : D2/D7 @ TR1 / TargetPurposeContext
Required source return: source document, OCR uncertainty, names, dates, numbers, stamps, signatures, page structure
Risk: fluent target text hides source mismatch
Blocked overread: translation draft is not certified QA
```

Safer conclusion:

> “This is a translation draft requiring source-target QA before use.”

---

## 15. Worked Example: Mathematical Proof

AI answer:

> “This proves the theorem.”

E7G-T review:

```text
Entity: proof claim
Bridge mode: formal proof required
Required substrate: definitions, assumptions, proof rules, proof checker or rigorous review
Risk: proof sketch mistaken for proof
Blocked overread: explanation is not proof object
```

Safer conclusion:

> “This is a proof sketch unless formal obligations are discharged.”

---

## 16. Worked Example: Business Recommendation

AI answer:

> “Sales dropped because customers dislike the product.”

E7G-T review:

```text
Entity: causal business interpretation
Source view: chart or metric
Risk: dashboard slice mistaken for cause
Required move: inspect stock, price, ads, traffic, conversion, reviews, returns, logistics, data quality
Blocked overread: AI interpretation of chart is not business reality
```

Safer conclusion:

> “The sales drop supports investigation, not yet causal diagnosis.”

---

## 17. Decision Tiers for AI Output

| Tier | Meaning | AI output use |
|---|---|---|
| Tier 0 | Brainstorm | Safe for ideas. |
| Tier 1 | Draft | Safe as editable text. |
| Tier 2 | Checklist | Safe for structuring review. |
| Tier 3 | Hypothesis | Safe for investigation. |
| Tier 4 | Source-linked summary | Usable after source comparison. |
| Tier 5 | Verified answer | Requires citations, current checks, tests, or source return. |
| Tier 6 | Reliance decision | Requires domain-appropriate evidence/expert/formal/empirical support. |

### Tier rule

AI output alone rarely supports Tier 5 or Tier 6.

---

## 18. Practical Prompts

### Prompt 1 — AI answer review

```text
Use E7G-T to review this AI answer as a projection, not as the source. Identify what it preserves, what it loses, what claim types it makes, what source return is needed, what use is admissible, and what overread must be blocked.
```

### Prompt 2 — Source-return check

```text
For each important claim in this AI answer, classify whether it is source-linked, unsourced, current-sensitive, expert-sensitive, formal, empirical, interpretive, or draft-only. Tell me what must be checked before reliance.
```

### Prompt 3 — Downgrade overconfident AI text

```text
Rewrite this AI answer so that every claim has an appropriate claim strength. Downgrade unsupported claims, mark source-return needs, and block any overread.
```

### Prompt 4 — AI answer before decision

```text
I am considering making a decision based on this AI answer. Use E7G-T to identify the weakest link, missing evidence, required verification, admissible decision tier, and stop conditions.
```

---

## 19. Source-Return Checklist

Before relying on an AI answer, check what source return is needed:

- [ ] Uploaded source file comparison
- [ ] Current web/source check
- [ ] Official legal/administrative source
- [ ] Medical or safety source
- [ ] Financial data source
- [ ] Mathematical proof check
- [ ] Code execution or tests
- [ ] Translation source-target QA
- [ ] Citation verification
- [ ] Expert review
- [ ] Raw data review
- [ ] Date/jurisdiction check
- [ ] Assumption check
- [ ] Stop / no reliance

---

## 20. Stop Conditions

Stop or downgrade the AI answer when:

- the answer makes a strong factual claim without source;
- the claim may have changed recently;
- the domain is legal, medical, financial, safety-critical, or high stakes;
- the answer gives a proof sketch but no proof;
- the answer gives code but no tests or runtime context;
- the answer summarises a document without source return;
- the answer translates a document without source-target QA;
- the answer gives causal explanation from a chart alone;
- the answer uses analogy as evidence;
- the answer hides uncertainty;
- reliance could harm people, finances, legal status, health, or safety.

---

## 21. Chapter Summary

AI is useful because it can preserve structure.

AI is dangerous because it can hide the source relation.

A fluent answer is not evidence.

A summary is not the source.

A draft is not QA.

A proof sketch is not proof.

An analogy is not evidence.

The practical question is:

> What did this AI answer project from, what did it preserve, what did it lose, and what may I responsibly do next?

---

## 22. Closing Rule

The AI answer is not the source.

The summary is not the document.

The draft is not the final.

The proof sketch is not the proof.

The analogy is not evidence.

Return to source when reliance matters.
