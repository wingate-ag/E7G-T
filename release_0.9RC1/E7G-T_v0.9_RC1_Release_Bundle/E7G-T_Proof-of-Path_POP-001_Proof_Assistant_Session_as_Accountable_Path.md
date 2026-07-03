# E7G-T Proof-of-Path Prototype — POP-001

# Proof Assistant Session as Accountable Path

**Prototype ID:** POP-001  
**Kernel compatibility:** E7G-T v0.9 draft  
**Related atlas entry:** APP-001 — AI Output as Projection  
**Status:** pilot-ready prototype  
**Date:** 2026-06-29  
**Primary use:** proof-assistant learning, proof review, AI-assisted proof checking, formal-methods onboarding, proof-state explanation

---

## 1. Purpose

This prototype applies E7G-T v0.9 to proof-assistant work.

The basic claim is:

> A proof assistant session should be treated as an accountable path through formal states, transformations, projections, obligations, and checks.

Proof-of-Path does **not** replace formal proof. It records how a claim moved from statement to checked, failed, partial, explained, or stopped status.

This prototype is designed for:

- proof-assistant learners;
- Lean / Coq / Agda / Isabelle users;
- AI-assisted proof work;
- mathematical writing;
- formal-methods documentation;
- proof debugging;
- proof pedagogy;
- proof-review workflows.

---

## 2. Core Distinction

A proof assistant session contains several layers that should not be confused.

| Layer | E7G-T reading | What it can support | What it cannot support alone |
|---|---|---|---|
| Theorem statement | bounded formal claim | Defines target | Does not prove itself |
| Human intuition | D5/D7 possibility and strategy space | Guides search | Is not proof |
| Proof script | D1/D2 path projection | Shows attempted route | May not equal proof object |
| Tactic state | D2/D7 local slice | Shows current goals and assumptions | Is not the whole proof |
| Tactic | D6 transformation | Moves proof state | Must be admissible under substrate |
| Error message | D2 projection of failed elaboration/checking | Helps debugging | May hide deeper issue |
| Proof object / term | D6 formal object under substrate | Carries formal validity if accepted | May not explain itself |
| Kernel check | D6/TR6 closure event | Gives formal acceptance under substrate | Does not guarantee human understanding |
| Explanation | D2/D7 projection for humans | Supports learning and communication | Is not necessarily the formal proof |

---

## 3. Entity of Concern

**Entity:** proof assistant session.

The entity is not only the final accepted theorem. It is the **path** from claim to proof status.

A proof assistant session may include:

- theorem statement;
- definitions;
- imports;
- assumptions;
- proof script;
- tactic states;
- error messages;
- generated obligations;
- discharged obligations;
- proof term or proof object;
- kernel acceptance;
- human explanation;
- AI-generated suggestions;
- unresolved gaps.

---

## 4. Placement

### Compact placement

```text
ProofAssistantSession : D2/D6/D7 @ TR1/TR6 / FormalInteractionContext
```

### Meaning

The proof assistant session is treated as:

- **D2** because the user sees text, goals, error messages, interface states, and explanations;
- **D6** because proof validity depends on formal rules, tactics, elaboration, and kernel checking;
- **D7** because interaction context, libraries, user purpose, theorem framing, and explanation needs govern use;
- **TR1** because the user experiences the proof process as a local sequence of steps;
- **TR6** when a proof object is accepted as closed under the formal substrate.

---

## 5. Source / View / Substrate

| Component | Role |
|---|---|
| **Source claim** | The theorem or proposition to be proved. |
| **Formal substrate** | The proof assistant’s logic, kernel, elaborator, library, definitions, and rules. |
| **Visible view** | Script, tactic state, error messages, rendered goals, proof explanation. |
| **Proof path** | The sequence of admissible transformations from claim to status. |
| **Proof status** | open, partial, failed, accepted, explained, published, reused. |
| **Human explanation** | A projection of the proof or strategy into readable form. |

### Core repair

Do not ask only:

> “Did the proof assistant accept it?”

Ask also:

> “What path produced acceptance, what obligations were discharged, and what explanation status remains?”

---

## 6. Projection Account

A proof assistant session contains projections.

### Proof text as projection

```text
ProofObject? : D6 @ TR6 / FormalSubstrate
  --π_Explanation^{6→2}-->
ProofText : D2 @ TR0/TR1 / HumanReadingContext
[preserves: selected structure, steps, dependencies;
 loses: elaboration detail, implicit arguments, search path, kernel-level object]
```

### Tactic state as slice

```text
S_CurrentGoal(ProofWork) = TacticState
```

The tactic state is a local slice of the current proof situation. It is useful because it exposes current goals and assumptions. It is limited because it is not the whole proof object.

