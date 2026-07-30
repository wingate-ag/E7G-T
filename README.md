# E7G-T

**Unified Geometry-Thinking Kernel**  
**Extensional–Projective–Phase Geometry of Configurations and Time**

E7G-T is a geometry-first modelling language and practical calculus for making **structural and temporal extension, projection, preservation, loss, reconstruction, operational sameness, material boundaries, transition paths, bridge mode, and admissible use** visible.

**Public site:** https://e7-g-t.vercel.app/

It helps users inspect representations and histories before relying on them: AI answers, charts, dashboards, translations, proof sketches, legal summaries, models, reports, workflows, version histories, and decision documents.

## Public landing page

A static public landing page is available in `site/index.html` for Vercel or any static host.

---

## What changed in v0.11

**Version:** v0.11-UC1  
**Status:** unified use-candidate with restored first-class temporal geometry.

The kernel now treats time through the same constitutional disciplines as configurations:

- **temporal extension:** event or temporal locality → interval or history → history family → higher temporal structures;
- **temporal projection:** a history may be reduced to a snapshot, final state, window, sample, branch, trend, or summary;
- **temporal preservation and loss:** order, duration, intermediate states, abandoned branches, recurrence, synchronisation, audit path, and clock uncertainty are made explicit;
- **temporal reconstruction:** the same visible endpoint may remain compatible with several histories;
- **temporal phase:** non-identical histories may count as equivalent under one inquiry and different under another;
- **TD0–TD7:** temporal point, line, surface, body, world-history, variation, transformation, and context roles;
- **TR0–TR6:** retained as derived, non-exclusive temporal-regime profiles rather than the whole temporal layer;
- **joint inference:** a view may determine configuration phase while leaving temporal phase indeterminate;
- **non-commutativity:** structural and temporal projections may produce different results when applied in different orders.

The kernel explicitly distinguishes:

- atemporality or timelessness;
- unbounded temporal extent;
- recurrence or cyclicity;
- completion or closure.

These are modelling distinctions, not claims that physical reality has multiple literal time dimensions.

## Start here

Read the current v0.11-UC1 unified public reference specification:

`E7G-T_Kernel_v0.11_UC1_Unified_Public_Reference_Specification.md`

## Route selection

Use the **extensional–projective route** when the main question concerns construction, order-role placement, viewing, projection, preservation, loss, reconstruction, or bridge discipline.

Use the **temporal-geometry route** when events, intervals, histories, alternative histories, temporal slices, clocks, recurrence, deadlines, completion, or temporal reconstruction affect the claim.

Use the **operational-phase route** when the main question concerns operational equivalence, material phase boundaries, typed transitions, path choice, operation order, or representative dependence.

Use the **combined route** when a structural or temporal view is being used to infer operational status.

## Core integration rules

For a configuration view `v`, projection or viewing map `π`, reconstruction fibre `Recπ(v)`, and phase criterion `Q`:

```text
PhaseCandidatesQ(v) = { [Γ]Q | Γ ∈ Recπ(v) }
```

For a temporal view `vΘ`, temporal projection `πΘ`, temporal reconstruction fibre `RecΘ,π(vΘ)`, and temporal-phase criterion `QΘ`:

```text
TemporalPhaseCandidatesQΘ(vΘ)
  = { [θ]QΘ | θ ∈ RecΘ,π(vΘ) }
```

- one supported candidate may permit classification;
- several candidates require abstention, another view, or source/history return;
- no admitted candidates require model, boundary, or criterion repair;
- one configuration phase candidate does not imply one temporal phase or one unique history.

## Project posture

E7G-T is not established mathematics as a whole, empirical physics, a proof system, a Theory of Everything, an authority decision, or a replacement for mature domain methods.

Its proper role is to frame, inspect, compare, classify, navigate, document, teach, bridge, lint, and route reasoning towards the next responsible move.

## Repository status

The v0.10 public specification is retained as predecessor material. The previous v0.9 RC1 materials remain under [`release_0.9RC1/`](release_0.9RC1/) and are no longer the active specification. See [Legacy Materials](legacy/README.md).

## Current validation priority

Do not expand the theory merely by adding terminology. Test whether the unified kernel changes a real next move.

Recommended cases:

- identical final document states produced by different audited and unaudited histories;
- a final-state view that determines configuration phase but spans several temporal phases;
- structural and temporal projections that fail to commute;
- AI answer whose source ambiguity spans different reliance phases;
- translation edit that may preserve wording while changing legal or operational force;
- dashboard or status display used to infer readiness;
- software refactoring assessed for behavioural equivalence;
- proof-path state classified from an incomplete interface view.

## Author and citation

E7G-T was created by **Alexander Gregory Wingate**.

Citation metadata is provided in [`CITATION.cff`](CITATION.cff). GitHub's **Cite this repository** function can generate a formatted citation from that file.

## Licence

Copyright © 2026 Alexander Gregory Wingate.

Except where otherwise noted, the original specifications, documentation, worksheets, pilot protocols, and other textual materials in this repository are licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/) (**CC BY-SA 4.0**).

When reusing or adapting the material:

- credit **Alexander Gregory Wingate** as creator;
- identify the work as **E7G-T** and link to this repository where reasonably practicable;
- indicate whether changes were made; and
- distribute adaptations under CC BY-SA 4.0 or another BY-SA-compatible licence permitted by the licence.

See [`LICENSE`](LICENSE) for the complete legal terms. Third-party material, if any, remains subject to its own rights and licence notices.
