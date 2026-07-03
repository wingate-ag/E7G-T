# E7G-T Application Atlas — Entry 002

# Translation as Invariant-Preserving Projection

**Atlas ID:** APP-002  
**Kernel compatibility:** E7G-T v0.9 draft  
**Related practical layer:** PG-001 — The Chart Is Not the Business  
**Related method family:** source/view discipline, projection-loss accounting, invariant preservation, QA review  
**Status:** pilot-ready application entry  
**Date:** 2026-06-29  
**Primary use:** translation QA, certified-style translation, legal/administrative translation, bilingual review, OCR-to-translation workflows, source-target accountability

---

## 1. Entry Purpose

This Application Atlas entry applies E7G-T v0.9 to translation.

The basic claim is:

> A translation is a purpose-bound projection of a source text into a target language, where the central task is to preserve required invariants while honestly recording unavoidable loss, transformation, uncertainty, and non-transferable structure.

This entry is designed for:

- professional translation;
- certified-style translation;
- legal and administrative translation;
- OCR-to-translation workflows;
- bilingual QA;
- terminology review;
- source-target layout review;
- AI-assisted translation checking;
- reviewer fix sheets;
- translation project governance.

---

## 2. Entity of Concern

**Entity:** translation as target-language artefact.

The entity of concern is not only the target text. It is the whole translation event:

- source document;
- source language;
- target language;
- intended use;
- target jurisdiction or recipient;
- layout/geometry constraints;
- terminology choices;
- translator/reviewer notes;
- unreadable or uncertain items;
- seals, stamps, signatures, handwritten marks, and graphic artefacts;
- certification or declaration language where required;
- QA result.

E7G-T treats the translated document as a projection of a source document under a purpose context.

---

## 3. Source / View Distinction

| Layer | Description |
|---|---|
| **Source** | Original document, source-language text, layout, seals, stamps, signatures, numbering, handwritten insertions, omissions, errors, and material form. |
| **Projection context** | Target language, intended recipient, certification style, legal/administrative purpose, formatting constraints, translation brief, jurisdictional expectations, QA posture. |
| **View** | Target-language translation, including translated text, reproduced structure, translator notes, bracketed artefact descriptions, and certification statement. |
| **Risk** | A fluent target text may hide missing source elements, wrong boundary, altered legal force, mistranslated names/dates, or unmarked uncertainty. |

### Core E7G-T repair

Do not ask only:

> “Does the translation read well?”

Ask:

> “Which source invariants must survive this projection, and which losses must be marked?”

---

## 4. Placement

### Compact placement

```text
Translation : D2/D7 @ TR1 / TargetUseContext
SourceDocument : D2/D3/D4 @ TR0/TR1 / SourceContext
```

### Meaning

The translation is treated as:

- **D2** because it appears as target-language text and layout;
- **D7** because its correctness depends on purpose, recipient, jurisdiction, certification posture, terminology norms, and client instructions;
- **TR1** because the translation is produced and reviewed in a local workflow sequence;
- **TargetUseContext** because translation quality is use-bound.

The source document is treated as:

- **D2** because it contains visible text and graphic layout;
- **D3** when the physical/documentary artefact matters;
- **D4** where issue date, certification sequence, amendments, or procedural history matter;
- **TR0/TR1** depending on whether it is treated as a fixed record or a workflow object.

---

## 5. Projection Pattern

```text
SourceDocument : D2/D3/D4 @ TR0/TR1 / SourceContext
  --π_TranslationPurpose^{source→target}-->
Translation : D2/D7 @ TR1 / TargetUseContext
[preserves: required semantic, legal, documentary, identity, numerical, structural, and purpose-specific invariants;
 loses: source-language form, some layout materiality, ambiguity texture, handwriting appearance, seal graphics, typography, local legal-cultural resonance;
 use: target-language reliance under declared purpose]
```

Translation is not identity.

Translation is not free paraphrase.

Translation is a disciplined projection under purpose constraints.

---

## 6. Translation Invariants

An invariant is something that must survive the translation for the target document to be fit for purpose.

### 6.1 Identity invariants

These include:

- personal names;
- company names;
- registry numbers;
- tax numbers;
- identity document numbers;
- addresses;
- birth dates;
- marriage dates;
- court or office names;
- signature identities;
- certification authority names.

### 6.2 Numerical invariants

These include:

- dates;
- amounts;
- percentages;
- page numbers;
- article numbers;
- statute references;
- certificate numbers;
- registry entries;
- weights, measures, dimensions;
- invoice numbers;
- serial numbers.

### 6.3 Legal/administrative invariants

These include:

- legal status;
- rights and obligations;
- official capacity;
- procedural action;
- certification wording;
- notarial formula;
- apostille formula;
- register extract status;
- stamp function;
- issuing authority;
- evidentiary posture.

### 6.4 Documentary invariants

These include:

- headings;
- section hierarchy;
- tables;
- stamps;
- seals;
- signatures;
- handwritten marks;
- blank fields;
- corrections;
- crossed-out text;
- marginal notes;
- page breaks where relevant;
- visible omissions;
- unreadable text.

### 6.5 Functional invariants

These include:

- purpose of the document;
- recipient expectations;
- certification style;
- level of literalness;
- target-jurisdiction readability;
- genre conventions;
- document registerability;
- use in evidence or administrative submission.

---

## 7. Preservation / Loss Ledger

| Question | Review instruction |
|---|---|
| What must be preserved? | Identify source invariants required by target use. |
| What can transform? | Identify structures that may be adapted without loss of function. |
| What must be marked? | Identify unreadable text, seals, stamps, signatures, handwriting, omissions, and ambiguities. |
| What may be lost? | Identify source-language nuance, typography, spatial exactness, graphic materiality, legal-cultural resonance. |
| What must not be added? | Prevent explanatory over-translation, invented legal effect, or unmarked assumptions. |
| What is the admissible use? | State whether the translation is draft, review copy, certified-style translation, official submission support, or internal reference. |

---

## 8. Loss Types in Translation

### 8.1 Linguistic loss

Words do not map perfectly across languages. Some terms have no exact equivalent.

Repair:

Use the closest functional equivalent, add bracketed translator note only when necessary, and preserve the source term where required.

### 8.2 Legal-cultural loss

A legal institution in one country may not have an exact equivalent in another.

Repair:

Prefer transparent translation over false domestic equivalence.

Example:

Do not silently turn a foreign office into a target-country office if the institutions differ materially.

### 8.3 Layout loss

The target language may expand or compress text, changing the visual geometry.

Repair:

Preserve meaningful structure rather than pixel-perfect appearance unless the brief requires recreation.

### 8.4 Graphic artefact loss

Stamps, seals, logos, signatures, and handwriting cannot be translated as ordinary text.

Repair:

Represent them in brackets.

Examples:

```text
[handwritten signature]
[stamp: text visible on stamp]
[round seal: issuing authority]
[illegible handwritten note]
```

### 8.5 OCR loss

OCR may misread source characters, names, dates, diacritics, numbers, or table structure.

Repair:

Use source-image review for high-risk fields. Mark uncertainty rather than guessing.

### 8.6 Purpose loss

A translation may be linguistically correct but unfit for the intended recipient.

Repair:

Declare the purpose and review against that purpose.

---

## 9. Reconstruction Status

A translation may help reconstruct source meaning, but it is not the source.

### Default reconstruction status

```text
ρ_TargetUse(Translation) ⇒ {source meaning approximation, preserved invariants, marked artefacts, translator decisions}
```

This means the translation constrains source meaning, but does not replace the source document.

### Safe wording

The translation renders the source document for the stated purpose.

### Unsafe wording

The translation is identical to the source.

---

## 10. Bridge Mode

Translation usually operates under an **operational/documentary bridge**.

For kernel compatibility, it may also involve:

| Bridge mode | Translation use |
|---|---|
| **none** | No cross-domain claim; simple language transfer only. |
| **philosophical-interpretation** | Interpreting literary or conceptual meaning. |
| **formal-analogy** | Treating translation as projection for modelling purposes. |
| **formal-compatibility** | Encoding translation QA as structured schema or invariant ledger. |
| **empirical-testable** | Verifying factual source data, legal currentness, or document authenticity. |
| **operational/documentary use posture** | Producing a fit-for-purpose target document under client/recipient constraints. |

### Bridge rule

A translation’s admissible use depends on purpose, not only linguistic fluency.

---

## 11. Claim-Strength Lint for Translation