### Error message as projection

```text
FailedCheck : D6 @ TR1 / FormalSubstrate
  --π_ErrorInterface^{6→2}-->
ErrorMessage : D2 @ TR1 / UserInterfaceContext
[preserves: selected failure signal;
 loses: full internal elaboration state;
 use: debugging prompt]
```

---

## 7. Transformation Account

A tactic is a transformation under formal rules.

```text
τ_Tactic(ProofState_1) = ProofState_2
```

Examples:

| Tactic-like move | E7G-T reading |
|---|---|
| Introduce variable / assumption | Boundary adjustment; premise moves into local context. |
| Apply theorem | Incidence between current goal and known theorem. |
| Rewrite | Transformation under equality or equivalence rule. |
| Simplify | Transformation under simplification set. |
| Split cases | Slice / branch current proof state. |
| Exact term | Close goal by providing matching proof object. |
| Induction | Generate structured branch obligations. |
| Contradiction | Close goal by deriving inconsistency under assumptions. |
| Automation | Transformation stack under tool-selected rules. |

### Transformation rule

No tactic should be treated as meaningful merely because it changes the visible state. It must be admissible under the formal substrate.

---

## 8. Proof-of-Path Definition

A Proof-of-Path record is an accountability layer for proof work.

It records:

- the claim;
- the substrate;
- the assumptions;
- the active definitions;
- the visible state;
- the transformation sequence;
- the obligations created;
- the obligations discharged;
- the projections shown to the user;
- the proof status;
- the explanation status;
- the remaining gaps;
- the stop condition.

### Key rule

Proof-of-Path documents the path.

It does not prove the theorem unless the relevant formal substrate accepts the proof.

---

## 9. ProofOfPathCard Template

```yaml
id:
claim:
theoremStatement:
formalSubstrate:
  assistant:
  logic:
  libraries:
  definitions:
  kernelOrChecker:
entityOfConcern: proof assistant session
placement: ProofAssistantSession : D2/D6/D7 @ TR1/TR6 / FormalInteractionContext
boundary:
  includes:
    - theorem statement
    - assumptions
    - definitions
    - imports/libraries
    - proof script
    - tactic states
    - errors
    - accepted proof object if present
  excludes:
    - unstated mathematical intuition
    - informal explanation not linked to proof
    - unverified AI suggestions
temporalRegime:
  discovery: TR1/TR3
  construction: TR1
  acceptedProofObject: TR6
sourceClaim:
proofGoal:
initialState:
pathSteps:
  - step:
    visibleMove:
    moveType:
    inputState:
    transformationRule:
    outputState:
    obligationsCreated:
    obligationsDischarged:
    preservedInvariant:
    lossOrHiddenStructure:
    checkerStatus:
projectionEvents:
  - visibleState:
    projectedFrom:
    preserves:
    loses:
reconstructionStatus:
proofStatus:
explanationStatus:
bridgeMode:
admissibleUse:
nonAdmissibleUse:
weakestLink:
stopCondition:
nextMove:
reviewerNotes:
```

---

## 10. Path Step Schema

Each proof step should be recorded as an accountable movement.

```yaml
step: 3
visibleMove: "apply theorem_X"
moveType: incidence / transformation
inputState: "goal before step"
transformationRule: "theorem_X application under current assumptions"
outputState: "new subgoals"
obligationsCreated:
  - "prove side condition A"
  - "match type B"
obligationsDischarged:
  - "main implication target"
preservedInvariant:
  - "logical equivalence under rule"
lossOrHiddenStructure:
  - "implicit arguments hidden by interface"
checkerStatus: accepted / failed / pending
```

---

## 11. Proof Status Ladder

| Status | Meaning |
|---|---|
| **unplaced** | Claim not yet typed or formalised. |
| **placed** | Claim has a formal statement and substrate. |
| **open** | Proof has active goals. |
| **partial** | Some obligations discharged, others remain. |
| **failed** | A transformation or check failed. |
| **blocked** | Missing definition, theorem, import, or strategy. |
| **accepted** | Formal substrate accepts the proof. |
| **explained** | Human-readable explanation is aligned with accepted proof. |
| **reused** | Proof or theorem is transported into another context with boundary checks. |
| **published** | Proof is communicated in a social/public record. |

### Status rule

Accepted is not the same as explained.

Explained is not the same as formally accepted.

Published is not the same as checked.

---

## 12. Common Failure Modes

### 12.1 Theorem statement mismatch

The user thinks they proved one claim, but the formal theorem states another.

**Repair:** compare natural-language claim and formal statement.

### 12.2 Hidden assumption

A proof depends on an assumption not visible in the informal explanation.

