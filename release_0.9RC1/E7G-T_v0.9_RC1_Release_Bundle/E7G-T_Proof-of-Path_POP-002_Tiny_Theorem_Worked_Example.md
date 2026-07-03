# E7G-T Proof-of-Path — POP-002

# Tiny Theorem Worked Example

**Prototype ID:** POP-002  
**Kernel compatibility:** E7G-T v0.9 draft  
**Builds on:** POP-001 — Proof Assistant Session as Accountable Path  
**Status:** worked example / teaching prototype  
**Date:** 2026-06-30  
**Primary use:** proof-assistant onboarding, Proof-of-Path demonstration, AI-assisted proof review

---

## 1. Purpose

POP-001 defined Proof-of-Path for proof-assistant sessions.

POP-002 shows a tiny worked example.

The purpose is not to prove a deep theorem. The purpose is to show how E7G-T records:

- the claim;
- the formal substrate;
- the boundary;
- the visible proof script;
- the proof-state path;
- the transformation;
- the obligation discharged;
- the proof status;
- the explanation status;
- the blocked overread.

Core rule:

> A checked proof and an explained proof are related, but not identical.

---

## 2. Tiny Theorem

We use a minimal Lean-style theorem:

```lean
theorem identity_proof (P : Prop) (h : P) : P := by
  exact h
```

Plain-language meaning:

> If proposition `P` is assumed, and `h` is a proof of `P`, then `P` follows directly from `h`.

This theorem is intentionally trivial because it makes the Proof-of-Path machinery visible without mathematical complexity.

---

## 3. E7G-T OneLine

```text
E7-OneLine: This proof assistant session is treated as a D2/D6/D7 path from theorem statement to checked closure under a formal substrate; admissible move: record how the assumption h discharges the goal P; blocked overread: visible script is not the whole proof object.
```

---

## 4. Placement

```text
ProofAssistantSession : D2/D6/D7 @ TR1/TR6 / FormalInteractionContext
```

Meaning:

- **D2** — the user sees text, goals, proof script, and interface output.
- **D6** — validity depends on formal rules, typing, elaboration, and checking.
- **D7** — context matters: theorem statement, assumptions, library, user purpose, explanation need.
- **TR1** — the user experiences proof construction as a sequence.
- **TR6** — once accepted, the proof is closed under the declared formal substrate.

Claim placement:

```text
TheoremClaim : D2/D6 @ TR0 / FormalSubstrate
```

Proof script placement:

```text
ProofScript : D2 @ TR1 / UserInterfaceContext
```

---

## 5. Boundary

### Included

- theorem name;
- proposition parameter `P`;
- assumption `h : P`;
- target conclusion `P`;
- proof script;
- tactic-style command `exact h`;
- formal checking status;
- explanation status.

### Excluded

- any claim about the truth of arbitrary real-world propositions;
- any empirical interpretation of `P`;
- any deep mathematical theorem beyond the local formal statement;
- any claim that the user understands the proof merely because it is accepted;
- any claim that Proof-of-Path itself proves the theorem.

Boundary rule:

```text
Given P and h : P, return P.
```

The theorem does not prove that every proposition is true.

---

## 6. Initial Proof State

After introducing the theorem parameters, the proof context contains:

```text
P : Prop
h : P
⊢ P
```

Meaning:

- `P : Prop` declares that `P` is a proposition.
- `h : P` declares that `h` is a proof or assumption of `P`.
- `⊢ P` means the current goal is to prove `P`.

E7G-T slice:

```text
S_CurrentGoal(ProofWork) = {context: P : Prop, h : P; goal: P}
```

The visible goal state preserves:

- local assumptions;
- current target;
- immediate proof obligation.

It loses:

- full internal elaboration detail;
- proof object representation;
- broader explanation unless supplied separately.

---

## 7. Transformation Step

The proof script contains one move:

```lean
exact h
```

E7G-T transformation notation:

```text
τ_exact-h(ProofState_1) = ProofState_2
```

Input state:

```text
P : Prop
h : P
⊢ P
```

Transformation rule:

`exact h` attempts to close the current goal by providing `h` as an exact term of the required type.

The goal is `P`.

The term `h` has type `P`.

Therefore, `h` satisfies the goal.

Output state:

```text
no remaining goals
```

The only obligation, `prove P`, is discharged by `h : P`.

---

## 8. Path Step Record

```yaml
step: 1
visibleMove: "exact h"
moveType: "transformation / direct closure"
inputState:
  context:
    - "P : Prop"
    - "h : P"
  goal: "P"
transformationRule: "provide a term whose type exactly matches the current goal"
outputState:
  goals: []
obligationsCreated: []
obligationsDischarged:
  - "P"
preservedInvariant:
  - "the conclusion matches the type of h"
lossOrHiddenStructure:
  - "elaboration details"
  - "kernel-level proof object representation"
checkerStatus: "accepted if formal substrate accepts the term"
```