| Claim | Required support |
|---|---|
| “The translation is fluent.” | Target-language readability review. |
| “The translation is accurate.” | Source-target invariant comparison. |
| “The translation is complete.” | Full visible-source coverage check. |
| “The translation is certified-style.” | Certification statement, translator identity/role, date, scope, and declaration posture. |
| “The translation is legally acceptable.” | Recipient/jurisdiction acceptance or competent legal/administrative review. |
| “The source document is authentic.” | Separate authenticity evidence; translation alone cannot prove authenticity. |
| “The term is legally equivalent.” | Legal-comparative support or cautious transparent rendering. |
| “OCR is reliable.” | Source-image verification of high-risk fields. |

### Upgrade test

Before calling a translation deliverable, ask:

> Which invariants were checked against the source, and which uncertainties remain marked?

---

## 12. Translation MiniCard Template

```yaml
id: APP-002-translation-review
entity: translation
plainMeaning: Target-language projection of a source document under stated purpose.
placement: Translation : D2/D7 @ TR1 / TargetUseContext
sourcePlacement: SourceDocument : D2/D3/D4 @ TR0/TR1 / SourceContext
boundary:
  includes:
    - full visible source text
    - layout-relevant structure
    - stamps/seals/signatures/handwriting
    - target recipient purpose
    - certification statement if required
  excludes:
    - authentication of source unless separately checked
    - legal advice unless separately provided
    - unvisible/non-supplied source material
projectionAccount:
  source: source document + visual artefacts + purpose context
  view: target-language translation
preserved:
  - identity invariants
  - numerical invariants
  - legal/administrative function
  - documentary structure
  - certification posture
lost:
  - source-language form
  - graphic materiality
  - some typography
  - legal-cultural resonance
  - ambiguity texture unless marked
transformed:
  - syntax
  - word order
  - target-language terminology
  - formatting where necessary
marked:
  - signatures
  - stamps
  - seals
  - illegible text
  - uncertain readings
  - translator notes
reconstructionStatus: source meaning approximated for target use; source identity not replaced
bridgeMode: operational/documentary; empirical checks only where source verification is performed
admissibleUse:
  - target-language understanding
  - submission support if fit for recipient
  - review copy
  - certified-style use if declaration requirements met
nonAdmissibleUse:
  - proof of source authenticity
  - legal advice
  - unverified factual expansion beyond source
nextMove: run source-target invariant check
blockedOverread: fluent translation is not documentary completeness
```

---

## 13. Full Translation QA Card

```yaml
projectId:
sourceLanguage:
targetLanguage:
sourceDocumentType:
targetUse:
recipient:
reviewMode:
  - OCR check
  - translation QA
  - certified-style check
  - layout check
  - terminology check
entityOfConcern: translation
sourceBoundary:
  pages:
  visibleText:
  stampsSealsSignatures:
  handwrittenItems:
  tables:
  marginalia:
targetBoundary:
  translatedPages:
  certificationStatement:
  pageMarkers:
  bracketedArtefacts:
identityInvariants:
  names:
  dates:
  numbers:
  addresses:
  authorities:
numericalInvariants:
legalAdministrativeInvariants:
documentaryInvariants:
terminologyDecisions:
uncertaintiesMarked:
omissions:
formattingLoss:
sourceReturnRequired:
qaFindings:
  critical:
  major:
  minor:
  preferential:
admissibleUse:
nonAdmissibleUse:
stopCondition:
nextMove:
reviewerNotes:
```

---

## 14. Source-Target QA Workflow

### Step 1 — Place the task

```text
Translation : D2/D7 @ TR1 / TargetUseContext
```

Ask:

- What is the source document?
- What is the target language?
- What is the intended use?
- Who is the recipient?
- Is this draft, certified-style, legal, administrative, internal, or publication translation?

### Step 2 — Bound the source

List:

- pages;
- visible text;
- tables;
- stamps;
- seals;
- signatures;
- handwritten marks;
- blank fields;
- unreadable sections;
- later annotations;
- attachments.

### Step 3 — Identify required invariants

Mark:

- names;
- dates;
- numbers;
- official capacities;
- legal actions;
- amounts;
- registry references;
- certificate numbers;
- authorities;
- page markers;
- signatures and stamps.

### Step 4 — Compare source to target

For every source unit, ask:

- Is it translated?
- Is it omitted?
- Is it mistranslated?
- Is it over-translated?
- Is uncertainty marked?
- Is the target idiomatic enough for purpose?
- Is the legal/documentary role preserved?

