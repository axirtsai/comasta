# COMASTA LLM Adaptation Protocol

**Version:** 0.2
**Status:** Experimental v0.2 — Adversarially evaluated under limited recorded conditions; not scientifically or generally validated

This protocol constrains how a language model performs a COMASTA assessment. It does not authorize the model to generate a preferred character action or predict behavior.

## 1. Primary instruction

> Evaluate whether the externally supplied assessment target can currently be understood from grounded information. Do not convert history, patterns, pressure, contradiction, or authorial intention into behavioral prediction.

## 2. Required distinctions

The model must keep separate:

- Pattern Consistency;
- Action Interpretability;
- Expression Interpretability when requested;
- explanation;
- prediction;
- current lack of support;
- critical missing context.

## 3. Required procedure

1. Read the Candidate Action and supplied assessment scope; treat them respectively as the assessment target and non-evidentiary metadata.
2. Assign identifiers only to relevant evidentiary EXPLICIT claims, excluding the assessment target and authorial-scope metadata.
3. Identify grounded supporting and conflicting conditions.
4. Identify Baseline Conflict or `NONE ESTABLISHED`.
5. For every DERIVED claim, list its EXPLICIT dependencies.
6. List UNGROUNDED claims separately.
7. Keep speculative interpretations outside supporting evidence.
8. If Baseline Conflict exists, evaluate Bridge Origin, Difference-Making Condition, Character Meaning, and Action Link.
9. Apply the Action-Link Substitution Test.
10. Identify grounded Unresolved Tensions and target-relevant Open Unknowns.
11. Determine epistemic status and assessment disposition.
12. If disposition is ISSUED, return exactly one core assessment state.
13. Preserve non-inevitability and authorial authority.

## 4. Valid outputs

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

### Behavioral Bridge status

- `BRIDGE ESTABLISHED`
- `BRIDGE NOT ESTABLISHED`

When disposition is `WITHHELD`, do not issue an assessment state.

## 5. Prohibited behavior

The model must not:

- predict what the character will do;
- identify a most likely or objectively true reaction;
- assign behavioral probabilities or numeric plausibility scores;
- infer behavior directly from a personality label;
- treat prior behavior as a deterministic rule;
- treat deviation as a penalty;
- invent trauma, motives, memories, relationships, events, values, or emotional states;
- label a culturally familiar or psychologically conventional guess as DERIVED without textual grounding;
- use a speculative or UNGROUNDED claim as evidence;
- silently complete unknown information;
- treat missing evidence as negative evidence;
- resolve contradiction into one true motive;
- use authorial intention as behavioral evidence;
- assign Authorial Scope, Interpretive Intention, or Protected Ambiguity a grounding label, place it in supporting claims or `depends_on`, or use it as a Behavioral Bridge component;
- use protected ambiguity to upgrade an assessment;
- assign a Candidate Action or Candidate Expression a grounding label merely because it is the assessment target;
- place a Candidate Action in supporting claims or in `depends_on` for a DERIVED claim evaluating that action;
- use the fact that a Candidate Action is proposed, described, or occurs as support for that action;
- automatically rewrite the character, dialogue, or scene.

## 6. Behavioral Bridge instruction

Evaluate a Behavioral Bridge only when a grounded Baseline Conflict exists.

Return `BRIDGE ESTABLISHED` only if:

- Bridge Origin is grounded;
- Difference-Making Condition is grounded;
- Character Meaning is traceable to supplied information;
- Action Link specifically explains the Candidate Action;
- every DERIVED link identifies its EXPLICIT dependencies;
- no necessary link is UNGROUNDED;
- the Action Link fails to explain an unrelated substituted action without meaningful revision.

Otherwise return `BRIDGE NOT ESTABLISHED` and identify the gap.

## 7. Unsupported versus withheld

Return an issued `UNSUPPORTED` assessment when the current material is sufficient to inspect but contains no grounded support or required bridge.

Use disposition `WITHHELD` only when a named missing fact materially controls the outcome and assuming either value would fabricate information.

Do not withhold merely because a character is not fully known.

## 8. Action and Expression targets

If the request includes a specific dialogue line, delivery style, timing, or physical expression, separate the targets when their support may differ.

Do not create an Action-Expression Divergence state. Report two ordinary assessments.

Do not infer expression support from action support.

## 9. Minimal structured response

```yaml
target:
  type: action
  candidate:

explicit_claims:
  - id:
    claim:

baseline_conflict:

derived_claims:
  - id:
    claim:
    depends_on: []

ungrounded_claims: []

speculative_interpretations: []

behavioral_bridge:
  required:
  bridge_origin:
  difference_making_condition:
  character_meaning:
  action_link:
  substitution_test:
  status:
  gaps: []

unresolved_tensions: []
open_unknowns: []

epistemic_status:
assessment_disposition:
assessment_state:

non_inevitability_statement:
author_questions: []
authorial_decision_reserved: true
```

Omit the Behavioral Bridge object when no grounded Baseline Conflict exists. Set `assessment_state` to `null` when disposition is `WITHHELD`.

The `target.candidate` field may reproduce the supplied Candidate Action or Candidate Expression without creating an evidentiary claim. Authorial-scope metadata may constrain the response but must remain outside `explicit_claims`, `derived_claims`, `ungrounded_claims`, their `depends_on` lists, and the Behavioral Bridge components.

Every Unresolved Tension must cite grounded claims. Open Unknowns must be relevant to the current target.

## 10. Required closing boundary

Every full assessment must preserve this meaning:

> The result describes current interpretive support. It does not predict the action, rank it as most likely, or exhaust other possible actions. Final interpretation remains with the author.

## 11. Model independence and evidence boundary

COMASTA is conceptually independent of a specific language-model provider. A model implements the constrained interpretation procedure; it does not validate the procedure merely by producing a compliant answer.

No current repository evidence establishes that v0.2 improves underlying LLM reasoning.
