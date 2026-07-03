# E7G-T Pilot Test 002

# Translation QA Protocol

**Pilot ID:** PILOT-002  
**Kernel compatibility:** E7G-T v0.9 draft  
**Uses:** APP-002 — Translation as Invariant-Preserving Projection  
**Related artifacts:** PG-002-W — AI Answer Source-Return Review; APP-003 — Legal / Administrative Summary as Projection  
**Status:** pilot protocol / ready for real or sample translations  
**Date:** 2026-07-01  
**Primary use:** translation QA, certified-style/documentary translation review, AI-assisted translation review, source-target invariant testing

---

## 1. Purpose

This pilot tests whether E7G-T improves translation QA.

The central question is:

> Does treating translation as invariant-preserving projection improve the reviewer’s ability to identify source-target errors, documentary omissions, formatting loss, OCR risk, and purpose-specific reliability?

This pilot is not about replacing professional translation standards or human review.

It tests whether E7G-T gives reviewers a clearer way to account for what a translation preserves, what it loses, and what must be checked before reliance.

---

## 2. Core Hypothesis

E7G-T review should improve the reviewer’s ability to identify:

- name mismatches;
- date mismatches;
- number mismatches;
- omitted text;
- added text;
- mistranslated legal/administrative terms;
- lost formatting or page geometry;
- missed stamps, seals, signatures, or handwritten notes;
- OCR uncertainty;
- unclear source passages;
- certification wording defects;
- source/target boundary drift;
- purpose-specific risks;
- severity classification;
- next corrective action.

---

## 3. Materials Needed

Use the following E7G-T artifacts:

1. `E7G-T_Application_Atlas_APP-002_Translation_as_Invariant_Preserving_Projection.md`
2. `E7G-T_Kernel_v0.9_Draft_Reference_Specification.md`

Optional supporting artifacts:

3. `E7G-T_Practical_Guide_Worksheet_PG-002_AI_Answer_Source_Return_Review.md`
4. `E7G-T_Application_Atlas_APP-003_Legal_Admin_Summary_as_Projection.md`

Translation materials:

- source document;
- target translation;
- purpose / receiving authority if known;
- any client instructions;
- any previous QA notes;
- OCR text if used;
- original scan/PDF if available;
- translation draft history if available.

---

## 4. Test Design

### 4.1 Baseline QA

The reviewer reviews the translation normally, without E7G-T.

The reviewer records:

- whether the translation seems acceptable;
- visible errors;
- missing elements;
- formatting/layout problems;
- severity;
- recommended corrections.

### 4.2 E7G-T QA

The same translation is reviewed using APP-002.

The reviewer records:

- source entity;
- target entity;
- purpose context;
- invariant categories;
- preservation/loss;
- OCR risk;
- documentary artefacts;
- formatting geometry;
- severity;
- admissible use;
- stop conditions;
- required correction.

### 4.3 Comparison

Compare baseline QA with E7G-T QA.

The key question:

> Did E7G-T identify source-target invariant failures or documentary risks that ordinary QA missed?

---

## 5. Test Set

Use 5–10 translations across several document types.

Recommended distribution:

| Case | Document type | Risk type |
|---|---|---|
| 1 | Civil status certificate | Names, dates, registry data, stamps |
| 2 | Commercial register extract | company names, IDs, legal terminology |
| 3 | Court/notarial document | authority wording, signatures, seals |
| 4 | Medical certificate | terminology, dates, risk of mistranslation |
| 5 | School/university record | grades, names, institutional terms |
| 6 | Immigration/admin letter | deadline, requested documents, consequences |
| 7 | Contract excerpt | legal terms, obligations, parties |
| 8 | AI-generated translation | fluency hiding source mismatch |
| 9 | OCR-heavy scan | unreadable text, layout, stamps |
| 10 | Multilingual/apostilled document | layered authorities and annotations |

If real documents cannot be used, create anonymised or synthetic samples first.

---

## 6. Translation Placement

Use this placement for every case:

```text
SourceDocument : D2/D3/D4 @ TR0/TR1 / SourcePurposeContext
  --π_Translation^{source→target}-->
TargetTranslation : D2/D7 @ TR1 / TargetPurposeContext
[preserves: selected semantic, documentary, legal, numerical, formatting, and artefact invariants;
 loses: exact material identity, original script, visual texture, some layout, ambiguity unless marked;
 use: target-language representation for declared purpose]
```

Short OneLine:

```text
E7-OneLine: This translation is treated as a D2/D7 target-language projection of a source document under declared purpose context; admissible move: check preserved invariants and documentary artefacts; blocked overread: translation is not source identity.
```

---

## 7. Case Intake Form

Use one form per translation.

```yaml
caseId:
date:
reviewer:
sourceLanguage:
targetLanguage:
targetLocale:
documentType:
sourceFormat:
  scan:
  pdf:
  image:
  docx:
  other:
targetFormat:
declaredPurpose:
receivingAuthority:
clientInstructions:
ocrUsed:
  yes:
  no:
  unknown:
aiUsed:
  yes:
  no:
  unknown:
initialRisk:
  low:
  medium:
  high:
  stop:
notes:
```

