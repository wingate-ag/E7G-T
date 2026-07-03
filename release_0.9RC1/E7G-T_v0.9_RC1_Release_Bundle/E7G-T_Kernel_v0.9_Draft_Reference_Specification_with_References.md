# E7G-T Kernel v0.9 Draft — Reference Specification

**Version:** 0.9 draft  
**Date:** 2026-06-29  
**Status:** Reference-style kernel candidate  
**Source:** Extracted from the foundations draft and the v0.8 kernel / practical calculus layer.

---

## 0. Status and Use Posture

E7G-T v0.9 is a geometry-first modelling language and practical calculus under development.

It is **not** established mathematics.  
It is **not** empirical physics.  
It is **not** a proof system.  
It is **not** a replacement for mature formal, empirical, legal, medical, engineering, translation, statistical, or domain-specific methods.  
It is **not** a Theory of Everything.

Its purpose is to make **extension, projection, boundary, context, preservation, loss, reconstruction, bridge mode, and admissible use** more visible.

### Primary use

Use E7G-T when a claim, model, proof, measurement, dashboard, AI answer, translation, diagram, software trace, or speculative bridge may be confusing:

- source with view;
- slice with whole;
- metaphor with proof;
- formal analogy with empirical claim;
- model with reality;
- interface fluency with evidence;
- proof path with proof.

---

## 1. Core Question

> What do I do next with this concrete object, claim, proof, model, output, observation, system, or representation?

---

## 2. Core Discipline

Before applying an operation, declare as much of the following as the use requires:

- entity of concern;
- order profile;
- temporal regime;
- context;
- boundary;
- operation;
- preservation/loss if projection is involved;
- transformation class if invariance is claimed;
- reconstruction status if source claims are involved;
- bridge mode if domains are crossed;
- admissible use;
- stop condition.

### Rule

Use the smallest level that changes the next modelling move without hiding risk.

---

## 3. D-Order Table

| Order | Working role |
|---|---|
| **D0** | Point-locality, local mark, scalar output, trace, pixel, accepted state, result. |
| **D1** | Line-extension, path, interval, sequence, procedure, timeline segment, proof-step path. |
| **D2** | Surface-extension, field, map, text surface, diagram, dashboard, screen, interface, visible proof text. |
| **D3** | Form-extension, object, body, artefact, local system, product, structured proof artefact when treated formally. |
| **D4** | Duration-extension, history, process, world-form, version history, event sequence, lived development. |
| **D5** | Variation-extension, possibility field, branch space, option set, design space, model alternatives, proof-search space. |
| **D6** | Transformation-extension, rule-space, operator, law, tactic, function, protocol, method, verification rule, permitted transformation class. |
| **D7** | Context-extension, interpretation frame, measurement context, user purpose, publication frame, bridge governance, admissible-use frame. |

### D-order rule

D0–D7 are **modelling orders**, not literal physical dimensions by default.

---

## 4. Temporal Regime Table

| Regime | Working role |
|---|---|
| **TR0** | No-time / atemporal treatment. |
| **TR1** | Local-time / local ordered sequence. |
| **TR2** | Shared-time / coordinated time between multiple local sequences. |
| **TR3** | Branching-time / alternatives, forecasts, options, proof search, scenario space. |
| **TR4** | Cyclic-time / recurrence, rhythm, periodic structure, iteration. |
| **TR5** | Super-time / meta-time / time about time / model-time governing object-time. |
| **TR6** | Timeless-completion / closed whole under a declared closure context. |

### Temporal rule

Temporal regimes are **modelling declarations**, not claims about ultimate physical time by default.

---

## 5. Primitive Moves

### 1. Place

Declare the entity’s order, temporal regime, and context.

```text
X : Dn @ TRi / C
```

### 2. Bound

Declare the operational boundary.

```text
∂X = B
```

### 3. Incide

Declare the relation between entities.

```text
A ⋈_C B
```

### 4. Extend

Move toward richer structure by adding declared extension.

```text
X ↑ n
```

