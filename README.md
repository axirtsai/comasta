# COMASTA

**Human-Centered Character Action Interpretability Specification**

> **COMASTA v0.2-draft**<br>
> **Experimental Specification**<br>
> **Not Yet Validated**

COMASTA is an experimental specification for evaluating whether an externally supplied character action can be understood from the character and situation information currently available.

Its central principle is:

> **A character's history may shape future behavior without determining it.**

COMASTA evaluates interpretive support. It does not predict what a character will do, assign behavioral probabilities, model a personality, diagnose psychology, generate characters, or replace authorial judgment.

## What v0.2-draft evaluates

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

COMASTA v0.2-draft has not been validated. The repository contains one historical v0.1 pilot run, T003-R001. That run found a clearer output structure under COMASTA but did not demonstrate superior underlying reasoning. It also had a control limitation because the two conditions did not receive textually identical character-data blocks.

The v0.2-draft tests define controlled and adversarial evaluations. They do not contain fabricated observed results.

## Repository structure

1. [Principles](PRINCIPLES.md)
2. [Specification](SPECIFICATION.md)
3. [Evaluation](EVALUATION.md)
4. [LLM adaptation protocol](PROMPTING.md)
5. [Structured examples](schemas/)
6. [Narrative examples](examples/)
7. [Test protocol and definitions](tests/)
8. [Preserved v0.1 materials](versions/v0.1/)

Existing v0.1 experiment records remain under `tests/results/` and must be treated as historical records rather than v0.2 evidence.

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

[https://axirverse.com](https://axirverse.com)
