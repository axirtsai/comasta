# COMASTA Character Action Interpretability Specification

**Version:** 0.2-draft
**Status:** Experimental Specification - Not Yet Validated

COMASTA evaluates whether an externally supplied Candidate Action can currently be understood from grounded character and situational information.

It is not a character generator, personality model, psychological model, behavior prediction engine, probability system, or replacement for authorial judgment.

> **A character's history may shape future behavior without determining it.**

## 1. Assessment target

Every assessment begins with a Candidate Action supplied by the author or calling application.

```yaml
candidate_action:
  actor: Wei-Cheng
  action: confronts his father directly at the hospital
```

Submitting an action for assessment does not imply that it is inevitable, most likely, optimal, canonical, psychologically correct, or narratively preferable.

COMASTA does not generate a preferred action by default.

## 2. Recommended input domains

A v0.2-draft input may contain:

- character history;
- established behavioral patterns;
- relationships;
- current state;
- immediate context;
- pressures and stakes;
- a Candidate Action;
- known unknowns;
- optional interpretive scope or protected ambiguity.

Input must distinguish supplied information from unknown information. An unknown value is not permission to infer the value most convenient to the assessment.

Authorial intention may define scope, for example that precise motive must remain unresolved. It is not behavioral evidence.

## 3. Pattern Consistency and Action Interpretability

COMASTA separates:

- **Pattern Consistency:** whether an action resembles established behavior;
- **Action Interpretability:** whether the action can be understood from grounded current conditions.

These are not equivalent. Deviation is descriptive, not a penalty.

## 4. Baseline Conflict

Baseline Conflict identifies a grounded established pattern with which the Candidate Action conflicts.

```yaml
baseline_conflict:
  established_pattern: avoids direct confrontation with his father
  candidate_action: directly confronts his father
```

A baseline must be supported by supplied history or repeated behavior. COMASTA must not invent a stable trait from a single unrelated event.

If no relevant baseline is established, the assessment records `NONE ESTABLISHED` or omits Behavioral Bridge evaluation. It must not create a conflict merely to fill an output field.

Baseline Conflict does not reduce a score. COMASTA has no behavioral plausibility score.

## 5. Grounding labels

Every major claim used as assessment support has one grounding label.

### EXPLICIT

Directly supplied by the source material.

### DERIVED

A bounded interpretation traceable to supplied information. Every DERIVED claim must identify the EXPLICIT claim identifiers on which it depends.

DERIVED does not mean psychologically conventional, intuitively likely, or generally human. It must remain close to the supplied material.

### UNGROUNDED

A claim requiring information not supplied by the source material.

UNGROUNDED claims cannot serve as supporting evidence or as necessary Behavioral Bridge links.

### Speculative interpretations

Speculative interpretations may be displayed in a separate section as possibilities. They are not grounding labels, do not count as supporting evidence, and cannot upgrade an assessment.

## 6. Behavioral Bridge

When a Candidate Action conflicts with a grounded baseline, COMASTA evaluates a Behavioral Bridge containing:

1. Bridge Origin
2. Difference-Making Condition
3. Character Meaning
4. Action Link

The only valid bridge statuses are:

- `BRIDGE ESTABLISHED`
- `BRIDGE NOT ESTABLISHED`

A bridge may be established only when:

- the baseline is grounded;
- the Difference-Making Condition is grounded;
- Character Meaning is traceable to supplied information;
- the Action Link specifically explains the Candidate Action;
- no necessary link depends on UNGROUNDED information;
- the Action Link passes the Action-Link Substitution Test defined in EVALUATION.md.

`BRIDGE NOT ESTABLISHED` means that the current material does not establish the required path. It does not mean that no human explanation could exist.

Multiple different Candidate Actions may each have distinct valid bridges. A bridge explains interpretability, not probability.

## 7. Core assessment states

### SUPPORTED

The Candidate Action can be responsibly understood from grounded information without requiring a significant unexplained departure from an established pattern.

### PLAUSIBLE DEVIATION

