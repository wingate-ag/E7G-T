# PILOT-001 — Unified Projection and Phase Review

## Purpose

Test whether the v0.10 unified kernel catches material risks or clarifies actions that the v0.9 projection-only review does not.

## Cases

Run at least five cases:

1. AI answer used for a consequential recommendation;
2. translation containing a modal, legal-force, identity, or documentary-status choice;
3. dashboard or status tile used to infer readiness or health;
4. software change claimed to preserve behaviour;
5. proof, workflow, or administrative interface used to infer completion.

## Comparison design

For each case perform:

### Pass A — ordinary review

Use the reviewer’s normal method.

### Pass B — v0.9-style projection review

Record entity, view, preserved structure, lost structure, reconstruction status, bridge mode, and next move.

### Pass C — v0.10 combined review

Add inquiry, admitted configurations, phase criterion, phase candidates, typed change, boundary status, representative dependence, and path/order checks.

## Outcome measures

Record whether Pass C:

- found an additional materially different source configuration;
- changed the operational classification;
- prevented classification from an insufficient view;
- identified a phase-boundary crossing missed by earlier review;
- exposed representative-dependent outcomes;
- changed the recommended next move;
- added burden without changing the decision.

## Success criterion

The phase layer is practically justified when it changes or materially strengthens the next responsible move in cases where operational equivalence or boundary crossing genuinely matters.

It is not justified when it merely renames an ordinary correction, direct invariant check, or source-return requirement.

## Report template

```yaml
caseId:
domain:
ordinaryReviewResult:
projectionReviewResult:
unifiedReviewResult:
additionalPhaseFinding:
decisionChanged: yes | no
riskCaught:
extraBurden:
reviewerAssessment:
recommendedKernelChange:
```
