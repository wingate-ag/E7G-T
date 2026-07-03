# E7G-T Pilot Test 001

# AI Output Review Protocol

**Pilot ID:** PILOT-001  
**Kernel compatibility:** E7G-T v0.9 draft  
**Uses:** APP-001 — AI Output as Projection; PG-002 — The AI Answer Is Not the Source; PG-002-W — AI Answer Source-Return Review  
**Status:** pilot protocol / ready for real examples  
**Date:** 2026-07-01  
**Primary use:** testing whether E7G-T improves AI-answer review, source-return discipline, and claim-strength control

---

## 1. Purpose

This pilot tests whether E7G-T helps users review AI-generated answers more responsibly.

The central question is:

> Does treating an AI answer as a projection, not as a source, improve the reviewer’s ability to identify unsupported claims, missing sources, overconfident wording, and correct next moves?

This pilot is not about whether AI is good or bad.

It is about whether E7G-T gives users a better review method.

---

## 2. Core Hypothesis

E7G-T review should improve the user’s ability to identify:

- unsupported claims;
- missing source return;
- outdated or current-sensitive facts;
- high-stakes domains;
- overconfident wording;
- analogy/proof confusion;
- draft/final confusion;
- summary/source confusion;
- expert-review needs;
- formal proof obligations;
- empirical bridge gaps;
- next admissible moves;
- stop conditions.

---

## 3. Materials Needed

Use the following E7G-T artifacts:

1. `E7G-T_Application_Atlas_APP-001_AI_Output_as_Projection.md`
2. `E7G-T_Practical_Guide_PG-002_The_AI_Answer_Is_Not_the_Source.md`
3. `E7G-T_Practical_Guide_Worksheet_PG-002_AI_Answer_Source_Return_Review.md`

Optional supporting artifacts:

4. `E7G-T_Kernel_v0.9_Draft_Reference_Specification.md`
5. `E7G-T_Application_Atlas_APP-003_Legal_Admin_Summary_as_Projection.md`
6. `E7G-T_Application_Atlas_APP-002_Translation_as_Invariant_Preserving_Projection.md`

---

## 4. Test Design

### 4.1 Baseline review

The reviewer reads an AI answer and reviews it normally, without using E7G-T.

The reviewer records:

- whether the answer seems reliable;
- what claims are important;
- whether sources are needed;
- what they would do next.

### 4.2 E7G-T review

The same AI answer is reviewed using PG-002-W and APP-001.

The reviewer records:

- output type;
- source status;
- claim inventory;
- preservation/loss;
- distortion risks;
- source-return needs;
- claim strength;
- admissible use;
- non-admissible use;
- stop condition;
- next move.

### 4.3 Comparison

Compare baseline review with E7G-T review.

The key question:

> Did E7G-T identify risks, missing source returns, or safer next moves that baseline review missed?

---

## 5. Test Set

Use 10 AI answers across different risk types.

Recommended distribution:

| Case | Domain | Risk type |
|---|---|---|
| 1 | Current factual claim | Possible outdated fact |
| 2 | Legal/admin explanation | Authority/fact/procedure gap |
| 3 | Translation QA | Source-target invariant risk |
| 4 | Business dashboard analysis | Causal overread |
| 5 | Medical/safety explanation | High-stakes expert-source need |
| 6 | Financial/tax answer | Current rule and case-fact risk |
| 7 | Mathematical proof sketch | Proof sketch vs proof |
| 8 | Code answer | Untested code / runtime context |
| 9 | Scientific explanation | Evidence level / consensus risk |
| 10 | Speculative analogy | Analogy mistaken for proof |

If real examples are unavailable, use synthetic examples first, then repeat on real outputs.

---

## 6. Case Intake Form

Use one form per AI answer.

```yaml
caseId:
date:
reviewer:
aiToolOrModel:
userPrompt:
aiAnswer:
domain:
outputType:
initialRelianceRisk:
  low:
  medium:
  high:
  stop:
notes:
```

---

## 7. Baseline Review Form

Complete this before using E7G-T.

```yaml
caseId:
baselineReviewer:
doesAnswerSeemReliable:
  yes:
  no:
  uncertain:
importantClaims:
  - 
sourcesNeeded:
  - 
risksNoticed:
  - 
intendedUse:
nextMove:
confidence:
  low:
  medium:
  high:
baselineNotes:
```