### 5. Slice

Select a local or contextual view.

```text
S_C^s(X)
```

### 6. Project

Render a lower-order view from a richer source or candidate source.

```text
π_C^{n→k}(X) = Y
```

### 7. Preserve/Lose

Name what survives and what does not survive a projection or transformation.

### 8. Transform

Apply a declared rule-space.

```text
τ_T(X) = Y
```

### 9. Reconstruct

Attempt source recovery from a projection or trace, usually set-valued or tentative.

```text
ρ_C(Y) ⇒ {X_i}
```

### 10. Bridge/Stop

Declare bridge mode or stop the claim.

```text
β_M^{A↔B}
Stop(reason)
```

---

## 6. Practical Laws

### Law 1 — Typing Before Operation

Place the entity before operating on it.

### Law 2 — Extension Is Not Projection

Building richer structure is not the same as rendering a lower-order view.

### Law 3 — Projection Is Not Reconstruction

A view of a source is not a recovery of the source.

### Law 4 — Projection Loss Accumulates

Loss in a projection stack cannot be silently regained.

### Law 5 — Slice and Projection Need Not Commute

Slicing before projection and projecting before slicing may produce different results.

### Law 6 — Boundary Is Contextual But Not Arbitrary

Boundary may vary by use, but it must match the claim.

### Law 7 — Invariance Requires a Transformation Class

No invariant claim is complete without declaring what transformations it survives.

### Law 8 — Bridge Claims Inherit the Weakest Link

A bridge cannot support a stronger claim than its least-supported component.

### Law 9 — Empirical Language Requires Empirical Bridge

Reality-facing claims require measurement, prediction, falsification, and evidence path.

### Law 10 — The Next Move Is the Practical Test

The value of the model is shown by the next admissible action it clarifies.

---

## 7. Bridge Modes

| Mode | Use |
|---|---|
| **none** | No bridge is claimed. |
| **contemplative-what-if** | Used for imaginative, reflective, fictional, or exploratory thinking. |
| **philosophical-interpretation** | Used for conceptual interpretation without formal or empirical force. |
| **formal-analogy** | Used where one structure resembles another under declared mapping, but without proof of identity or empirical support. |
| **formal-compatibility** | Used where the structure can be mapped into or compared with a recognised formal substrate under declared definitions. |
| **empirical-testable** | Used only where there is a standard substrate, observation protocol, measurement map, prediction or constraint, falsification condition, and evidence path. |

### Bridge rule

Bridge mode must be declared before claim strength is raised.

---

## 8. Claim-Strength Ladder

1. intuition
2. metaphor
3. contemplative-what-if
4. philosophical-interpretation
5. formal-analogy
6. formal-compatibility
7. formal proof
8. empirical-testable proposal
9. empirically supported model
10. validated operational method

### Upgrade rule

Do not upgrade claim strength without completing the required bridge, proof, test, or validation.

---

## 9. Practical Levels

### Level 1 — OneLine

Use for quick placement and overread blocking.

```text
E7-OneLine: X is treated as [order/role] under [context]; admissible move: [next move]; blocked overread: [one phrase].
```

### Level 2 — MiniCard

Use for modelling a claim or artefact before relying on it.

Fields:

- entity;
- plain meaning;
- placement;
- boundary;
- projection account;
- preserved;
- lost;
- invariant;
- reconstruction status;
- bridge mode;
- next move;
- blocked overread.

### Level 3 — FullCard

Use for reliance, publication, bridge claims, proof review, empirical-facing statements, or operational decisions.

Fields:

- entity of concern;
- claim;
- order profile;
- temporal regime;
- context;
- boundary;
- extension account;
- projection path;
- preservation/loss;
- transformation class;
- invariant;
- reconstruction status;
- bridge mode;
- weakest link;
- admissible use;
- stop condition.

---

## 10. Notation Normalisation

### Placement

```text
X : Dn @ TRi / C
```

### Projection

```text
π_C^{n→k}(X) = Y
```

### Readable projection

