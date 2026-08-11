# COMASTA Evaluation Model

**Version:** 0.2-draft
**Status:** Experimental Specification - Not Yet Validated

COMASTA uses categorical, non-additive evaluation. It does not calculate psychological scores, behavioral probabilities, or a most-likely action.

## 1. Evidence is relational

A condition has no fixed behavioral output. Attachment may support staying, leaving, confronting, remaining silent, or another action through different grounded paths.

The relevant question is:

> How does this supplied condition support or conflict with this Candidate Action in the current situation?

This permits multiple actions to remain interpretable without making every action supported.

## 2. Evaluation sequence

For each assessment target:

1. Identify the Candidate Action or specific Expression.
2. Inventory relevant EXPLICIT claims and assign identifiers.
3. Identify a grounded Baseline Conflict, or record `NONE ESTABLISHED`.
4. State supporting DERIVED claims and list their EXPLICIT dependencies.
5. Expose UNGROUNDED claims and non-evidentiary speculative interpretations.
6. If Baseline Conflict exists, evaluate the Behavioral Bridge.
7. Apply the Action-Link Substitution Test.
8. Identify grounded Unresolved Tensions and relevant Open Unknowns.
9. Determine whether any unknown is critical to the target.
10. Set epistemic status and assessment disposition.
11. If disposition is ISSUED, return one core assessment state.
12. Preserve non-inevitability and authorial authority.

The order is intended to expose assumptions before classification.

## 3. Grounding rules

### 3.1 EXPLICIT claims

An EXPLICIT claim must be directly recoverable from supplied material. Paraphrase is allowed if it does not add meaning.

### 3.2 DERIVED claims

A DERIVED claim must:

- cite one or more EXPLICIT claim identifiers;
- remain within the interpretive scope of those claims;
- avoid adding a hidden motive, memory, value, trauma, relationship, event, or emotional state;
- be stated as an interpretation rather than an established psychological fact.

Common human behavior, genre convention, or therapeutic language is not sufficient provenance.

Example:

```yaml
- id: D1
  claim: The opportunity for direct conversation may soon disappear.
  grounding: DERIVED
  depends_on:
    - E4  # doctors say the condition may rapidly deteriorate
    - E5  # this may be the final meaningful opportunity to speak
```

### 3.3 UNGROUNDED claims

An UNGROUNDED claim has no adequate source in the supplied material. It cannot become evidence merely because it is psychologically conceivable.

### 3.4 Speculative interpretations

Speculative possibilities must appear outside supporting claims. They may help an author see possible additions or ambiguities, but the assessment must remain unchanged if they are removed.

## 4. Necessary links

A necessary link is a claim without which the current explanation would not establish support or a Behavioral Bridge.

If any necessary link is UNGROUNDED, the claimed bridge is `BRIDGE NOT ESTABLISHED`.

An evaluator may not avoid this rule by relabeling an indispensable hidden assumption as optional commentary.

## 5. Behavioral Bridge

A Behavioral Bridge is evaluated only when the Candidate Action materially conflicts with a grounded baseline.

### 5.1 Bridge Origin

Identify the grounded established pattern that makes the action a deviation.

### 5.2 Difference-Making Condition

Identify supplied information that changes the present interpretive situation. It may be a new event, new information, accumulated pressure explicitly present in the record, a newly available opportunity, a removed constraint, or an existing condition made immediately relevant by the current context.

It must not be a generic statement that "people sometimes change."
### 5.3 Character Meaning

Explain why the Difference-Making Condition matters to this character using supplied history, relationship, value, obligation, conflict, attachment, pressure, or another grounded condition.

Severity alone is insufficient. Character Meaning must not invent how the character privately experiences the event.

### 5.4 Action Link

Explain why the grounded Character Meaning makes this particular Candidate Action interpretable.

The Action Link must describe more than emotional intensity, unpredictability, or the fact that the action occurred.

## 6. Bridge establishment rule

Return `BRIDGE ESTABLISHED` only when all of the following are true:

1. Bridge Origin is grounded.
2. Difference-Making Condition is grounded.
3. Character Meaning is EXPLICIT or validly DERIVED.
4. Action Link specifically connects that meaning to the Candidate Action.
5. Every DERIVED link lists its EXPLICIT dependencies.
6. No necessary link is UNGROUNDED.
7. The Action Link passes the Action-Link Substitution Test.

Otherwise return `BRIDGE NOT ESTABLISHED` and identify the bridge gaps.

The statuses do not measure probability or strength.

`BRIDGE NOT ESTABLISHED` may result from an UNGROUNDED necessary link or from a specifically identified critical unknown. Epistemic status and assessment disposition distinguish those cases; the bridge label alone does not.

## 7. Action-Link Substitution Test

Temporarily replace the Candidate Action with an unrelated action while leaving the proposed Action Link unchanged.

If the same link still appears to explain the unrelated action with little or no modification, the link is too generic. Return `BRIDGE NOT ESTABLISHED`.

Example of a failing link:

> The situation is emotionally extreme, so an unusual action becomes understandable.

That sentence could be attached to confrontation, theft, disappearance, violence, confession, or nearly anything else.

A passing link need not prove that the Candidate Action is unique. Multiple actions may each pass through different, action-specific links.

## 8. Determining epistemic status

### SUFFICIENT FOR TARGET

Use when the supplied material permits a limited judgment of current support. Relevant unknowns may remain.

### CRITICAL CONTEXT MISSING

Use only when:

- a specific fact is missing;
- the fact is necessary to determine whether the proposed support or bridge exists;
- materially different possible values would change the assessment;
- selecting a value would invent information.

"More context could always help" does not satisfy this rule.

## 9. Disposition and state logic

| Condition | Epistemic Status | Disposition | Assessment State |
|---|---|---|---|
| Grounded support, no significant unexplained baseline departure | SUFFICIENT FOR TARGET | ISSUED | SUPPORTED |
| Grounded Baseline Conflict and BRIDGE ESTABLISHED | SUFFICIENT FOR TARGET | ISSUED | PLAUSIBLE DEVIATION |
| Current material is assessable but grounded support or a required bridge is not established | SUFFICIENT FOR TARGET | ISSUED | UNSUPPORTED |
| A specific critical unknown prevents responsible classification | CRITICAL CONTEXT MISSING | WITHHELD | No state issued |

Missing evidence is not negative evidence. UNSUPPORTED describes the limits of current supplied support. WITHHELD describes the inability to issue that judgment because of a critical unresolved fact.

## 10. Contradiction

Opposing grounded conditions remain visible as Unresolved Tensions. They do not cancel each other and do not automatically create a deviation.

An issued action may be SUPPORTED while important contradictions remain.

## 11. Action and Expression

When a scene includes a specific expression form, evaluate action and expression independently.

Example targets:

- Action: confronts his father.
- Expression: delivers a calm, uninterrupted monologue using precise psychological terminology.

The Expression assessment must not inherit the Action result automatically. It uses the same grounding and state rules and does not trigger automatic rewriting.

## 12. Comparative analysis

When several Candidate Actions are submitted, evaluate each independently. Comparative notes may identify differences in support structure, missing context, or bridge construction.

Do not rank the actions, assign likelihoods, or state which one the character would really choose unless a separate system outside COMASTA is explicitly being used. Such a system is not defined by v0.2-draft.

## 13. No automatic repair

COMASTA may expose:

- an UNGROUNDED necessary assumption;
- an unestablished bridge;
- a critical unknown;
- grounded contradiction;
- a difference between action and expression support.

It must not automatically rewrite dialogue, backstory, motivation, or scene structure. Author Questions may identify unresolved information, but unanswered questions remain unknown.