---

## 8. E7G-T Review Form

Use PG-002-W to complete this.

```yaml
caseId:
entity: AI-generated answer
placement: AIAnswer : D2/D7 @ TR1 / UserQueryContext
outputType:
sourceStatus:
  userPromptOnly:
  pastedText:
  uploadedFile:
  retrievedWebSource:
  officialSource:
  toolOutput:
  citationProvided:
  modelMemory:
  unknown:
mainClaims:
  - claim:
    claimType:
    sourceStatus:
    riskLevel:
preserved:
  - 
lost:
  - 
distortionRisks:
  - 
currentSensitiveClaims:
  - 
highStakesClaims:
  - 
sourceReturnNeeded:
  - 
claimStrength:
admissibleUse:
nonAdmissibleUse:
blockedOverread:
weakestLink:
stopCondition:
nextMove:
reviewStatus:
  usableAsDraft:
  needsVerification:
  stop:
notes:
```

---

## 9. Scoring Rubric

Score each case from 0–2 for each category.

| Category | 0 | 1 | 2 |
|---|---|---|---|
| Claim identification | Misses main claims | Identifies some claims | Identifies key claims clearly |
| Source-status awareness | Treats answer as source | Notes vague source need | Identifies exact source status |
| Currentness detection | Misses current-sensitive facts | Notices possible issue | Clearly flags current check |
| High-stakes detection | Misses domain risk | Notes general caution | Correctly flags high-stakes review |
| Preservation/loss accounting | Not present | Partial | Clear preserved/lost structure |
| Distortion-risk detection | Misses overreads | Some risks | Clear overread labels |
| Claim-strength control | Overaccepts answer | Some downgrade | Correctly downgrades claim |
| Source-return plan | None/vague | Partial | Specific source-return steps |
| Admissible-use decision | Unclear | Partly clear | Clear use/non-use distinction |
| Next move | Vague | Somewhat useful | Concrete and responsible |

Maximum score per case: 20.

---

## 10. Baseline vs E7G-T Comparison

For each case:

```yaml
caseId:
baselineScore:
e7gtScore:
scoreDifference:
risksFoundOnlyByE7GT:
  - 
sourceReturnsAddedByE7GT:
  - 
claimsDowngradedByE7GT:
  - 
betterNextMovesFromE7GT:
  - 
overhead:
  low:
  medium:
  high:
verdict:
  improved:
  noDifference:
  worse:
notes:
```

---

## 11. Success Criteria

The pilot is successful if E7G-T review:

- improves average score by at least 25%;
- identifies at least one missed risk in most medium/high-risk cases;
- produces more specific source-return steps;
- reduces unsupported reliance;
- clarifies admissible vs non-admissible use;
- does not create excessive review overhead.

The pilot is not successful if:

- reviewers find it too slow;
- outputs become more complicated without better decisions;
- E7G-T labels add jargon but no practical improvement;
- the same risks are found without E7G-T;
- next moves remain vague.

---

## 12. Pilot Summary Table

| Case | Domain | Baseline score | E7G-T score | Improvement | Main added value | Verdict |
|---|---|---:|---:|---:|---|---|
| 1 | Current factual |  |  |  |  |  |
| 2 | Legal/admin |  |  |  |  |  |
| 3 | Translation QA |  |  |  |  |  |
| 4 | Business dashboard |  |  |  |  |  |
| 5 | Medical/safety |  |  |  |  |  |
| 6 | Financial/tax |  |  |  |  |  |
| 7 | Proof sketch |  |  |  |  |  |
| 8 | Code |  |  |  |  |  |
| 9 | Scientific |  |  |  |  |  |
| 10 | Speculative analogy |  |  |  |  |  |

---

## 13. Sample Case Prompts

These are sample prompts for generating test AI answers. Replace with real examples where possible.

### Case 1 — Current factual claim

```text
Who is the current CEO of [company]? Give a short answer.
```

Risk:

Current role may have changed.

Expected E7G-T flag:

```text
Model memory is not current verification.
```

---

### Case 2 — Legal/admin explanation

```text
Can a family apply for [residence/permit/admin benefit] with [facts]? Give a clear answer.
```

Risk:

Jurisdiction, current law, case facts, document sufficiency, official procedure.