---

## 9. Projection Events

### 9.1 Theorem text as projection

```text
FormalClaim : D6 @ TR0 / FormalSubstrate
  --π_TextRender^{6→2}-->
TheoremText : D2 @ TR0 / HumanReadingContext
```

Preserves:

- theorem name;
- parameters;
- assumption;
- target proposition;
- proof script.

Loses:

- internal proof term;
- kernel checking details;
- educational explanation.

### 9.2 Proof state as projection

```text
ProofState_Internal : D6 @ TR1 / FormalSubstrate
  --π_Interface^{6→2}-->
VisibleGoalState : D2 @ TR1 / UserInterfaceContext
```

Preserves:

- current context;
- current goal.

Loses:

- full elaboration state;
- internal constraints;
- possible implicit arguments.

### 9.3 Explanation as projection

```text
CheckedProof : D6 @ TR6 / FormalSubstrate
  --π_Explanation^{6→2}-->
HumanExplanation : D2/D7 @ TR1 / TeachingContext
```

Preserves:

- the intuitive reason the proof works;
- the relationship between `h : P` and goal `P`.

Loses:

- formal object detail.

---

## 10. Proof Status

If the formal substrate accepts the script, the proof status is:

```text
proofStatus: accepted under declared formal substrate
```

Accepted means:

> The formal checker accepts the proof under the declared assumptions and rules.

Accepted does **not** mean:

- the user understands the proof;
- the theorem says more than its formal statement;
- Proof-of-Path itself is the proof.

If the theorem has not actually been run, use:

```text
proofStatus: illustrative / unchecked
```

---

## 11. Explanation Status

Minimal human explanation:

> The goal is to prove `P`. The context already contains `h : P`, which is a proof of `P`. Therefore `exact h` closes the goal by giving the proof already available in the context.

This gives:

```text
explanationStatus: explained-minimal
```

Conceptual explanation:

> In type-theoretic proof assistants, propositions may be treated as types of proofs. If `h : P`, then `h` is a term inhabiting the proposition `P`; supplying `h` proves `P`.

This gives:

```text
explanationStatus: explained-conceptual
```

---

## 12. Full ProofOfPathCard

```yaml
id: POP-002-identity-proof
claim: "Given a proposition P and h : P, prove P."
theoremStatement: "theorem identity_proof (P : Prop) (h : P) : P := by exact h"
formalSubstrate:
  assistant: "Lean-style proof assistant syntax"
  logic: "dependent type theory / propositions-as-types style"
  libraries: []
  definitions:
    - "Prop"
  kernelOrChecker: "declared formal checker, if actually run"
entityOfConcern: proof assistant session
placement: "ProofAssistantSession : D2/D6/D7 @ TR1/TR6 / FormalInteractionContext"
boundary:
  includes:
    - theorem name
    - proposition parameter P
    - assumption h : P
    - target conclusion P
    - proof script
    - checker status if available
    - explanation status
  excludes:
    - empirical meaning of P
    - proof that arbitrary propositions are true
    - hidden assumptions outside the formal context
    - claim that the user understands the proof merely from acceptance
temporalRegime:
  discovery: "TR1"
  construction: "TR1"
  acceptedProofObject: "TR6 if checker accepts"
sourceClaim: "If h is a proof of P, then P follows."
proofGoal: "P"
initialState:
  context:
    - "P : Prop"
    - "h : P"
  goal: "P"
pathSteps:
  - step: 1
    visibleMove: "exact h"
    moveType: "transformation / direct closure"
    inputState: "P : Prop, h : P ⊢ P"
    transformationRule: "provide a term matching the goal type"
    outputState: "no remaining goals"
    obligationsCreated: []
    obligationsDischarged:
      - "P"
    preservedInvariant:
      - "goal type P matches h : P"
    lossOrHiddenStructure:
      - "internal elaboration details"
      - "kernel proof object representation"
    checkerStatus: "accepted if run under compatible substrate"
projectionEvents:
  - visibleState: "theorem text"
    projectedFrom: "formal claim"
    preserves:
      - "parameters"
      - "assumption"
      - "goal"
      - "script"
    loses:
      - "internal proof object"
  - visibleState: "goal state"
    projectedFrom: "formal proof state"
    preserves:
      - "context"
      - "goal"
    loses:
      - "internal elaboration constraints"
reconstructionStatus: "strong if checker acceptance is available; otherwise Lean-style illustrative"
proofStatus: "accepted if checked; illustrative if not actually run"
explanationStatus: "explained-minimal"
bridgeMode: "formal-compatibility; formal proof only if actually checked"
admissibleUse:
  - teaching Proof-of-Path
  - explaining assumption discharge
  - proof-assistant onboarding
nonAdmissibleUse:
  - claiming Proof-of-Path replaces formal checking
  - claiming theorem proves all propositions
weakestLink: "actual checker run if formal-proof status is claimed"
stopCondition: "stop before formal-proof claim unless checker acceptance is confirmed"
nextMove: "run in declared proof assistant or keep as Lean-style illustrative example"
reviewerNotes: "The example is intentionally trivial to make path-accounting visible."
```

