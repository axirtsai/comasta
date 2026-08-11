# T003 - Plausible Deviation

**Version:** 0.2-draft
**Status:** Controlled Test Definition - Post-Run-001 Harness Clarification

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

## Condition B - Original compact COMASTA instruction used for Run 001

The following compact instruction is the exact Condition B instruction that produced `T003-B-run-001`. A post-run harness audit found that it omitted material normative definitions from the current COMASTA v0.2-draft protocol. It is retained here to preserve the historical meaning and attribution of Run 001 and must not be used as the revised instruction for future runs.

```text
Perform a COMASTA v0.2-draft assessment using the supplied Candidate Action.

Do not predict behavior, assign probability, rank alternative actions, or invent information.

Identify EXPLICIT claims. For every DERIVED claim, list the EXPLICIT claims on which it depends. Keep speculative interpretations separate from evidence and do not use UNGROUNDED claims as support.

Identify grounded Baseline Conflict. If it exists, evaluate Bridge Origin, Difference-Making Condition, Character Meaning, and Action Link. Apply the Action-Link Substitution Test and return only BRIDGE ESTABLISHED or BRIDGE NOT ESTABLISHED.

Separate Action Interpretability from Expression Interpretability. Identify grounded Unresolved Tensions and target-relevant Open Unknowns.

For each target, return epistemic status, assessment disposition, and an assessment state only when issued. Preserve non-inevitability and authorial authority.
```

Append the same canonical fixture byte-for-byte.

## Condition B - Revised COMASTA instruction for future runs

**Post-Run-001 harness clarification:** This revised instruction applies prospectively. It does not replace or reinterpret the original compact instruction used for `T003-B-run-001`.

```text
Perform a COMASTA v0.2-draft assessment of the supplied Candidate Action and Candidate Expression.

Evaluate whether each externally supplied assessment target can currently be understood from grounded information. Do not convert history, patterns, pressure, contradiction, or authorial intention into behavioral prediction or proof of why one action was selected over alternatives. Keep Pattern Consistency separate from Action Interpretability. Deviation is descriptive, not a penalty.

Do not predict behavior, assign probability, rank alternative actions, identify a most likely action, or invent information.

Treat the Candidate Action and Candidate Expression as assessment targets, not evidence. Their wording may be reproduced in the target field, but the fact that a target is proposed or described does not support its own interpretability and does not permit an EXPLICIT, DERIVED, or UNGROUNDED grounding label. Do not include a target in supporting claims or in depends_on for a DERIVED claim evaluating that target.

Assign identifiers only to relevant evidentiary EXPLICIT claims. Every major claim used as assessment support must have one grounding label. For every DERIVED claim, list the identifiers of the EXPLICIT claims on which it depends. List relevant UNGROUNDED claims separately; they cannot serve as supporting evidence or necessary Behavioral Bridge links. Keep speculative interpretations separate from evidence.

Baseline Conflict identifies a grounded established pattern with which the Candidate Action conflicts. The baseline must be supported by supplied history or repeated behavior. Apply the same rule independently to the Candidate Expression as its own assessment target. If no relevant baseline is established for a target, record NONE ESTABLISHED and omit Behavioral Bridge evaluation for that target.

When a target materially conflicts with a grounded baseline, evaluate a Behavioral Bridge containing:

1. Bridge Origin: identify the grounded established pattern that makes the target a deviation.
2. Difference-Making Condition: identify supplied information that changes the present interpretive situation. It may be a new event, new information, accumulated pressure explicitly present in the record, a newly available opportunity, a removed constraint, or an existing condition made immediately relevant by the current context.
3. Character Meaning: explain why the Difference-Making Condition matters to this character using supplied history, relationship, value, obligation, conflict, attachment, pressure, or another grounded condition. Severity alone is insufficient. Do not invent how the character privately experiences the event.
4. Action Link: explain why the grounded Character Meaning makes this particular Candidate Action interpretable. The link must describe more than emotional intensity, unpredictability, or the fact that the action occurred, and its support must come from independent grounded claims. Apply the same rule independently to the Candidate Expression as its own assessment target.

Return BRIDGE ESTABLISHED only when all of the following are true:

1. Bridge Origin is grounded.
2. Difference-Making Condition is grounded.
3. Character Meaning is EXPLICIT or validly DERIVED.
4. Action Link specifically connects that meaning to the Candidate Action or independently assessed Candidate Expression.
5. Every DERIVED link lists its EXPLICIT dependencies.
6. No necessary link is UNGROUNDED.
7. The Action Link passes the Action-Link Substitution Test.

Otherwise return BRIDGE NOT ESTABLISHED and identify the bridge gaps. The only valid Bridge Status values are BRIDGE ESTABLISHED and BRIDGE NOT ESTABLISHED.

Action-Link Substitution Test: temporarily replace the Candidate Action with an unrelated action while leaving the proposed Action Link unchanged. If the same link still appears to explain the unrelated action with little or no meaningful revision, the link is too generic and the result is BRIDGE NOT ESTABLISHED. A passing link need not prove that the Candidate Action is unique. Multiple actions may each pass through different action-specific links. Do not require an explanation of why this action was selected over other possible actions.

Produce two independent ordinary assessments, one for Action and one for Expression. Each uses the same grounding, epistemic-status, disposition, and assessment-state rules. Neither assessment may inherit the other's result.

Keep grounded opposing conditions simultaneously active as Unresolved Tensions rather than resolving them into one true motive. Identify target-relevant Open Unknowns and do not assume their values.

Use only these values:

Epistemic Status:
- SUFFICIENT FOR TARGET
- CRITICAL CONTEXT MISSING

Assessment Disposition:
- ISSUED
- WITHHELD

Assessment State:
- SUPPORTED
- PLAUSIBLE DEVIATION
- UNSUPPORTED

Bridge Status:
- BRIDGE ESTABLISHED
- BRIDGE NOT ESTABLISHED

Use SUFFICIENT FOR TARGET when the supplied material permits a limited judgment of current support; relevant unknowns may remain. Use CRITICAL CONTEXT MISSING only when a specific missing fact is necessary to determine whether support or a bridge exists, materially different possible values would change the assessment, and selecting a value would invent information.

For each target:
- grounded support with no significant unexplained baseline departure yields SUFFICIENT FOR TARGET, ISSUED, SUPPORTED;
- grounded Baseline Conflict with BRIDGE ESTABLISHED yields SUFFICIENT FOR TARGET, ISSUED, PLAUSIBLE DEVIATION;
- an assessable record in which grounded support or a required bridge is not established yields SUFFICIENT FOR TARGET, ISSUED, UNSUPPORTED;
- a specific critical unknown that prevents responsible classification yields CRITICAL CONTEXT MISSING, WITHHELD, and assessment_state null.

Close with this boundary: The result describes current interpretive support. It does not predict the action, rank it as most likely, or exhaust other possible actions. Final interpretation remains with the author.
```

Append the same canonical fixture byte-for-byte. Do not append the Expected action-assessment pattern, Expression observation, or Failure criteria to the model prompt.

## Harness Revision Record

- `T003-B-run-001` remains a valid observation of the original compact Condition B instruction.
- Run 001 is not treated as a clean test of the full current COMASTA v0.2-draft normative protocol.
- The revised harness is prospective and does not retroactively alter Run 001.
- Future revised-harness observations must use new run identifiers.

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