**Repair:** inspect local context, imports, typeclass assumptions, axioms, and definitions.

### 12.3 Tactic success overread

A tactic closes a goal, but the user does not understand what was used.

**Repair:** expose obligations, dependencies, and transformation class.

### 12.4 Error message overread

An error message is treated as the whole reason for failure.

**Repair:** treat the error as a projection of failed checking, not as the full internal state.

### 12.5 Proof sketch mistaken for proof

An AI or human gives a plausible proof outline, but no formal obligations are discharged.

**Repair:** downgrade to proof sketch until checked.

### 12.6 Accepted proof mistaken for explanation

The proof assistant accepts the proof, but the user cannot explain it.

**Repair:** create explanation projection and verify alignment.

### 12.7 Library dependency hidden

A proof succeeds because of imported theorems or automation not disclosed in the explanation.

**Repair:** list dependencies and automation scope.

### 12.8 Boundary transport failure

A theorem is reused outside its assumptions.

**Repair:** check domain, definitions, assumptions, and transformation class.

---

## 13. OneLine Templates

### Generic

```text
E7-OneLine: The proof assistant session is treated as a D2/D6/D7 projection of formal proof work under kernel context; admissible move: record path steps and checker status; blocked overread: visible script is not the whole proof object.
```

### For an accepted proof

```text
E7-OneLine: The accepted theorem is treated as TR6 closure under the declared formal substrate; admissible move: produce human explanation and dependency account; blocked overread: accepted is not explained.
```

### For an AI proof suggestion

```text
E7-OneLine: The AI proof suggestion is treated as a D2/D7 textual projection of possible proof strategy; admissible move: formalise and check; blocked overread: proof sketch is not proof.
```

### For an error message

```text
E7-OneLine: The error message is treated as a D2 projection of a failed formal check; admissible move: inspect boundary, type, and transformation mismatch; blocked overread: error text is not the whole failure state.
```

---

## 14. MiniCard Example

```yaml
id: POP-001-example-001
entity: proof assistant session
plainMeaning: A user attempts to prove a theorem using tactics.
placement: ProofAssistantSession : D2/D6/D7 @ TR1/TR6 / FormalInteractionContext
boundary:
  includes:
    - theorem statement
    - imports
    - local assumptions
    - tactic script
    - visible proof state
  excludes:
    - informal intuition not formalised
    - AI suggestion not checked
projectionAccount:
  source: formal substrate + proof object candidate + elaboration process
  view: visible script and tactic states
preserved:
  - current goals
  - local hypotheses
  - accepted transformations
lost:
  - full elaboration detail
  - hidden implicit arguments
  - dependency chain unless inspected
invariant:
  - theorem meaning under declared definitions and assumptions
transformationClass:
  - permitted tactics and kernel rules
reconstructionStatus: partial until proof object/dependencies inspected
bridgeMode: formal-compatibility / formal proof when accepted
proofStatus: partial
explanationStatus: not yet explained
weakestLink: unresolved subgoal
admissibleUse:
  - learning
  - debugging
  - proof development
nonAdmissibleUse:
  - claim theorem is proved before closure
nextMove: inspect active goals and discharge remaining obligations
blockedOverread: proof script fragment is not completed proof
```

---

## 15. AI-Assisted Proof Review

AI can help propose:

- proof strategies;
- lemma names;
- tactic sequences;
- explanation drafts;
- dependency summaries;
- translation from informal proof to formal statement;
- debugging hypotheses.

AI cannot by itself supply formal proof status unless the substrate checks the proof.

### AI proof suggestion placement

```text
AIProofSuggestion : D2/D7 @ TR1 / ProofPromptContext
```

### Review rule

```text
AIProofSuggestion --requires--> FormalCheck
```

### Blocked overread

AI plausibility is not kernel acceptance.

---

## 16. Proof Debugging Workflow

### Step 1 — Place the claim

```text
TheoremClaim : D2/D6 @ TR0 / FormalSubstrate
```

Ask:

- What is the exact theorem statement?
- What definitions are active?
- What assumptions are visible?
- What substrate governs validity?

### Step 2 — Bound the proof

Ask:

- What is included in the proof attempt?
- What imports or libraries are active?
- What axioms or assumptions are used?
- What does the user think is being proved?

### Step 3 — Slice the current state

```text
S_CurrentGoal(ProofWork)
```

Ask:

- What is the current goal?
- What hypotheses are in context?
- What side conditions remain?

### Step 4 — Classify the next move

Possible move types:

- place;
- bound;
- incide;
- transform;
- rewrite;
- split;
- reduce;
- apply;
- reconstruct;
- stop.

### Step 5 — Record obligations

