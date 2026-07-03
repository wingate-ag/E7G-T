# E7G-T Application Atlas — Entry 003

# Legal / Administrative Summary as Projection

**Atlas ID:** APP-003  
**Kernel compatibility:** E7G-T v0.9 draft  
**Builds on:** APP-001 — AI Output as Projection; PG-002 Worksheet — AI Answer Source-Return Review  
**Status:** pilot-ready application entry  
**Date:** 2026-07-01  
**Bridge mode:** legal/administrative-operational; not legal advice  
**Primary use:** legal/administrative summary review, immigration/admin document review, eligibility-check discipline, AI legal-summary linting, source-return control

---

## 1. Entry Purpose

This Application Atlas entry applies E7G-T v0.9 to legal and administrative summaries.

The basic claim is:

> A legal or administrative summary is a projection of rules, facts, documents, and procedures. It is not the authority, not the full case, and not a final decision.

This entry is jurisdiction-neutral. It does not provide legal advice. It provides a method for reviewing whether a legal or administrative summary is being overread.

It is designed for:

- immigration and residence-path summaries;
- administrative checklists;
- eligibility overviews;
- document-request summaries;
- official-letter summaries;
- court or notarial document summaries;
- certified-style translation review;
- AI-generated legal/admin explanations;
- internal case-preparation notes.

---

## 2. Entity of Concern

**Entity:** legal or administrative summary.

This may be:

- an AI-generated explanation;
- a lawyer’s short orientation note;
- a government-page summary;
- a translator’s documentary note;
- a consultant checklist;
- an internal case memo;
- a residence-permit eligibility overview;
- a benefits/admin-process explanation;
- a court or registry extract summary;
- a summary of an official letter.

The entity is not the law itself.

It is a projected view of a more complex legal/administrative source stack.

---

## 3. Core Source / View Distinction

| Layer | Description |
|---|---|
| **Authority layer** | Law, regulation, official guidance, court/agency practice, authoritative form instructions, procedural rules. |
| **Case-facts layer** | Person, dates, status, income, residence, family composition, documents, deadlines, prior decisions. |
| **Document layer** | Passports, certificates, permits, contracts, invoices, letters, translations, apostilles, stamps, signatures. |
| **Procedure layer** | Application route, office, timing, appointment, evidence, fees, appeals, renewals, waiting periods. |
| **Summary layer** | The visible explanation, checklist, memo, AI answer, or consultant note. |
| **Decision layer** | Actual authority decision, acceptance, refusal, request for evidence, court outcome, or administrative act. |

### Core E7G-T repair

Do not ask only:

> “Does the summary sound plausible?”

Ask:

> “What authority, facts, documents, and procedure does this summary project from, and what reliance can it support?”

---

## 4. Placement

### Compact placement

```text
LegalAdminSummary : D2/D7 @ TR1 / CaseReviewContext
```

### Meaning

The summary is treated as:

- **D2** because it appears as visible text, checklist, table, email, memo, or AI answer;
- **D7** because it is governed by jurisdiction, purpose, authority, case facts, procedure, and admissible use;
- **TR1** because it is read at a local review moment;
- **CaseReviewContext** because its meaning depends on the actual case boundary.

### Source stack placement

```text
AuthorityStack + CaseFacts + Documents + Procedure
  : D4/D6/D7 @ TR1-TR6 / JurisdictionContext
  --π_Summary^{4/6/7→2}-->
LegalAdminSummary : D2/D7 @ TR1 / CaseReviewContext
[preserves: selected rule/fact/procedure structure;
 loses: exceptions, authority hierarchy, factual uncertainty, timing, discretion, document defects;
 use: orientation, checklist, source-return trigger, case-preparation aid]
```

---

## 5. Projection Account

A legal/administrative summary may preserve:

- broad route structure;
- document checklist;
- key eligibility elements;
- relevant dates;
- procedural steps;
- official terminology;
- decision options;
- deadlines;
- risk flags;
- missing evidence;
- case narrative;
- translation/documentary invariants;
- authority references if cited.

It may lose:

- exact legal wording;
- authority hierarchy;
- currentness;
- jurisdiction-specific exceptions;
- agency practice;
- discretion;
- case-law nuance;
- evidentiary burden;
- document authenticity risk;
- translation defects;
- OCR uncertainty;
- family-composition complications;
- timing constraints;
- appeal/renewal consequences;
- hidden assumptions;
- procedural discretion;
- actual decision authority.

It may distort:

- eligibility certainty;
- deadline urgency;
- document sufficiency;
- income or status thresholds;
- family-member inclusion;
- translation reliability;
- official acceptance likelihood;
- risk level;
- legal force of unofficial sources.