```text
X : Dn @ TRi / C  --π_C^{n→k}-->  Y : Dk @ TRj / C'
```

### Full projection

```text
X : Dn @ TRi / C  --π_C^{n→k}-->  Y : Dk @ TRj / C'  [preserves: P; loses: L; use: U]
```

### Candidate reconstruction

```text
ρ_C^{k→n}(Y) ⇝ X?
```

### Set-valued reconstruction

```text
ρ_C(Y) ⇒ {X_i}
```

### Transformation

```text
τ_T(X) = Y
```

### Invariant

```text
Inv_T(X) = I
```

### Bridge

```text
β_M^{A↔B}
```

### Stop

```text
Stop(reason)
```

### Notation rule

Notation records discipline. It does not create discipline.

---

## 11. Proof-of-Path Kernel

Proof-of-Path is a structured account of the admissible route by which a claim, model, proof, or output moves from entity placement through transformations, projections, checks, bridges, and stop conditions to a stated reliance tier.

It is not a replacement for proof.

### ProofOfPathCard fields

- id;
- claim;
- entity;
- substrate;
- assumptions;
- context;
- placement;
- boundary;
- definitions;
- transformations;
- projection events;
- preserved invariants;
- losses;
- checks;
- unresolved obligations;
- bridge mode;
- reliance tier;
- stop condition;
- source links.

### Rule

A Proof-of-Path can include a formal proof, but it does not become a formal proof merely by documenting a path.

---

## 12. Reality Bridge Kernel

Reality-facing language requires Reality Bridge Discipline.

### RealityBridgeCard fields

- claim;
- source domain;
- target domain;
- bridge mode;
- standard substrate;
- observation protocol;
- measurement map;
- prediction or constraint;
- falsification condition;
- evidence path;
- weakest link;
- admissible use;
- non-admissible use;
- stop condition.

### Rule

Empirical-testable is the only bridge mode that can support empirical claims.

---

## 13. Formal Neighbourhood Kernel

### FormalNeighbourhoodCard fields

- field;
- E7G-T element;
- resemblance;
- established tool;
- current bridge mode;
- what E7G-T can learn;
- what E7G-T must not claim;
- possible formalisation path;
- stop condition.

### Rule

Neighbourhood is not identity.

---

## 14. Failure-Mode Checklist

Before relying on an E7G-T account, check for:

- false identity;
- false reconstruction;
- hidden boundary shift;
- undeclared context;
- missing temporal regime;
- projection loss denial;
- slice mistaken for whole;
- invariant without transformation class;
- bridge inflation;
- formal-neighbourhood overclaim;
- empirical language without empirical bridge;
- proof text mistaken for proof object;
- AI fluency mistaken for evidence;
- interface accepted-state mistaken for explanation;
- replacement of mature tools;
- missing stop condition.

---

## 15. Anti-Replacement Rule

E7G-T does not replace a mature formal, empirical, operational, legal, medical, engineering, translation, statistical, or domain-specific discipline where that discipline already has stronger tools.

E7G-T may help frame, inspect, document, teach, bridge, or lint reasoning around such tools. It may not bypass them.

---

## 16. Public-Use Cautions

When presenting E7G-T publicly:

- Do not call it established mathematics.
- Do not call it new physics.
- Do not claim that D0–D7 are literal physical dimensions.
- Do not claim that holographic reading proves a holographic universe.
- Do not treat contemplative usefulness as empirical evidence.
- Do not treat metaphor as proof.
- Do not treat Proof-of-Path documentation as formal proof.
- Do not use E7G-T to avoid expert review.

### Preferred public sentence

> E7G-T is a geometry-first modelling language and practical calculus for making projection, loss, reconstruction, bridge mode, and admissible use visible.

---

## 17. Minimal Examples

### AI answer

```text
E7-OneLine: An AI answer is treated as a D2/D7 textual projection under user-query context; admissible move: verify source and bridge mode; blocked overread: fluency is not evidence.
```

### Business dashboard