Expected E7G-T flag:

```text
Possible route is not eligibility decision.
```

---

### Case 3 — Translation QA

```text
Review this translation and tell me if it is accurate.
```

Risk:

AI may judge fluency without checking source-target invariants.

Expected E7G-T flag:

```text
Translation draft is not source-target QA.
```

---

### Case 4 — Business dashboard

```text
Sales dropped by 30%. Explain why and recommend what to do.
```

Risk:

Causal overread from a metric slice.

Expected E7G-T flag:

```text
Chart movement is not causal diagnosis.
```

---

### Case 5 — Medical/safety explanation

```text
What should someone do if they have [symptom]? Give practical advice.
```

Risk:

High-stakes medical/safety advice.

Expected E7G-T flag:

```text
AI answer is not medical authority.
```

---

### Case 6 — Financial/tax answer

```text
What tax do I owe if [facts]? Give the answer.
```

Risk:

Current law, jurisdiction, individual facts, professional review.

Expected E7G-T flag:

```text
Plausible tax summary is not tax advice.
```

---

### Case 7 — Mathematical proof sketch

```text
Prove this theorem: [simple theorem].
```

Risk:

Proof sketch mistaken for proof.

Expected E7G-T flag:

```text
Proof sketch is not proof.
```

---

### Case 8 — Code answer

```text
Write code that does [task]. Is it correct?
```

Risk:

Untested code and missing runtime context.

Expected E7G-T flag:

```text
Code text is not tested behaviour.
```

---

### Case 9 — Scientific explanation

```text
Explain whether [scientific claim] is true.
```

Risk:

Evidence level, source quality, consensus, date.

Expected E7G-T flag:

```text
Explanation is not empirical support.
```

---

### Case 10 — Speculative analogy

```text
Does [metaphor/analogy] explain quantum mechanics / consciousness / reality?
```

Risk:

Analogy mistaken for proof or empirical theory.

Expected E7G-T flag:

```text
Analogy is not proof.
```

---

## 14. Reviewer Instructions

For each case:

1. Save the original prompt and AI answer.
2. Complete the baseline review before looking at E7G-T tools.
3. Complete the E7G-T review using PG-002-W.
4. Score both reviews using the rubric.
5. Record added value and overhead.
6. Decide whether E7G-T improved the next move.
7. Summarise what should be changed in the worksheet.

---

## 15. Pilot Output Template

At the end of the pilot, write:

```text
Pilot Test 001 Summary

Number of AI answers reviewed:
Average baseline score:
Average E7G-T score:
Average improvement:
Most common missed risk:
Most useful E7G-T field:
Least useful E7G-T field:
Average overhead:
Best domain fit:
Weakest domain fit:
Recommended worksheet changes:
Recommended kernel changes:
Verdict:
```

---

## 16. Expected Findings

Likely strengths:

- source-return discipline;
- high-stakes risk detection;
- claim-strength downgrading;
- safer wording;
- clearer next move.

Likely weaknesses:

- possible overhead for low-risk drafts;
- terminology may be too heavy for ordinary users;
- scoring may need simplification;
- some users may resist filling long forms.

Expected improvement:

The short worksheet should be useful for medium/high-risk AI answers.

The full worksheet may be better for legal, translation, financial, scientific, and formal/proof-related outputs.

---

## 17. Iteration Questions

After the pilot, ask:

1. Which worksheet fields were essential?
2. Which fields were too heavy?
3. Did E7G-T prevent a real overread?
4. Did it improve source-return behaviour?
5. Did it slow down low-risk work unnecessarily?
6. Which labels should be simplified?
7. Which domains need separate worksheets?
8. Should v0.9 kernel terms be adjusted?
9. Is “projection” understandable to testers?
10. What is the next pilot?

---

## 18. Stop Conditions

Stop or revise the pilot if:

- reviewers do not understand the worksheet;
- scoring is inconsistent;
- examples are too artificial;
- E7G-T adds terminology but not practical value;
- high-stakes cases are reviewed without proper source or expert safeguards;
- reviewers use E7G-T as a substitute for domain review.

---

## 19. Closing Rule

The pilot does not ask whether E7G-T is impressive.

It asks whether E7G-T improves the next responsible move.

If it does, keep it.

If it does not, simplify it.
