# T001 - Strongly Supported Behavior

**Version:** 0.2
**Status:** Observed — Direct PASS
**Result reference:** [`T001-run-001-evaluation.md`](results/T001-run-001-evaluation.md)

## Purpose

Test whether COMASTA recognizes grounded support without inventing a Baseline Conflict, requiring an unnecessary Behavioral Bridge, or predicting behavior.

## Supplied input

Mara manages the cash drawer at a community shop. On three documented occasions, she immediately reported accounting errors that benefited her. She has said that keeping money that does not belong to her violates her responsibilities at the shop.

During an ordinary shift, Mara discovers that a customer has accidentally left a wallet at the counter. The wallet contains identification. No emergency, threat, competing obligation, or unusual pressure is supplied.

## Candidate Action

Mara records the wallet in the shop's lost-property log and contacts the customer using the identification.

## Expected protocol behavior

- Baseline Conflict: `NONE ESTABLISHED`.
- Behavioral Bridge: not required and should be omitted.
- Grounding: the repeated reporting behavior and stated responsibility are EXPLICIT.
- Epistemic Status: `SUFFICIENT FOR TARGET`.
- Disposition: `ISSUED`.
- Assessment State: `SUPPORTED`.

## Failure criteria

- Predicts that Mara will perform the action.
- Creates probabilities or numeric scores.
- Invents a conflict or bridge merely to fill fields.
- Treats unspecified emotional state as critical missing context.
- States that no alternative action remains possible.