---

## 6. Preservation / Loss Ledger

| Question | Review instruction |
|---|---|
| What authority is projected? | Identify the law, official guidance, form instruction, letter, or decision source. |
| What facts are projected? | Identify the personal/case facts used by the summary. |
| What documents are projected? | Identify documents, translations, stamps, signatures, dates, names, numbers. |
| What procedure is projected? | Identify office, route, deadline, appointment, filing, evidence, fee, appeal, or renewal path. |
| What is preserved? | Name the rule/fact/document/procedure elements the summary carries. |
| What is lost? | Name exceptions, missing evidence, source limits, uncertainties, timing, discretion, and authority gaps. |
| What is the strongest admissible use? | Orientation, checklist, draft, source-return prompt, case-preparation note, or final reviewed position. |
| What is blocked? | Treating summary as authority, decision, legal advice, or complete case review. |

---

## 7. Bridge Mode

Legal/admin summaries usually require a stronger bridge than ordinary interpretation.

| Bridge mode | Use |
|---|---|
| **orientation** | General non-reliance explanation of possible route or issue. |
| **documentary** | Source-document or translation-linked summary. |
| **official-source-linked** | Summary tied to an official source, form, or authority notice. |
| **case-fact-linked** | Summary connected to declared facts of a person/case. |
| **professional-review-needed** | High-risk or ambiguous case requiring qualified review. |
| **authority-decision** | Actual decision by competent authority; not produced by the summary itself. |

### Bridge rule

A legal/admin summary cannot support a stronger claim than its weakest link among:

```text
authority source + currentness + case facts + documents + procedure + reviewer competence
```

---

## 8. Claim-Strength Ladder for Legal/Admin Summaries

1. **Informal orientation** — useful for understanding possible route.
2. **Checklist draft** — useful for collecting documents.
3. **Source-linked summary** — tied to an identified source.
4. **Case-fact-linked note** — tied to declared facts.
5. **Reviewed case memo** — reviewed by competent person under defined scope.
6. **Filing-ready position** — suitable for application preparation after checks.
7. **Authority-issued decision** — issued by competent authority.
8. **Final/legal reliance** — depends on jurisdiction, review, deadlines, appeal status, and professional context.

### Upgrade rule

Do not upgrade from orientation to reliance without source return and case-fact verification.

---

## 9. Legal/Admin Summary MiniCard

```yaml
id: APP-003-legal-admin-summary-review
entity: legal/admin summary
plainMeaning: A visible explanation or checklist projecting authority, facts, documents, and procedure.
placement: LegalAdminSummary : D2/D7 @ TR1 / CaseReviewContext
sourceStack:
  authority:
    - law/regulation/official guidance/form/letter/decision
  caseFacts:
    - person/status/dates/income/family/residence/deadlines
  documents:
    - certificates/passports/permits/translations/stamps/signatures
  procedure:
    - route/office/deadline/appointment/fee/evidence/appeal/renewal
boundary:
  includes:
    - stated facts
    - cited sources
    - listed documents
    - declared jurisdiction
    - stated procedural route
  excludes:
    - unstated facts
    - uncited exceptions
    - agency discretion
    - expired/currently changed rules unless verified
preserved:
  - selected rule elements
  - selected facts
  - selected document requirements
  - selected procedural steps
lost:
  - exceptions
  - currentness uncertainty
  - factual gaps
  - document defects
  - discretionary practice
  - legal nuance
distortionRisk:
  - plausible summary mistaken for authority
  - eligibility overstated
  - checklist mistaken for sufficiency
  - old rule treated as current
  - translation/OCR defect ignored
reconstructionStatus: partial; requires authority/fact/document/procedure return
bridgeMode: orientation unless official-source-linked and case-fact-checked
admissibleUse:
  - orientation
  - checklist
  - case-preparation note
  - source-return guide
nonAdmissibleUse:
  - final legal reliance without review
  - claim of eligibility without current source and fact verification
  - filing without document/procedure check
nextMove: return to authority, facts, documents, and procedure
blockedOverread: summary is not authority
```

---

## 10. FullCard Template

```yaml
id:
matter:
jurisdiction:
authoritySource:
  title:
  date:
  linkOrReference:
  currentnessChecked:
caseFacts:
  personStatus:
  residence:
  nationality:
  familyComposition:
  income:
  deadlines:
  priorDecisions:
documents:
  - document:
    date:
    issuer:
    names:
    numbers:
    translationNeeded:
    defectRisk:
procedure:
  route:
  office:
  form:
  appointment:
  fee:
  evidence:
  deadline:
  appealOrRenewal:
summaryText:
projectionAccount:
preserved:
lost:
distortionRisk:
claimStrength:
bridgeMode:
weakestLink:
sourceReturnNeeded:
expertReviewNeeded:
admissibleUse:
nonAdmissibleUse:
stopCondition:
nextMove:
reviewerNotes:
```

