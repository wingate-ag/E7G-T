# E7G-T Practical Guide Worksheet — PG-002

# AI Answer Source-Return Review

**Worksheet ID:** PG-002-W  
**Related chapter:** PG-002 — The AI Answer Is Not the Source  
**Related atlas entry:** APP-001 — AI Output as Projection  
**Kernel compatibility:** E7G-T v0.9 draft  
**Status:** reusable worksheet / pilot tool  
**Date:** 2026-07-01  
**Primary use:** responsible AI use, AI-answer review, source checking, drafting, research support, translation QA, business analysis, decision hygiene

---

## 1. Purpose

Use this worksheet whenever an AI answer may influence a decision, document, claim, translation, analysis, proof, recommendation, or public statement.

The worksheet is built on one rule:

> The AI answer is not the source.

An AI answer is a projection. It may preserve useful structure, but it may also lose provenance, uncertainty, freshness, boundary, assumptions, and evidence.

Before relying on it, identify what it preserves, what it loses, what source return is needed, and what use is admissible.

---

## 2. Fast OneLine

```text
E7-OneLine: This AI answer is treated as a D2/D7 textual projection under user-query context; admissible move: classify claim type, verify source status, and return to source before reliance; blocked overread: AI answer is not the source.
```

---

## 3. Worksheet — Quick Version

Use this version during ordinary AI work.

| Field | Answer |
|---|---|
| AI answer / output title |  |
| Original user prompt |  |
| Output type | Draft / summary / claim / translation / code / proof sketch / recommendation / analysis / other |
| Source status | Uploaded file / pasted text / cited source / live web / tool output / model memory / unknown |
| Main claim(s) |  |
| What the answer preserves |  |
| What the answer loses |  |
| Distortion risks |  |
| Current-sensitive claims? | Yes / No |
| High-stakes domain? | Legal / medical / financial / safety / immigration / formal proof / none |
| Source return needed |  |
| Admissible use |  |
| Non-admissible use |  |
| Next move |  |
| Stop condition |  |

---

## 4. Worksheet — Full Version

### 4.1 Output identity

**AI tool / model:**  
`[insert if known]`

**Date of answer:**  
`[insert date]`

**Original user prompt:**  

```text
[insert prompt]
```

**AI answer being reviewed:**  

```text
[insert answer or link/reference]
```

**Output type:**  

- [ ] Draft text
- [ ] Summary
- [ ] Factual answer
- [ ] Recommendation
- [ ] Translation
- [ ] Translation QA
- [ ] Legal / administrative explanation
- [ ] Medical / safety explanation
- [ ] Financial / tax explanation
- [ ] Business analysis
- [ ] Code
- [ ] Mathematical proof sketch
- [ ] Scientific explanation
- [ ] Speculative analogy
- [ ] Creative text
- [ ] Other: 

---

### 4.2 E7G-T placement

```text
AIAnswer : D2/D7 @ TR1 / UserQueryContext
```

Plain meaning:

The AI answer is a visible textual output shaped by the user query, conversation context, system rules, available tools, source material, and model behaviour.

Possible source side:

```text
SourceSet? : D4/D5/D6/D7 @ TR0-TR6 / ModelAndRetrievalContext
  --π_UserQuery^{?→2}-->
AIAnswer : D2/D7 @ TR1 / UserQueryContext
```

The question mark means the source basis may be partly unknown.

---

### 4.3 Source status

What did the AI answer rely on?

- [ ] User prompt only
- [ ] Pasted text
- [ ] Uploaded file
- [ ] Retrieved web source
- [ ] Official source
- [ ] Tool output
- [ ] Code execution
- [ ] Search result
- [ ] Citation supplied by AI
- [ ] Prior conversation context
- [ ] Model memory
- [ ] Inference / synthesis
- [ ] Unknown

**Source status in one sentence:**  
`[insert]`

**Are source links or file references visible?**  
`[yes/no]`

**Are sources current enough for the claim?**  
`[yes/no/unknown/not applicable]`

---

### 4.4 Claim inventory

List the main claims made by the AI answer.

| No. | Claim | Claim type | Source status | Risk level |
|---|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |
| 4 |  |  |  |  |
| 5 |  |  |  |  |

Claim types:

- factual;
- current factual;
- legal / administrative;
- medical / safety;
- financial / tax;
- formal / mathematical;
- code / technical;
- translation / linguistic;
- causal;
- interpretive;
- speculative;
- creative;
- operational.

Risk levels:

- low;
- medium;
- high;
- stop.

---

