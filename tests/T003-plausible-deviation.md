# T003 - Plausible Deviation

**Version:** 0.2-draft
**Status:** Controlled Test Definition - No v0.2 Observed Result

The historical v0.1 definition is preserved under `versions/v0.1/tests/`. T003-R001 remains unchanged under `tests/results/`.

## Purpose

Test whether COMASTA distinguishes low Pattern Consistency from Action Interpretability while preserving contradiction, unknown information, and non-inevitability.

The test also observes whether a separate Expression assessment surfaces a concern that the historical baseline response identified but the historical COMASTA response did not.

## Canonical input fixture

Both conditions must append the exact, unmodified contents of:

`tests/fixtures/T003-character-context.md`

Record the fixture hash before each run. Do not insert COMASTA concepts, disclaimers, or explanatory notes into the fixture for either condition.

## Condition A - Baseline instruction

```text
Based only on the supplied character and situation information, evaluate whether the Candidate Action makes sense for the character. Also comment separately on whether the exact expression is supported. Explain your reasoning. Do not add facts that are not supplied.
```

Append the canonical fixture byte-for-byte.

## Condition B - COMASTA instruction

```text
Perform a COMASTA v0.2-draft assessment using the supplied Candidate Action.

Do not predict behavior, assign probability, rank alternative actions, or invent information.

Identify EXPLICIT claims. For every DERIVED claim, list the EXPLICIT claims on which it depends. Keep speculative interpretations separate from evidence and do not use UNGROUNDED claims as support.

Identify grounded Baseline Conflict. If it exists, evaluate Bridge Origin, Difference-Making Condition, Character Meaning, and Action Link. Apply the Action-Link Substitution Test and return only BRIDGE ESTABLISHED or BRIDGE NOT ESTABLISHED.

Separate Action Interpretability from Expression Interpretability. Identify grounded Unresolved Tensions and target-relevant Open Unknowns.

For each target, return epistemic status, assessment disposition, and an assessment state only when issued. Preserve non-inevitability and authorial authority.
```

Append the same canonical fixture byte-for-byte.

## Control requirement

The character, context, unknowns, Candidate Action, and exact expression must be identical in Conditions A and B. The only difference is the instruction layer above the fixture.

Any difference in fixture bytes invalidates the run as a controlled A/B comparison.

## Expected action-assessment pattern

- Baseline Conflict: direct confrontation conflicts with avoidance, low disclosure, and withdrawal.
- Bridge Origin: EXPLICIT established patterns.
- Difference-Making Condition: rapid deterioration and final meaningful opportunity, EXPLICIT.
- Character Meaning: DERIVED from attachment, resentment, approval desire, unresolved conflict, and possible irreversible loss.
- Action Link: confrontation directly addresses the supplied unresolved conflict before conversation may become unavailable.
- Bridge Status: `BRIDGE ESTABLISHED` if all DERIVED dependencies are exposed and the Action Link passes substitution.
- Epistemic Status: `SUFFICIENT FOR TARGET`.
- Disposition: `ISSUED`.
- Action Assessment: `PLAUSIBLE DEVIATION`.

## Expression observation

The exact fluency and emotional precision may have different support from the confrontation itself. The test does not prescribe an expected expression state before a run; it requires the model to assess the expression separately without inventing delivery details.

## Failure criteria

- Treats low consistency as sufficient evidence of implausibility.
- Treats current pressure as making confrontation inevitable.
- Labels UNGROUNDED immediate emotion as DERIVED.
- Uses a generic "extreme pressure causes unusual behavior" Action Link.
- Resolves attachment and resentment into one true motive.
- Silently completes the known unknowns.
- Automatically transfers the Action result to the Expression target.
- Claims v0.2 improves reasoning based on one run.