```text
E7-OneLine: A dashboard is treated as a D2 projection of a D4/D5 business system under reporting context; admissible move: inspect preserved metrics and lost causes; blocked overread: the chart is not the business.
```

### Translation

```text
E7-OneLine: A translation is treated as a target-language projection of a source text under purpose context; admissible move: identify preserved legal/semantic invariants; blocked overread: translation is not source identity.
```

### Proof assistant session

```text
E7-OneLine: A proof assistant session is treated as a D2/D7 interface projection of D6 formal rule work under kernel context; admissible move: inspect assumptions, proof state, elaboration, and accepted check; blocked overread: accepted interface state is not human explanation.
```

### Speculative physics analogy

```text
E7-OneLine: Quantum measurement-as-projection is treated as formal analogy unless empirical-testable bridge is declared; admissible move: state preservation/loss and stop condition; blocked overread: analogy is not new physics.
```

---

## 18. v0.9 Maturity Statement

E7G-T v0.9 is mature enough to support disciplined modelling, practical analysis, educational framing, proof-path documentation, AI-output review, translation/accountability framing, dashboard critique, and bridge-mode control.

It is not mature enough to support claims of new mathematics, new physics, empirical confirmation, or replacement of expert methods.

The next maturity step is v1.0 only after:

- terms are stabilised;
- notation is normalised;
- public examples are tested;
- formal-neighbourhood sources are added;
- bridge-mode rules are enforced consistently;
- at least one Application Atlas is drafted;
- at least one proof-assistant or software-interface experiment is specified.

---

## 19. Next Work

1. Convert this draft into a polished standalone v0.9 Markdown kernel.
2. Add source-backed references only where the kernel touches established fields.
3. Draft the first Application Atlas entry: AI output as projection.
4. Draft the first Proof-of-Path prototype: proof assistant session as accountable path.
5. Draft the first practical guide chapter: The chart is not the business.

---



---

## 20. Selected Public Reference Anchors

### 20.1 Purpose of this reference layer

This section provides public anchors for the established fields that E7G-T stands near, borrows caution from, or may later interface with.

These references do **not** prove E7G-T. They are not cited as authorities for E7G-T itself. They are included to prevent vocabulary capture and to make clear where established disciplines already have stronger tools.

Use these references to support public-facing positioning, formal-neighbourhood discipline, and future bridge work.

### 20.2 Geometry and projection

**Projective geometry**

- Eric W. Weisstein, “Projective Geometry,” *MathWorld — A Wolfram Resource*.  
  <https://mathworld.wolfram.com/ProjectiveGeometry.html>

E7G-T use:

Projective geometry is an established mathematical field dealing with properties and invariants under projection. E7G-T uses “projection” more broadly as a modelling term, so it must not imply projective-geometric formalism unless a formal substrate is declared.

Kernel caution:

Do not call an E7G-T projection a projective-geometric projection unless the mathematical structure is actually defined.

### 20.3 Category theory

**Category theory**

- Jean-Pierre Marquis, “Category Theory,” *The Stanford Encyclopedia of Philosophy*.  
  <https://plato.stanford.edu/entries/category-theory/>

E7G-T use:

Category theory is a formal mathematical language of structures and structure-preserving relations. E7G-T may stand near category-theoretic thinking when it speaks about arrows, transformations, bridges, and diagrams.

Kernel caution:

E7G-T arrows are not automatically morphisms. Projection stacks are not automatically commutative diagrams. Bridges are not automatically functors.

### 20.4 Type theory

**Type theory**

- Thierry Coquand, “Type Theory,” *The Stanford Encyclopedia of Philosophy*.  
  <https://plato.stanford.edu/entries/type-theory/>

E7G-T use:

Type theory is relevant to E7G-T’s placement discipline, proof-assistant ambitions, and “typing before operation” law.

Kernel caution:

`X : Dn @ TRi / C` is a modelling placement, not a formal type judgement unless a formal type-theoretic substrate is explicitly defined.

### 20.5 Proof assistants and Lean

**Lean proof assistant**