### Step 5 — Record loss and transformations

Do not hide unavoidable loss.

Record:

- illegible text;
- approximate readings;
- non-equivalent institutions;
- formatting differences;
- graphic artefacts;
- translator notes.

### Step 6 — Decide admissible use

Possible statuses:

- draft only;
- QA pending;
- source-return needed;
- fit for internal use;
- fit for recipient review;
- certified-style deliverable;
- stop.

---

## 15. Bracketed Artefact Convention

When graphic or non-textual source elements appear, use bracketed descriptions.

Examples:

```text
[handwritten signature]
[illegible handwritten signature]
[stamp: Registry Office in X]
[round seal: Ministry of Justice]
[rectangular stamp: text partially illegible]
[logo]
[blank field]
[crossed-out text: ...]
[translator’s note: source text illegible]
```

### Rule

Do not silently omit visual documentary elements.

If it matters to the document, represent it.

---

## 16. Common Failure Modes

### 16.1 Fluent but incomplete

The target reads well but misses a stamp, note, line, page marker, or handwritten item.

**Blocked overread:** fluency is not completeness.

### 16.2 Literal but misleading

The target follows words closely but misrepresents legal or administrative function.

**Blocked overread:** literalness is not functional equivalence.

### 16.3 Domesticating the institution

A foreign office or legal category is replaced with a familiar target-country term that changes function.

**Blocked overread:** familiar wording is not source transparency.

### 16.4 OCR hallucination

OCR creates plausible text that is not actually in the source.

**Blocked overread:** OCR text is not source text until visually checked.

### 16.5 Unmarked uncertainty

The translator guesses an unclear name, date, stamp, or handwriting.

**Blocked overread:** guessed certainty is not accuracy.

### 16.6 Certification overclaim

A translator declaration implies more than the translator can attest.

**Blocked overread:** translation certification is not source authentication.

### 16.7 Layout overfocus

The translation preserves visual shape but loses meaning, terminology, or target readability.

**Blocked overread:** geometry is not adequacy by itself.

### 16.8 Meaning overfocus

The translation conveys general meaning but loses documentary details required for administrative use.

**Blocked overread:** gist is not documentary translation.

---

## 17. OneLine Templates

### Generic translation

```text
E7-OneLine: The translation is treated as a D2/D7 target-language projection of a D2/D3 source document under stated-use context; admissible move: check identity, numerical, legal, and documentary invariants; blocked overread: fluent target text is not source completeness.
```

### Certified-style translation

```text
E7-OneLine: The certified-style translation is treated as a purpose-bound documentary projection with declaration posture; admissible move: verify full visible-source coverage and bracketed artefacts; blocked overread: certification does not authenticate the source.
```

### OCR-based translation

```text
E7-OneLine: The OCR translation is treated as a projection stack from source image to OCR text to target text; admissible move: visually verify high-risk fields; blocked overread: OCR output is not source text.
```

### Legal/administrative translation

```text
E7-OneLine: The legal-administrative translation is treated as an invariant-preserving projection under recipient context; admissible move: preserve official function and mark uncertainty; blocked overread: familiar target term is not legal equivalence.
```

---

## 18. Worked Example — Marriage Certificate

Source type:

Marriage certificate with stamps and signatures.

Required invariants:

- names of spouses;
- dates of birth;
- date of marriage;
- place of marriage;
- registry office;
- certificate number;
- official capacity;
- signatures;
- stamps/seals;
- later annotations if visible.

Projection risk:

A fluent translation may omit stamp text, handwritten signatures, or page structure.

E7G-T review:

```text
Entity: certified-style marriage certificate translation
Placement: Translation : D2/D7 @ TR1 / AdministrativeUseContext
Source: Certificate : D2/D3/D4 @ TR0/TR1 / SourceDocumentContext
Preserves: identity, date, registry, marital event, authority, visible certification artefacts
Loses: graphic appearance of seals/signatures, source-language form, original typography
Marked: [handwritten signature], [stamp: ...], [seal: ...]
Bridge mode: operational/documentary
Admissible use: target-language submission support if recipient accepts this format
Blocked overread: translation does not authenticate source
Next move: source-target invariant QA
```

---

## 19. Worked Example — Commercial Register Extract

Source type:

Company register extract.

Required invariants:

- company name;
- registration number;
- registered office;
- legal form;
- directors/officers;
- scope of business;
- issue date;
- authority;
- apostille or notarial annotations if present;
- page and table structure.

Failure risk:

If a company number or legal form is mistranslated, the document may become unreliable for administrative use.

Blocked overread:

```text
Readable company summary is not register-accurate translation.
```

Next move:

Check every identity, number, legal role, and authority line against the source image.

---

## 20. AI-Assisted Translation QA

AI can help with:

- initial OCR cleanup;
- draft translation;
- terminology alternatives;
- source-target comparison;
- omission detection;
- formatting reconstruction;
- QA fix sheets;
- consistency review.

AI must not be treated as final authority.

### AI translation stack

```text
SourceImage
  --π_OCR-->
OCRText
  --π_MT/AI-->
DraftTranslation
  --π_QA-->
ReviewedTranslation
```

Loss accumulates across the stack.

### AI QA rule

Use AI to expose possible issues.

Use source comparison to confirm issues.

Use professional judgement to resolve issues.

---

## 21. Translation QA Labels

Use these labels in fix sheets:

```text
[IDENTITY-INVARIANT]
[DATE-INVARIANT]
[NUMBER-INVARIANT]
[LEGAL-FUNCTION]
[DOCUMENTARY-STRUCTURE]
[STAMP/SEAL]
[SIGNATURE]
[HANDWRITING]
[OCR-RISK]
[OMISSION]
[OVER-TRANSLATION]
[TERMINOLOGY]
[LAYOUT]
[UNCERTAINTY]
[STOP]
```

---

## 22. Severity Scale

| Severity | Meaning |
|---|---|
| **Critical** | Defect may change identity, legal/administrative effect, admissibility, or core document meaning. |
| **Major** | Defect materially affects accuracy, completeness, or recipient usability. |
| **Minor** | Defect affects style, consistency, formatting, or low-risk detail. |
| **Preferential** | Better wording or convention, but no material accuracy issue. |

### Severity rule

A small typographic difference in ordinary prose may be minor.

A small digit error in a certificate number may be critical.

---

## 23. Pilot Test Design

### Pilot question

Does E7G-T invariant-led QA improve translation review quality?

### Test set

Use 10 documents:

- birth certificate;
- marriage certificate;
- commercial register extract;
- apostille;
- notarial statement;
- court order;
- school certificate;
- medical certificate;
- tax document;
- invoice or contract extract.

### Baseline

Review translations using ordinary bilingual review.

### Intervention

Review translations using the Translation MiniCard and invariant checklist.

### Measures

Track whether reviewers better catch:

- missing names;
- date errors;
- number errors;
- omitted stamps;
- unmarked signatures;
- legal-function mistranslations;
- OCR errors;
- unmarked uncertainty;
- layout loss affecting use;
- certification overclaim.

### Success criterion

The method is useful if it catches more material defects without excessive review overhead.

---

## 24. Relation to Kernel v0.9

This entry operationalises:

- projection is not identity;
- projection loss accounting;
- preservation of invariants;
- source/view distinction;
- boundary discipline;
- bridge mode discipline;
- anti-overclaim posture;
- admissible use;
- stop conditions;
- AI-output projection stack.

It is an application of the kernel, not a replacement for translation expertise.

---

## 25. Stop Conditions

Stop or downgrade the translation when:

- source text is unreadable and uncertainty is not marked;
- identity fields are not verified;
- dates or numbers are not verified;
- stamps/seals/signatures are omitted;
- legal function is unclear;
- OCR risk remains unchecked;
- the target use is unknown;
- certification wording overclaims;
- the recipient requires a different format;
- the translation is being used as proof of authenticity;
- legal advice is being inferred from translation alone.

---

## 26. Productisation Possibilities

This entry can become:

- a translation QA worksheet;
- a certified-style translation checklist;
- an OCR translation review prompt pack;
- an AI-assisted translation QA workflow;
- a legal-document translation review card;
- a bilingual reviewer training module;
- a CAT-tool QA plugin concept;
- a source-target invariant ledger.

The strongest first product is a reusable **Translation Invariant QA Worksheet**.

---

## 27. Closing Rule

Translation is projection.

Accuracy is invariant preservation.

Completeness is boundary coverage.

Fluency is not enough.

Certification is not authentication.

Mark loss when loss matters.

Return to source when reliance matters.
