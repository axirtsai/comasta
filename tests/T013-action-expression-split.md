# T013 - Action-Expression Split

**Version:** 0.2
**Status:** Observed — PASS WITH OBSERVATION
**Result reference:** [`T013-run-001-evaluation.md`](results/T013-run-001-evaluation.md)

## Purpose

Test whether Action Interpretability and Expression Interpretability are evaluated separately without creating a separate divergence state.

## Supplied input

Use the T003 character and hospital context. Add one EXPLICIT condition:

> Wei-Cheng has never used therapeutic terminology and, during prior family conflict, speaks in short fragments or stops speaking.

## Action target

Wei-Cheng directly confronts his father about years of control.

## Expression target

Wei-Cheng delivers a calm, uninterrupted four-minute monologue using precise therapeutic terms about attachment style, intergenerational trauma, emotional enmeshment, and conditioned avoidance.

## Expected protocol behavior

- Assess the Action and Expression independently.
- The Action may receive `PLAUSIBLE DEVIATION` if its bridge is established.
- The Expression must not inherit that result.
- The exact expression conflicts with supplied communication behavior and lacks supplied support for its vocabulary, uninterrupted delivery, and explicit conceptual framework.
- Expected Expression assessment: epistemic status `SUFFICIENT FOR TARGET`, disposition `ISSUED`, state `UNSUPPORTED`.
- Do not introduce an additional formal state for the difference between the two assessments.

## Failure criteria

- Returns one combined assessment only.
- Assumes crisis automatically produces eloquence or therapeutic self-analysis.
- Invents therapy history, reading, rehearsal, or prior vocabulary.
- Automatically rewrites the monologue.
- Treats the Action assessment as evidence for the Expression assessment.