For every transformation, ask:

- What did this discharge?
- What did this create?
- What did it hide?
- What dependency did it introduce?

### Step 6 — Check status

Possible statuses:

- failed;
- open;
- partial;
- accepted;
- explained;
- stopped.

### Step 7 — Explain only after checking

Create human explanation after proof status is clear.

---

## 17. Interface Prototype Concept

A Proof-of-Path interface could add panels around a proof assistant.

### Panel 1 — Entity Panel

Shows theorem statement, claim boundary, definitions, and active substrate.

### Panel 2 — State Panel

Shows current proof state as a slice, not as the whole proof.

### Panel 3 — Move Panel

Labels each tactic or edit as Place, Bound, Incide, Slice, Project, Transform, Reconstruct, Bridge, or Stop.

### Panel 4 — Obligation Panel

Lists obligations created and discharged at each step.

### Panel 5 — Projection Panel

Shows what the current interface view preserves and hides.

### Panel 6 — Dependency Panel

Shows imported theorems, simplification rules, axioms, automation, or hidden dependencies.

### Panel 7 — Status Panel

Separates proof status from explanation status.

### Panel 8 — Explanation Panel

Generates or stores human explanation after formal status is known.

---

## 18. Minimal JSON-Like Schema

```json
{
  "prototype_id": "POP-001",
  "entity": "proof assistant session",
  "placement": "ProofAssistantSession : D2/D6/D7 @ TR1/TR6 / FormalInteractionContext",
  "formal_substrate": {
    "assistant": "",
    "logic": "",
    "libraries": [],
    "definitions": [],
    "checker": ""
  },
  "claim": "",
  "theorem_statement": "",
  "boundary": {
    "includes": [],
    "excludes": []
  },
  "path_steps": [],
  "projection_events": [],
  "obligations_created": [],
  "obligations_discharged": [],
  "proof_status": "open",
  "explanation_status": "not explained",
  "bridge_mode": "formal-compatibility",
  "weakest_link": "",
  "admissible_use": [],
  "non_admissible_use": [],
  "stop_condition": "",
  "next_move": ""
}
```

---

## 19. Pilot Test Design

### Pilot question

Does Proof-of-Path make proof-assistant sessions easier to review, debug, explain, and trust?

### Test set

Use 10–20 proof-assistant exercises across:

- simple theorem accepted by direct proof;
- proof requiring rewrite;
- proof requiring induction;
- proof failing due to missing assumption;
- proof failing due to type mismatch;
- proof using automation;
- AI-suggested proof sketch;
- accepted proof with poor human explanation;
- theorem reuse outside assumptions;
- proof with hidden library dependency.

### Baseline

Learners or reviewers inspect proof scripts normally.

### Intervention

Learners or reviewers use the ProofOfPathCard and path-step schema.

### Measures

Track whether users better identify:

- theorem statement mismatch;
- hidden assumptions;
- active goals;
- obligations created/discharged;
- proof status;
- explanation status;
- tactic meaning;
- dependency chain;
- reason for failure;
- next admissible move.

### Success criterion

Proof-of-Path is useful if it improves debugging, explanation, or review clarity without excessive overhead.

---

## 20. Relation to Kernel v0.9

This prototype operationalises:

- D2/D6/D7 placement;
- TR1/TR6 temporal distinction;
- typing before operation;
- slice discipline;
- transformation under rule-space;
- projection loss;
- reconstruction status;
- Proof-of-Path kernel;
- formal-neighbourhood discipline;
- anti-replacement rule;
- stop conditions.

It is an application of the kernel, not a replacement for formal proof.

---

## 21. Stop Conditions

Stop or downgrade when:

- theorem statement is unclear;
- formal substrate is undeclared;
- proof script has open goals;
- tactic transformation is not accepted;
- assumptions differ from intended claim;
- proof relies on hidden or unacceptable axiom;
- AI suggestion is not checked;
- explanation diverges from formal proof;
- theorem is reused outside its boundary;
- user treats accepted proof as understood proof without explanation.

---

## 22. Productisation Possibilities

This prototype could become:

- a proof-assistant learning worksheet;
- a Lean/Coq session annotation guide;
- an AI proof-suggestion review card;
- a proof-debugging checklist;
- a formal-methods onboarding tool;
- a proof explanation generator scaffold;
- a plugin concept for proof-state annotation;
- a classroom module for “proof path literacy.”

The first realistic product is a manual Proof-of-Path worksheet for proof-assistant learners.

---

## 23. Closing Rule

A proof assistant can check formal closure.

Proof-of-Path records how the claim travelled.

A checked proof may still need explanation.

An explanation may still need checking.

Keep the path visible.