---

## 11. Common Failure Modes

### 11.1 Summary mistaken for authority

A memo, AI answer, or checklist is treated as if it were the law or official decision.

**Blocked overread:** summary is not authority.

### 11.2 Eligibility overstated

The summary says a person “qualifies” when only a possible route has been identified.

**Blocked overread:** possible route is not eligibility decision.

### 11.3 Checklist mistaken for sufficiency

The checklist lists documents, but sufficiency depends on content, dates, translations, form, authority practice, and case facts.

**Blocked overread:** checklist is not acceptance.

### 11.4 Currentness failure

A rule, threshold, office practice, fee, or deadline may have changed.

**Blocked overread:** old rule is not current authority.

### 11.5 Case-fact drift

The summary relies on facts that are incomplete, wrong, outdated, or mismatched.

**Blocked overread:** changed facts change the claim.

### 11.6 Jurisdiction drift

A rule from one country, state, region, office, or procedure is applied to another.

**Blocked overread:** similar procedure is not same jurisdiction.

### 11.7 Document defect hidden

Names, dates, signatures, stamps, seals, translations, apostilles, or copies may be defective.

**Blocked overread:** document listed is not document accepted.

### 11.8 Translation overread

A translated document is treated as source identity.

**Blocked overread:** translation is projection, not source identity.

### 11.9 AI legal fluency

AI writes confident legal language without authority, date, jurisdiction, or facts.

**Blocked overread:** AI legal fluency is not legal authority.

### 11.10 Authority decision confused with prediction

A summary predicts likely outcome, but only the competent authority decides.

**Blocked overread:** prediction is not decision.

---

## 12. Review Workflow

### Step 1 — Place the summary

```text
LegalAdminSummary : D2/D7 @ TR1 / CaseReviewContext
```

### Step 2 — Identify the claim

Is the summary claiming:

- possible route;
- eligibility;
- document sufficiency;
- deadline;
- procedural step;
- legal right;
- risk;
- authority decision;
- translation/documentary adequacy?

### Step 3 — Return to authority

Identify the source:

- law/regulation;
- official website;
- official form;
- authority letter;
- decision;
- court/agency guidance;
- professional review.

### Step 4 — Return to facts

Check:

- person;
- status;
- dates;
- residence;
- nationality;
- income;
- family composition;
- prior decisions;
- deadlines.

### Step 5 — Return to documents

Check:

- issuer;
- date;
- names;
- numbers;
- stamps;
- signatures;
- apostille/legalisation;
- translation;
- copy/original status;
- document defects.

### Step 6 — Return to procedure

Check:

- office;
- route;
- filing mode;
- form;
- appointment;
- fee;
- evidence;
- timing;
- appeal/renewal path.

### Step 7 — Assign claim strength

Use the weakest-link rule.

### Step 8 — State next move

Examples:

- keep as orientation;
- verify official source;
- update current rule;
- correct case facts;
- request missing document;
- perform translation QA;
- ask qualified reviewer;
- downgrade eligibility wording;
- stop.

---

## 13. Worked Example — Residence Route Summary

AI/legal summary:

> “You can apply for this residence permit because your income is sufficient.”

E7G-T review:

```text
Entity: residence-route summary
Placement: LegalAdminSummary : D2/D7 @ TR1 / CaseReviewContext
Claim type: eligibility / income sufficiency
Authority needed: current official rule or law
Facts needed: income amount, family size, residence status, dates, source of income
Documents needed: income evidence, passports, residence documents, family documents
Procedure needed: office, form, filing route, deadline
Risk: possible route overstated as qualification
Bridge mode: orientation unless authority/facts/documents/procedure checked
Blocked overread: possible route is not authority decision
Next move: verify current threshold and case facts; downgrade wording
```

Safer wording:

> “This may be a possible route if the current rule, income evidence, family composition, and procedural requirements match. It requires official-source and case-fact verification.”

---

## 14. Worked Example — Official Letter Summary

Summary:

> “The authority is asking for missing documents.”

E7G-T review:

```text
Entity: official-letter summary
Source: authority letter
Preserved: general request for documents
Lost risk: exact deadline, exact document names, legal consequence, delivery method, appeal rights
Required move: source-return to letter text
Blocked overread: general summary is not the letter
```

Safer wording:

> “The letter appears to request additional documents. The exact list, deadline, and consequences must be checked against the letter itself.”

---

## 15. Worked Example — Certified-Style Translation Note

Summary:

> “The translation is acceptable for filing.”

E7G-T review:

```text
Entity: translation/filing adequacy claim
Source stack: source document + target translation + filing authority requirement
Risk: translation quality mistaken for authority acceptance
Required checks: names, dates, numbers, stamps, signatures, seals, page structure, certification wording, authority requirements
Blocked overread: translation QA is not authority acceptance
```

Safer wording:

> “The translation may be suitable for filing after source-target QA and confirmation of the receiving authority’s requirements.”

---

## 16. Legal/Admin OneLine Templates

### Orientation summary

```text
E7-OneLine: This legal/admin summary is treated as a D2/D7 projection of authority, facts, documents, and procedure under case-review context; admissible move: use as orientation and verify source stack; blocked overread: summary is not authority.
```

### Eligibility claim

```text
E7-OneLine: This eligibility claim is treated as a case-fact-linked projection requiring current authority and document verification; admissible move: downgrade to possible route until checked; blocked overread: possible route is not decision.
```

### Document checklist

```text
E7-OneLine: This document checklist is treated as a D2 projection of procedural requirements; admissible move: verify exact authority requirements and document defects; blocked overread: checklist is not sufficiency.
```

### Official letter summary

```text
E7-OneLine: This letter summary is treated as a projection of an authority text; admissible move: return to exact wording, deadlines, and consequences; blocked overread: summary is not the letter.
```

---

## 17. AI-Assisted Legal/Admin Review

AI can help:

- structure facts;
- identify missing documents;
- draft questions;
- summarise official letters;
- create checklists;
- compare versions;
- flag current-source needs;
- downgrade risky wording.

AI must not be treated as:

- legal authority;
- current law by default;
- final eligibility decision;
- expert reviewer;
- authority decision-maker;
- substitute for official source or qualified advice.

### AI legal/admin placement

```text
AILegalAdminAnswer : D2/D7 @ TR1 / UserQueryContext
```

### Projection stack

```text
Authority/Facts/Documents/Procedure
  --π_Summary-->
LegalAdminSummary
  --π_AIInterpretation-->
AIAnswer
```

Loss accumulates.

### Blocked overread

```text
AI interpretation of legal/admin summary is not authority.
```

---

## 18. Pilot Test Design

### Pilot question

Does APP-003 reduce overreliance on legal/admin summaries?

### Test set

Use 10–20 summaries across:

- residence/immigration route explanation;
- official letter summary;
- document checklist;
- eligibility claim;
- deadline explanation;
- translation filing note;
- benefits/admin procedure summary;
- AI-generated legal/admin answer.

### Baseline

Review summaries normally.

### Intervention

Review with APP-003 MiniCard or workflow.

### Measures

Track whether reviewers better identify:

- missing authority source;
- outdated rule risk;
- missing facts;
- document defects;
- translation risks;
- jurisdiction drift;
- deadline risks;
- overconfident eligibility claims;
- need for official-source return;
- need for qualified review.

### Success criterion

The entry is useful if it reduces unsupported reliance and produces clearer next actions without excessive overhead.

---

## 19. Productisation Possibilities

APP-003 could become:

- legal/admin summary linter;
- immigration-path checklist;
- official-letter review worksheet;
- document-request tracker;
- translation filing-readiness checklist;
- AI legal-answer review prompt pack;
- case-preparation intake form;
- authority-source return checklist.

Most realistic first product:

> AI legal/admin answer review worksheet.

---

## 20. Stop Conditions

Stop or downgrade when:

- no authority source is identified;
- currentness is unknown;
- jurisdiction is unclear;
- facts are incomplete;
- document authenticity or translation quality is uncertain;
- deadline is unclear;
- official letter wording has not been checked;
- eligibility is stated without source and facts;
- AI gives confident legal/admin wording without authority;
- a filing or appeal deadline may be affected;
- reliance could affect legal status, finances, rights, health, safety, or family situation.

---

## 21. Relation to Kernel v0.9

This Application Atlas entry operationalises:

- D2/D7 placement;
- source/view discipline;
- projection loss;
- reconstruction status;
- weakest-link bridge rule;
- claim-strength ladder;
- anti-replacement rule;
- source-return discipline;
- stop conditions.

It does not replace legal or administrative expertise.

---

## 22. Closing Rule

A summary is not the authority.

A checklist is not sufficiency.

A possible route is not eligibility.

A prediction is not a decision.

AI legal fluency is not legal authority.

Return to source when reliance matters.
