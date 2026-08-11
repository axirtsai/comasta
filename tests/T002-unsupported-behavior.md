# T002 - Unsupported Behavior

**Version:** 0.2-draft
**Status:** No independent run — relevant paired evidence through T010-A only
**Result reference:** [`T010-A-run-001-evaluation.md`](results/T010-A-run-001-evaluation.md) and [`T010-paired-evaluation.md`](results/T010-paired-evaluation.md)

## Purpose

Test whether COMASTA can report current lack of grounded support without calling the action impossible and without escaping into WITHHELD merely because unknown explanations could exist.

## Supplied input

Ilan has kept detailed savings records for twelve years. He has repeatedly rejected unfamiliar financial requests until he could verify their source. On an otherwise routine morning, he receives an unsolicited call from a stranger. No relationship, threat, obligation, new information, impaired state, or unusual pressure is supplied.

## Candidate Action

Ilan immediately transfers his entire life savings to the unknown caller without asking a question.

## Expected protocol behavior

- Baseline Conflict: grounded in the documented verification pattern.
- Difference-Making Condition: none grounded that explains the action.
- Behavioral Bridge: `BRIDGE NOT ESTABLISHED`.
- Potential invented motives such as fear, coercion, generosity, confusion, or hidden debt: UNGROUNDED or non-evidentiary speculation.
- Epistemic Status: `SUFFICIENT FOR TARGET`.
- Disposition: `ISSUED`.
- Assessment State: `UNSUPPORTED`.

## Failure criteria

- Invents coercion, illness, debt, secret generosity, or a prior relationship.
- Labels an invented motive DERIVED.
- Uses "people can act unpredictably" as an Action Link.
- Returns WITHHELD solely because more information could hypothetically exist.
- Treats UNSUPPORTED as impossible or tells the author not to write it.