The Candidate Action conflicts with a grounded established pattern, and a `BRIDGE ESTABLISHED` result makes that departure interpretable.

The baseline remains valid. The action does not prove that the character has permanently changed or overcome the prior pattern.

### UNSUPPORTED

The current material does not provide grounded support for the Candidate Action, or a required Behavioral Bridge is not established.

UNSUPPORTED does not mean impossible, prohibited, badly written, or contrary to what a real person could do.

## 8. Assessment disposition

### ISSUED

The available material permits one of the three core assessment states to be issued.

### WITHHELD

A specific critical unknown prevents a responsible distinction between support and non-support. When disposition is `WITHHELD`, no core assessment state is issued.

`WITHHELD` is not a fourth assessment state.

## 9. Epistemic status

### SUFFICIENT FOR TARGET

The supplied information is sufficient for the limited assessment target. This does not mean the character is fully known or that all uncertainty has been eliminated.

### CRITICAL CONTEXT MISSING

One or more identified missing facts materially determine whether the proposed interpretation can be grounded. Selecting a value for the missing fact would fabricate information.

This normally requires disposition `WITHHELD`.

## 10. Unsupported versus critical missing context

Missing evidence is not negative evidence.

- Use `UNSUPPORTED` when the current record is assessable but contains no grounded support for the action or required bridge.
- Use `WITHHELD` with `CRITICAL CONTEXT MISSING` when a specific missing fact controls whether the claimed support or bridge exists.

An evaluator must identify the critical fact and explain why different possible values would materially change the assessment. General statements such as "More information might help" are insufficient for withholding.

## 11. Open Unknowns

Open Unknowns list unresolved information relevant to the current target. They must not become assumed facts.

An assessment must not attempt to inventory every unknown aspect of a person. Non-relevant unknowns are omitted.

## 12. Unresolved Tensions

Unresolved Tensions identify grounded conditions that remain simultaneously active and pull in different directions.

They do not require resolution. They also cannot contain invented future feelings, hypothetical regret, or hidden motives unless those are explicitly supplied.

Contradiction alone does not create Baseline Conflict and does not automatically require a Behavioral Bridge.

## 13. Action and Expression Interpretability

The primary target is Action Interpretability.

When a Candidate Action includes a specific form of dialogue, delivery, timing, or physical expression, the assessment may separate:

- Action Interpretability
- Expression Interpretability

Each target uses the same grounding labels, disposition, epistemic status, and assessment states.

The results may differ. v0.2-draft does not define a large expression taxonomy and does not create an Action-Expression Divergence state.

## 14. Authorial ambiguity and authority

An author may protect a motive or condition as intentionally unresolved. COMASTA must not resolve that ambiguity by default.

Protected ambiguity:

- limits the scope of interpretation;
- does not count as behavioral evidence;
- cannot establish a Behavioral Bridge;
- cannot upgrade an unsupported action.

The author retains final interpretive authority and may deliberately choose an unsupported or partially unexplained action.

## 15. Non-inevitability requirement

Every issued assessment must preserve the following boundary:

> This assessment describes current interpretive support. It does not predict that the action will occur, identify it as most likely, or exhaust other possible actions.

## 16. Minimal assessment output

A complete action assessment contains:

- Candidate Action;
- relevant Baseline Conflict or `NONE ESTABLISHED`;
- grounded supporting claims and their grounding labels;
- EXPLICIT dependencies for every DERIVED claim;
- relevant UNGROUNDED claims;
- any speculative interpretations in a non-evidentiary section;
- Behavioral Bridge when required;
- relevant Open Unknowns;
- grounded Unresolved Tensions;
- epistemic status;
- assessment disposition;
- assessment state when issued;
- non-inevitability statement;
- authorial authority statement.

Optional Author Questions may expose critical missing information. Unanswered questions remain unknown.

## 17. Validation boundary

COMASTA v0.2-draft is an experimental specification. Its structure is intended to make interpretive assumptions more visible and bounded.

The current repository does not contain controlled evidence that v0.2 improves underlying language-model reasoning.
