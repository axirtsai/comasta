# T010 - Unsupported vs Critical Missing

**Version:** 0.2-draft
**Status:** Observed — Paired PASS WITH OBSERVATION
**Result reference:** [`T010-A-run-001-evaluation.md`](results/T010-A-run-001-evaluation.md), [`T010-B-run-001-evaluation.md`](results/T010-B-run-001-evaluation.md), and [`T010-paired-evaluation.md`](results/T010-paired-evaluation.md)

## Purpose

Test whether COMASTA distinguishes an assessable lack of current support from a specifically identified missing fact that controls the assessment.

## Case A - Unsupported

Use T002 unchanged. No supplied event or identified missing item controls whether Ilan has a grounded reason to transfer his savings.

Expected hypothesis:

- Epistemic Status: `SUFFICIENT FOR TARGET`.
- Disposition: `ISSUED`.
- Assessment State: `UNSUPPORTED`.

## Case B - Critical missing context

Use T005 unchanged. The intentionally omitted note is the only supplied possible Difference-Making Condition, and its value controls whether a bridge can be evaluated.

Expected hypothesis:

- Epistemic Status: `CRITICAL CONTEXT MISSING`.
- Disposition: `WITHHELD`.
- Assessment State: none.

## Failure criteria

- WITHHELD in both cases because people are never fully known.
- UNSUPPORTED in both cases because missing information is treated as negative evidence.
- Invents a controlling fact in either case.
- Cannot name the specific critical dependency in Case B.