---

## 13. Claim-Strength Classification

| Claim | Status |
|---|---|
| “This is a Lean-style proof script.” | Formal-compatibility / illustrative unless actually run. |
| “If `h : P`, then `P` follows by exact `h`.” | Formal reasoning under propositions-as-types style. |
| “The proof is accepted.” | Requires actual checker acceptance. |
| “The proof is explained.” | Requires human explanation aligned with proof. |
| “Proof-of-Path proves the theorem.” | Not allowed. |
| “This example shows how Proof-of-Path records proof movement.” | Operational / educational claim. |

---

## 14. Blocked Overreads

### Overread 1 — “The theorem proves every proposition.”

Blocked.

The theorem proves only:

> If a proof of `P` is already available, then `P`.

### Overread 2 — “The proof script is the whole proof object.”

Blocked.

The visible script is a D2 projection. The proof object/checking substrate is D6.

### Overread 3 — “The user understands the proof because the checker accepted it.”

Blocked.

Acceptance and explanation are different statuses.

### Overread 4 — “Proof-of-Path replaces formal checking.”

Blocked.

Proof-of-Path documents the path. The formal substrate checks proof validity.

### Overread 5 — “An AI-generated proof suggestion is enough.”

Blocked.

AI suggestion remains D2/D7 projection until formal checking.

---

## 15. Mini Lesson

This tiny theorem teaches five E7G-T proof principles.

1. **The goal must be placed.**  
   The proof starts only after the theorem statement defines the target.

2. **The boundary matters.**  
   The theorem has an assumption `h : P`. Remove `h`, and the proof no longer works.

3. **The tactic is a transformation.**  
   `exact h` changes the proof state by closing the goal.

4. **The visible script is a projection.**  
   The script is useful, but it is not identical with the internal proof object.

5. **Proof status and explanation status differ.**  
   A checked proof may still need explanation.

---

## 16. Teaching Version

For a beginner, explain the proof like this:

1. The theorem asks us to prove `P`.
2. The context already gives us `h : P`.
3. That means `h` is already a proof of `P`.
4. The command `exact h` says: use `h` exactly as the proof.
5. No goals remain.
6. Therefore the proof is complete if the checker accepts it.

---

## 17. E7G-T Diagram

```text
Theorem statement
  ↓ Place
Context: P : Prop, h : P
Goal: P
  ↓ Slice current goal
Visible proof state: h : P ⊢ P
  ↓ Transform
exact h
  ↓ Discharge obligation
Goal P closed
  ↓ Check
Accepted under formal substrate
  ↓ Project
Human explanation
```

---

## 18. Test Instructions

To use this as a real proof-assistant test:

1. Open a compatible Lean-style environment.
2. Enter the theorem.
3. Run the checker.
4. Record whether it is accepted.
5. If accepted, set `proofStatus: accepted`.
6. Write a human explanation.
7. Set `explanationStatus`.
8. Record any syntax adjustments required by the environment.

If the proof is not run, keep the status as:

```text
proofStatus: illustrative / unchecked
```

---

## 19. Relation to POP-001

POP-001 gave the general architecture.

POP-002 provides a minimal complete path:

```text
claim → context → goal → exact h → no goals → accepted/explained status
```

This demonstrates the practical value of Proof-of-Path:

> It prevents “the proof worked” from hiding the path by which it worked.

---

## 20. Relation to Kernel v0.9

This worked example operationalises:

- Typing Before Operation;
- Boundary Is Contextual But Not Arbitrary;
- Invariance Requires a Transformation Class;
- Projection Is Not Reconstruction;
- Proof-of-Path does not replace proof;
- accepted status is not explanation status;
- formal proof claims require a declared formal substrate.

---

## 21. Stop Conditions

Stop or downgrade the claim when:

- the theorem has not been run in a checker;
- the formal substrate is undeclared;
- syntax differs from the actual proof assistant version;
- assumptions are hidden or changed;
- the user claims more than the theorem states;
- an AI-generated proof is accepted without checking;
- explanation diverges from the formal statement;
- Proof-of-Path is treated as proof rather than path documentation.

---

## 22. Closing Rule

A tiny theorem can still teach the whole discipline:

place the claim;

name the boundary;

slice the state;

record the transformation;

track the obligation;

separate acceptance from explanation;

do not let the visible script become the whole proof.
