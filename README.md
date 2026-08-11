# COMASTA

**Human-Centered Character Action Interpretability Specification**

> **COMASTA v0.2**<br>
> **Experimental v0.2 — Adversarially evaluated under limited recorded conditions; not scientifically or generally validated**

COMASTA is an experimental specification for evaluating whether an externally supplied character action can be understood from the character and situation information currently available.

Its central principle is:

> **A character's history may shape future behavior without determining it.**

COMASTA evaluates interpretive support. It does not predict what a character will do, assign behavioral probabilities, model a personality, diagnose psychology, generate characters, or replace authorial judgment.

## What v0.2 evaluates

An assessment begins with a `Candidate Action`. When necessary, the action and its specific form of expression may be evaluated as separate targets.

The protocol asks:

> Can this Candidate Action be understood from grounded character and situational conditions without silently completing unknown information?

It distinguishes:

- established patterns from deterministic rules;
- deviation from implausibility;
- supplied information from derived interpretation;
- `UNGROUNDED` claims from `UNSUPPORTED` actions and `CRITICAL CONTEXT MISSING`;
- action interpretability from expression interpretability;
- explanation from prediction.

## Core architecture

### Assessment states

- `SUPPORTED`
- `PLAUSIBLE DEVIATION`
- `UNSUPPORTED`

### Assessment disposition

- `ISSUED`
- `WITHHELD`

### Epistemic status

- `SUFFICIENT FOR TARGET`
- `CRITICAL CONTEXT MISSING`

### Grounding labels

- `EXPLICIT`
- `DERIVED`
- `UNGROUNDED`

Speculative interpretations may be shown separately. They are never supporting evidence.

### Behavioral Bridge

When an action conflicts with an established baseline, COMASTA examines:

1. Bridge Origin
2. Difference-Making Condition
3. Character Meaning
4. Action Link

The only bridge statuses are:

- `BRIDGE ESTABLISHED`
- `BRIDGE NOT ESTABLISHED`

A bridge describes why a deviation may be interpretable. It does not estimate whether the deviation will occur.

## Current evidence boundary

COMASTA v0.2 has been adversarially evaluated only under the limited conditions recorded in [`tests/results/`](tests/results/README.md). Observed results are evidence about those particular runs, not general validation. A direct PASS means that the named test's criteria passed in the recorded run; paired evidence does not convert a component test into an independent pass.

| Test | Public result boundary |
|---|---|
| T001 | Direct **PASS** (`T001-run-001`). |
| T002 | **No independent run.** Relevant paired evidence exists through `T010-A-run-001` only. |
| T003 | Controlled Run 001 **FAIL**. Controlled Run 002 observed the core expected action pattern but remained a strict protocol **FAIL** because of DERIVED-to-EXPLICIT provenance. Historical v0.1 pilot `T003-R001` remains separate. |
| T004 | Direct **PASS** (`T004-run-001`). |
| T005 | **No independent run.** Relevant paired evidence exists through `T010-B-run-001` only. |
| T006 | **NOT RUN**. |
| T007 | **PASS**, with the historical/non-blind `T007-R001` compliance observation preserved alongside blind/isolated `T007-run-002` and positive control `T007-PC001`. |
| T008 | **PASS WITH OBSERVATION** for the paired `T008-A-run-001` / `T008-B-run-001` record. No normative change is made here. |
| T009 | **PASS WITH OBSERVATION** (`T009-run-001`). |
| T010 | Paired **PASS WITH OBSERVATION** (`T010-A-run-001` / `T010-B-run-001`). These cases are paired evidence for T002 and T005, not independent executions of those tests. |
| T011 | `T011-run-001` **FAIL** → normative clarification → `T011-run-002` regression **PASS**. The initial failure remains part of the record. |
| T012 | Direct **PASS** (`T012-run-001`). |
| T013 | **PASS WITH OBSERVATION** (`T013-run-001`). No normative change is made here. |
| T014 | **NOT RUN**. |
| T015 | Repeated-run **PASS WITH MINOR OBSERVATION** across `T015-R001`–`T015-R005`, under its recorded runtime only. |

### Validation summary

This evidence does **not** establish:

- scientific validity;
- psychological validity;
- statistical reliability;
- cross-model reliability;
- improved underlying LLM reasoning;
- prediction of human behavior;
- general superiority to baseline prompting.

## Repository structure

1. [Principles](PRINCIPLES.md)
2. [Specification](SPECIFICATION.md)
3. [Evaluation](EVALUATION.md)
4. [LLM adaptation protocol](PROMPTING.md)
5. [Structured examples](schemas/)
6. [Narrative examples](examples/)
7. [Test protocol and definitions](tests/)
8. [Preserved v0.1 materials](versions/v0.1/)

The result index distinguishes the preserved v0.1 pilot from v0.2 observations and identifies tests that were not independently run.

## Status boundary

COMASTA may report that a Candidate Action is unsupported by current material. The author may still choose that action deliberately. `UNSUPPORTED` does not mean impossible, incorrect, or forbidden.

Authorial intention may define the scope of interpretation, including protected ambiguity. It does not count as behavioral evidence and cannot upgrade an unsupported action.

## License

COMASTA is licensed under the [Apache License 2.0](LICENSE).

Unless otherwise noted, the license applies to the contents of this repository. It does not include unpublished screenplays, private narrative materials, or other creative works not contained in the repository.

## Author

**AXIR TSAI**  
Original Series Creator  
Taiwan  

[axirverse.com](https://axirverse.com)