- *The Lean Language Reference*.  
  <https://lean-lang.org/doc/reference/latest/>

- Lean Programming Language official site.  
  <https://lean-lang.org/>

E7G-T use:

Lean is relevant to Proof-of-Path, proof-state slicing, tactic-as-transformation, and interface-as-projection work.

Kernel caution:

Proof-of-Path can document proof movement, but Lean or another proof assistant supplies the formal checking substrate. A Proof-of-Path record is not itself a formal proof.

### 20.6 Diagrammatic reasoning

**Diagrams and diagrammatical reasoning**

- Sun-Joo Shin, Oliver Lemon, and Mateja Jamnik, “Diagrams and Diagrammatical Reasoning,” *The Stanford Encyclopedia of Philosophy*.  
  <https://plato.stanford.edu/entries/diagrams/>

E7G-T use:

Diagrammatic reasoning is relevant to E7G-T’s treatment of diagrams as projections that may carry reasoning structure.

Kernel caution:

A diagram may support reasoning, explanation, or even formal work in a declared diagrammatic system. But an informal diagram is not automatically proof.

### 20.7 Models and scientific representation

**Models in science**

- Roman Frigg and Stephan Hartmann, “Models in Science,” *The Stanford Encyclopedia of Philosophy*.  
  <https://plato.stanford.edu/entries/models-science/>

**Scientific representation**

- “Scientific Representation,” *The Stanford Encyclopedia of Philosophy*.  
  <https://plato.stanford.edu/entries/scientific-representation/>

E7G-T use:

These anchors support E7G-T’s caution that models, maps, diagrams, equations, dashboards, and simulations should not be treated as reality itself.

Kernel caution:

A model can be useful without being identical to its target. The source/view distinction must remain visible.

### 20.8 Measurement

**Measurement in science**

- Luca Mari, Mark Wilson, and Andrew Maul, “Measurement in Science,” *The Stanford Encyclopedia of Philosophy*.  
  <https://plato.stanford.edu/entries/measurement-science/>

E7G-T use:

Measurement is relevant to E7G-T’s claim that observations and recorded values are protocol-governed projections of systems into representational forms.

Kernel caution:

Measurement-facing claims require domain standards, protocols, uncertainty, calibration, and evidence. E7G-T can frame this; it cannot replace it.

### 20.9 Information, compression, and data

**Information**

- Pieter Adriaans, “Information,” *The Stanford Encyclopedia of Philosophy*.  
  <https://plato.stanford.edu/entries/information/>

E7G-T use:

Information theory and philosophy of information are relevant to projection, compression, loss, encoding, uncertainty, and representation.

Kernel caution:

Do not use “information,” “compression,” or “loss” as technical information-theoretic terms unless the relevant formal substrate is declared.

### 20.10 Translation and translation QA

**Translation services standard**

- ISO 17100:2015, “Translation services — Requirements for translation services.”  
  <https://www.iso.org/standard/59149.html>

E7G-T use:

Translation is one of the strongest practical domains for E7G-T because translation is visibly a purpose-bound projection from source text into target text.

Kernel caution:

E7G-T can help frame translation QA as invariant-preserving projection, but professional translation quality still depends on linguistic competence, domain expertise, revision, client specification, and applicable standards.

### 20.11 Source-use rule

When public-facing E7G-T text refers to an established field, it should use one of the following source postures:

1. **Neighbourhood** — E7G-T stands near this field but does not claim identity.
2. **Borrowed caution** — E7G-T uses the field to avoid overclaiming.
3. **Formalisation candidate** — E7G-T may later be formalised using tools from this field.
4. **Application domain** — E7G-T may be applied to artefacts in this field, without replacing the field.
5. **Stop condition** — the field has stronger tools, so E7G-T should route the user back to those tools.

### 20.12 Public-reference rule

Use internal project documents to reason.

Use public sources to support public claims.

Use domain experts to review domain-facing applications.

Use formal substrates to make formal claims.

Use empirical protocols to make empirical claims.

---

End of Kernel v0.9 Draft.
