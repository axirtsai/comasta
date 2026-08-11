# COMASTA v0.2

**Status:** Experimental — Adversarially evaluated under limited recorded conditions; not scientifically or generally validated.

## What v0.2 is

COMASTA v0.2 is an experimental specification for evaluating the interpretability of externally supplied Candidate Actions and Candidate Expressions from grounded character and situational information.

It evaluates current interpretive support. It is not a behavior predictor, probability system, personality model, psychology model, character generator, or replacement for authorial judgment.

## What changed from v0.1

v0.2 formalizes and clarifies:

- the separation of Pattern Consistency from Action Interpretability;
- separate assessment of Candidate Actions and Candidate Expressions when needed;
- `EXPLICIT`, `DERIVED`, and `UNGROUNDED` grounding labels, including direct EXPLICIT dependencies for DERIVED claims;
- the distinction among assessment state, assessment disposition, and epistemic status;
- the four-part Behavioral Bridge and Action-Link Substitution Test;
- the rule that assessment targets and authorial intention are not behavioral evidence;
- preservation of Open Unknowns, Unresolved Tensions, non-inevitability, and authorial authority;
- a controlled and adversarial validation record with preserved failures and observations.

The historical v0.1 materials remain preserved under `versions/v0.1/`. Historical result artifacts were not rewritten during release promotion.

## Core normative boundaries

- Use only grounded character and situational information as assessment support.
- Do not treat history, patterns, pressure, contradiction, or authorial intention as behavioral prediction or determinism.
- Treat Candidate Actions and Candidate Expressions as assessment targets, not as evidence supporting themselves.
- Keep speculative interpretations separate from evidence; `UNGROUNDED` claims cannot support an assessment or establish a Behavioral Bridge.
- Distinguish an assessable lack of support from a specifically identified missing fact that requires withholding assessment.
- Require a grounded, action-specific Behavioral Bridge when a target materially conflicts with an established baseline.
- Preserve Action Interpretability and Expression Interpretability as separate assessments when both are evaluated.
- Preserve non-inevitability: an assessment does not identify what the character will do or what action is most likely.
- Preserve authorial authority: an author may deliberately choose an unsupported or partially unexplained action.

## Validation record

The record below summarizes only the preserved observations under their recorded conditions. A PASS applies to the identified test and run; it is not general validation.

| Test | Release record |
|---|---|
| T001 | Direct **PASS**. |
| T002 | **No independent run**; related evidence through T010-A only. |
| T003 | Controlled Run 001 **FAIL**; Controlled Run 002 observed the core expected action pattern but remained a strict provenance **FAIL**. Both controlled runs remain strict failures. |
| T004 | Direct **PASS**. |
| T005 | **No independent run**; related evidence through T010-B only. |
| T006 | **NOT RUN**. |
| T007 | Controlled blind **PASS** plus positive control; the non-blind pilot is preserved separately and is not controlled validation evidence. |
| T008 | **PASS WITH OBSERVATION**. |
| T009 | **PASS WITH OBSERVATION**. |
| T010 | Paired **PASS WITH OBSERVATION**. |
| T011 | Initial **FAIL** → clarification → regression **PASS**. The initial failure remains part of the record. |
| T012 | Direct **PASS**. |
| T013 | **PASS WITH OBSERVATION**. |
| T014 | **NOT RUN**. |
| T015 | Repeated-run **PASS WITH MINOR OBSERVATION** under its recorded runtime only. |

See [`tests/results/README.md`](tests/results/README.md) for exact run identifiers, evidence types, observations, limitations, and recorded runtime-metadata availability.

## Known limitations

- Evaluation coverage is limited to the preserved tests and recorded execution conditions.
- T002 and T005 do not have independent runs; their related evidence comes only from the T010 pair.
- T006 and T014 were not run.
- T003 retains two controlled strict failures.
- T011 requires the full failure, clarification, and regression history to interpret its regression PASS.
- T008, T009, T010, T013, and T015 retain documented observations or limitations alongside their PASS results.
- Full runtime metadata is not available for every recorded run.
- T015 demonstrates repeated-run consistency only for its frozen input and recorded runtime, not across models or configurations.
- Natural-language grounding and interpretability distinctions still require bounded human or model judgment.

## Explicit non-claims

COMASTA v0.2 makes:

- no scientific validation claim;
- no psychological validation claim;
- no statistical reliability claim;
- no cross-model reliability claim;
- no claim of improved underlying LLM reasoning;
- no claim to predict human behavior;
- no claim of general superiority to baseline prompting.

## Deferred work

- T006 execution;
- T014 execution;
- possible independent T002 and T005 runs;
- T008 auxiliary-link formalization;
- T013 target-neutral field naming;
- broader runtime and model replication.