---

## 8. Baseline QA Form

Complete this before E7G-T review.

```yaml
caseId:
baselineReviewer:
overallAssessment:
  acceptable:
  acceptableWithMinorFixes:
  needsRevision:
  notAcceptable:
errorsFound:
  - 
omissionsFound:
  - 
formattingIssues:
  - 
terminologyIssues:
  - 
documentaryArtefactIssues:
  - 
severity:
  minor:
  major:
  critical:
recommendedCorrections:
  - 
baselineNotes:
```

---

## 9. E7G-T QA Form

Use APP-002 to complete this.

```yaml
caseId:
entityOfConcern: translation
placement: "TargetTranslation : D2/D7 @ TR1 / TargetPurposeContext"
sourceEntity:
targetEntity:
purposeContext:
sourceBoundary:
targetBoundary:
invariants:
  identity:
    preserved:
    issues:
  dates:
    preserved:
    issues:
  numbers:
    preserved:
    issues:
  legalAdministrative:
    preserved:
    issues:
  formattingGeometry:
    preserved:
    issues:
  stampsSealsSignatures:
    preserved:
    issues:
  handwrittenContent:
    preserved:
    issues:
  pageStructure:
    preserved:
    issues:
  terminology:
    preserved:
    issues:
  ambiguity:
    preserved:
    issues:
lostStructure:
  - 
distortionRisks:
  - 
ocrRisks:
  - 
sourceReturnNeeded:
  - 
severity:
admissibleUse:
nonAdmissibleUse:
stopCondition:
nextCorrection:
reviewStatus:
  deliverable:
  deliverableAfterMinorFixes:
  needsRevision:
  stop:
notes:
```

---

## 10. Invariant Categories

### 10.1 Identity invariants

Check:

- personal names;
- company names;
- maiden names;
- aliases;
- transliteration;
- titles;
- roles;
- issuing authority names;
- place names.

Blocked overread:

```text
Fluent name rendering is not identity preservation.
```

### 10.2 Date invariants

Check:

- birth dates;
- issue dates;
- expiry dates;
- registration dates;
- certification dates;
- notarisation dates;
- apostille dates;
- deadlines;
- date format.

Blocked overread:

```text
Readable date is not necessarily correct date.
```

### 10.3 Number invariants

Check:

- certificate numbers;
- registry numbers;
- company IDs;
- tax IDs;
- passport numbers;
- case numbers;
- page numbers;
- monetary amounts;
- percentages;
- measurements;
- grades;
- reference codes.

Blocked overread:

```text
One digit error can change the document.
```

### 10.4 Legal/administrative invariants

Check:

- authority titles;
- document type;
- legal status;
- capacity/role;
- procedural consequence;
- official formulae;
- registry terminology;
- notarial wording;
- certification wording;
- apostille/legalisation wording.

Blocked overread:

```text
Approximate legal wording may not preserve legal function.
```

### 10.5 Documentary artefact invariants

Check:

- stamps;
- seals;
- signatures;
- handwritten notes;
- marginal annotations;
- QR codes;
- barcodes;
- logos;
- watermarks;
- page marks;
- crossings-out;
- illegible text;
- empty fields.

Recommended representation:

```text
[stamp: <visible text>]
[seal: <visible text / description>]
[handwritten signature]
[handwritten note: <text>]
[illegible]
[blank field]
```

Blocked overread:

```text
Visible artefact omitted is documentary loss.
```

### 10.6 Formatting / geometry invariants

Check:

- page order;
- headings;
- table structure;
- line breaks where meaningful;
- columns;
- labels and values;
- signature/stamp placement;
- source page markers;
- appended notes;
- cover pages;
- margins where documentary meaning is implied.

Blocked overread:

```text
Plain text may lose documentary geometry.
```

### 10.7 Ambiguity invariants

Check:

- unclear source wording;
- illegible handwriting;
- damaged scan;
- uncertain OCR;
- ambiguous abbreviation;
- unclear stamp;
- source typo;
- contradictory document data.

Recommended handling:

```text
[illegible]
[unclear]
[source spelling retained]
[translator's note: ...]
```

Blocked overread:

```text
Uncertainty must not be silently resolved.
```

---

## 11. Severity Scale

| Severity | Definition | Example |
|---|---|---|
| **Minor** | Does not materially affect identity, legal meaning, document use, or core facts. | Slight formatting difference, optional wording preference. |
| **Major** | May affect meaning, reliability, documentary function, or receiving-authority acceptance. | Wrong title, omitted stamp, mistranslated legal role. |
| **Critical** | Changes identity, date, legal status, numerical value, document effect, or could cause rejection/harm. | Wrong name, wrong date, wrong amount, omitted refusal deadline. |

### Severity rule

When in doubt between minor and major, choose major if the issue may affect reliance.

When in doubt between major and critical, choose critical if the issue may affect identity, status, deadline, amount, or legal effect.

---

## 12. Scoring Rubric

Score each case from 0–2 for each category.