## 5. Preservation / Loss Review

### 5.1 What the AI answer may preserve

Tick what applies:

- [ ] User’s requested structure
- [ ] User’s tone or style
- [ ] Key facts from provided text
- [ ] Summary-level meaning
- [ ] Argument structure
- [ ] Possible reasoning path
- [ ] Formatting
- [ ] Checklist structure
- [ ] Translation equivalents
- [ ] Code pattern
- [ ] Proof strategy
- [ ] Business hypothesis
- [ ] Source wording
- [ ] Other: 

**Preserved structure in one sentence:**  
`[insert]`

---

### 5.2 What the AI answer may lose

Tick what applies:

- [ ] Exact source provenance
- [ ] Full context
- [ ] Uncertainty
- [ ] Alternative interpretations
- [ ] Currentness
- [ ] Date / jurisdiction
- [ ] Exceptions
- [ ] Assumptions
- [ ] Edge cases
- [ ] Source formatting
- [ ] OCR uncertainty
- [ ] Numerical precision
- [ ] Legal qualifications
- [ ] Medical/safety qualifications
- [ ] Formal proof obligations
- [ ] Code runtime constraints
- [ ] Business data limitations
- [ ] Rival evidence
- [ ] Other: 

**Lost structure in one sentence:**  
`[insert]`

---

### 5.3 Distortion risks

Tick any risk that applies:

- [ ] Fluency makes weak support look strong.
- [ ] AI blends multiple sources without saying so.
- [ ] AI states outdated information as current.
- [ ] AI upgrades a possibility into a fact.
- [ ] AI turns analogy into evidence.
- [ ] AI turns proof sketch into proof.
- [ ] AI turns draft into final.
- [ ] AI turns summary into source identity.
- [ ] AI gives legal/medical/financial confidence without authority.
- [ ] AI hides missing data.
- [ ] AI changes the user’s boundary.
- [ ] AI invents or misstates a citation.
- [ ] AI gives causal explanation without evidence.
- [ ] Other: 

**Main distortion risk:**  
`[insert]`

---

## 6. Source-Return Checklist

Before relying on the answer, what must be checked?

- [ ] Compare against uploaded file
- [ ] Compare against pasted source text
- [ ] Check citation
- [ ] Check official source
- [ ] Check current web source
- [ ] Check date
- [ ] Check jurisdiction
- [ ] Check calculations
- [ ] Check names
- [ ] Check dates
- [ ] Check numbers
- [ ] Check legal basis
- [ ] Check medical/safety basis
- [ ] Check financial/tax basis
- [ ] Run code
- [ ] Run tests
- [ ] Use proof assistant / formal checker
- [ ] Perform translation source-target QA
- [ ] Ask domain expert
- [ ] Inspect raw data
- [ ] No reliance possible

**Required source return:**  

1. 
2. 
3. 

---

## 7. Claim-Strength Decision

### 7.1 Current claim strength

What is the strongest claim the AI answer currently supports?

- [ ] Brainstorm
- [ ] Draft
- [ ] Checklist
- [ ] Hypothesis
- [ ] Interpretation
- [ ] Source-linked summary
- [ ] Verified answer
- [ ] Proof sketch
- [ ] Formal proof
- [ ] Empirical claim
- [ ] Operational recommendation
- [ ] Stop / not reliable

**Current strength:**  
`[insert]`

### 7.2 Required upgrade path

What is required to upgrade the claim?

| Desired strength | Required support |
|---|---|
| Source-linked summary | Source comparison |
| Current factual answer | Current reliable source |
| Legal/administrative claim | Official/current source and facts of case |
| Medical/safety claim | Reliable medical/safety source and professional caution |
| Financial/tax claim | Current financial/tax source and case facts |
| Formal proof | Formal substrate or rigorous proof review |
| Code claim | Runtime, tests, specification |
| Translation QA | Source-target comparison and invariant check |
| Business recommendation | Data, causal checks, decision context |

**Upgrade requirement for this answer:**  
`[insert]`

---

## 8. Admissible and Non-Admissible Use

### 8.1 Admissible use

This AI answer may be used as:

- [ ] Brainstorm
- [ ] Draft
- [ ] Outline
- [ ] Checklist
- [ ] Hypothesis
- [ ] Search prompt
- [ ] Source-return guide
- [ ] Explanation for learning
- [ ] Translation draft
- [ ] Code draft
- [ ] Proof strategy
- [ ] Decision support after verification
- [ ] Other: 

### 8.2 Non-admissible use

This AI answer should not be used as:

- [ ] Final source
- [ ] Final legal advice
- [ ] Final medical/safety advice
- [ ] Final financial/tax advice
- [ ] Formal proof
- [ ] Certified translation without QA
- [ ] Business causal conclusion without data
- [ ] Public factual claim without source
- [ ] Decision basis where harm/risk is high
- [ ] Other: 

---

## 9. Safer Rewriting

### 9.1 Original risky claim

```text
[insert risky claim]
```

### 9.2 Safer version

Rewrite it with correct claim strength.

```text
[insert safer version]
```

Examples:

Risky:

```text
This proves the theorem.
```

Safer:

```text
This is a proof sketch. It should be treated as a strategy until the proof obligations are formally discharged.
```

Risky:

```text
You qualify for this permit.
```

Safer:

```text
Based on the stated facts, this may be a possible route, but it requires checking against current official rules and the full case facts.
```

Risky:

```text
Sales dropped because customers dislike the product.
```

Safer:

```text
Sales dropped in the selected reporting slice. Customer dissatisfaction is one possible hypothesis, but the chart does not establish causation.
```

---

## 10. Next Move

Choose one next move:

- [ ] Use as low-risk draft.
- [ ] Ask for sources.
- [ ] Check current source.
- [ ] Compare against uploaded file.
- [ ] Verify citations.
- [ ] Run calculation.
- [ ] Run code/tests.
- [ ] Formalise proof/check theorem.
- [ ] Perform translation QA.
- [ ] Ask domain expert.
- [ ] Inspect raw data.
- [ ] Downgrade claim.
- [ ] Stop.

**Next move in one sentence:**  
`[insert]`

**Owner:**  
`[insert]`

**Deadline / review date:**  
`[insert]`

---

## 11. Stop Conditions

Stop or downgrade the AI answer if:

- [ ] The answer makes a strong factual claim without source.
- [ ] The claim may have changed recently.
- [ ] The domain is legal, medical, financial, safety-critical, or immigration-related.
- [ ] The answer gives a proof sketch but no proof.
- [ ] The answer gives code but no tests or runtime context.
- [ ] The answer summarises a document without source return.
- [ ] The answer translates a document without source-target QA.
- [ ] The answer gives causal explanation from a chart alone.
- [ ] The answer uses analogy as evidence.
- [ ] The answer hides uncertainty.
- [ ] The answer has possible hallucinated citations.
- [ ] Reliance could harm people, finances, legal status, health, or safety.

**Stop condition triggered:**  
`[yes/no]`

**Reason:**  
`[insert]`

---

## 12. Completed Review Summary

Use this block at the end of the review.

```text
The AI answer is: [output type].

It appears to rely on: [source status].

It preserves: [preserved structure].

It loses: [lost structure].

The main risk is: [distortion/overread].

The strongest admissible use is: [use].

The answer does not support: [blocked overread].

Required source return: [checks].

Next move: [next action].

Review status: [usable as draft / needs verification / stop].
```

---

## 13. Example Completed Summary

```text
The AI answer is a legal/administrative orientation summary.

It appears to rely on model memory and the user’s stated facts, with no official source cited.

It preserves a possible route structure and document checklist.

It loses current legal basis, jurisdiction-specific exceptions, dates, and full case facts.

The main risk is that a plausible summary may be mistaken for legal authority.

The strongest admissible use is orientation and preparation of questions.

The answer does not support a final decision to apply.

Required source return: current official guidance, exact income threshold, family-composition rules, and expert review if needed.

Next move: verify against official sources and downgrade all eligibility wording.

Review status: needs verification.
```

---

## 14. AI Prompt Version

Use this prompt with an AI assistant:

```text
Use E7G-T PG-002 Worksheet: AI Answer Source-Return Review.

Treat the AI answer as a D2/D7 textual projection, not as the source.

Review the answer and identify:
1. output type;
2. source status;
3. main claims;
4. claim types;
5. what is preserved;
6. what is lost;
7. distortion risks;
8. source-return needs;
9. current-sensitive claims;
10. high-stakes claims;
11. admissible use;
12. non-admissible use;
13. safer rewritten claims;
14. next move;
15. stop conditions.

Block unsupported overreads such as:
- fluency is evidence;
- summary is source;
- draft is final;
- analogy is proof;
- proof sketch is proof;
- AI interpretation is expert authority.
```

---

## 15. Closing Reminder

The AI answer is not the source.

The summary is not the document.

The draft is not the final.

The proof sketch is not the proof.

The analogy is not evidence.

Return to source when reliance matters.