| Category | 0 | 1 | 2 |
|---|---|---|---|
| Identity preservation | Misses key identity issue | Partial | Complete check |
| Date preservation | Misses date issue | Partial | Complete check |
| Number preservation | Misses numeric issue | Partial | Complete check |
| Legal/admin terminology | Unchecked/wrong | Partial | Correct and source-sensitive |
| Artefact handling | Omits artefacts | Partial | Complete bracketed handling |
| Formatting geometry | Ignores layout | Partial | Preserves meaningful geometry |
| OCR/legibility risk | Ignores uncertainty | Partial | Clearly marks uncertainty |
| Omission/addition detection | Misses changes | Partial | Clear detection |
| Severity classification | Incorrect | Partly correct | Correct severity |
| Next correction | Vague | Partial | Specific actionable fix |

Maximum score per case: 20.

---

## 13. Baseline vs E7G-T Comparison

For each case:

```yaml
caseId:
baselineScore:
e7gtScore:
scoreDifference:
issuesFoundOnlyByE7GT:
  - 
invariantsAddedByE7GT:
  - 
severityChangesAfterE7GT:
  - 
correctionsImprovedByE7GT:
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

## 14. Success Criteria

The pilot is successful if E7G-T review:

- improves average score by at least 20%;
- identifies source-target invariant failures missed in baseline review;
- improves handling of stamps, signatures, seals, and handwritten content;
- improves severity classification;
- produces clearer correction instructions;
- improves source-return discipline for OCR/legibility problems;
- does not add excessive overhead for low-risk texts.

The pilot is not successful if:

- reviewers already catch the same issues without E7G-T;
- the invariant categories slow review without improving accuracy;
- terminology adds confusion;
- E7G-T fails to improve correction quality;
- the method is too heavy for ordinary translation QA.

---

## 15. Pilot Summary Table

| Case | Document type | Baseline score | E7G-T score | Improvement | Main added value | Verdict |
|---|---|---:|---:|---:|---|---|
| 1 | Civil status |  |  |  |  |  |
| 2 | Commercial register |  |  |  |  |  |
| 3 | Court/notarial |  |  |  |  |  |
| 4 | Medical |  |  |  |  |  |
| 5 | Education |  |  |  |  |  |
| 6 | Admin letter |  |  |  |  |  |
| 7 | Contract |  |  |  |  |  |
| 8 | AI translation |  |  |  |  |  |
| 9 | OCR-heavy scan |  |  |  |  |  |
| 10 | Apostilled document |  |  |  |  |  |

---

## 16. Reviewer Instructions

For each case:

1. Save the source document and target translation.
2. Record the purpose and target locale.
3. Complete baseline QA first.
4. Complete E7G-T QA using the invariant categories.
5. Score both reviews.
6. Record issues found only by E7G-T.
7. Apply corrections.
8. Record whether the final translation became more reliable.
9. Note which fields were useful and which were too heavy.

---

## 17. Output Template

At the end of the pilot, write:

```text
Pilot Test 002 Summary

Number of translations reviewed:
Document types:
Average baseline score:
Average E7G-T score:
Average improvement:
Most common baseline misses:
Most useful invariant category:
Least useful invariant category:
Most common severity change:
Average overhead:
Best domain fit:
Weakest domain fit:
Recommended APP-002 changes:
Recommended worksheet/tool changes:
Verdict:
```

---

## 18. Expected Findings

Likely strengths:

- better documentary artefact handling;
- better name/date/number discipline;
- clearer OCR uncertainty marking;
- better severity classification;
- better correction instructions;
- stronger source-target comparison logic.

Likely weaknesses:

- may be too heavy for simple marketing or general texts;
- may require tailoring by document type;
- reviewers may need examples for bracketed artefacts;
- formatting geometry may be subjective unless purpose is declared.

Expected best fit:

- certified-style translations;
- legal/admin documents;
- civil status documents;
- official extracts;
- apostilled documents;
- OCR-heavy scans;
- immigration/supporting documents.

---

## 19. Iteration Questions

After the pilot, ask:

1. Which invariant categories caught real errors?
2. Which categories were unnecessary?
3. Did E7G-T improve severity classification?
4. Did E7G-T improve final correction quality?
5. Did it help with stamps, signatures, seals, and handwritten content?
6. Did it help with OCR uncertainty?
7. Did it slow down review too much?
8. Should there be a one-page translation QA worksheet?
9. Should there be separate templates for civil status, company, legal, medical, and education documents?
10. Should APP-002 be simplified or expanded?

---

## 20. Stop Conditions

Stop or downgrade the translation QA claim if:

- source document is unavailable;
- OCR uncertainty is unresolved;
- names, dates, or numbers cannot be verified;
- legal/admin terms are uncertain;
- stamps, seals, signatures, or handwritten notes are omitted;
- formatting geometry affects meaning and is not preserved;
- source text is illegible but not marked;
- target purpose is unknown for a high-stakes document;
- receiving-authority requirements are unknown;
- AI translation was used without source-target QA;
- reliance may affect legal status, finances, health, education, or official acceptance.

---

## 21. Closing Rule

A translation is not the source.

A fluent translation is not automatically accurate.

A checklist is not QA.

OCR text is not the document.

A visible artefact omitted is documentary loss.

Return to source when reliance matters.
