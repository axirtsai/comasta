```yaml
target:
  type: action
  candidate: "Wei-Cheng directly confronts his father about years of control."

explicit_claims:
  - id: E1
    claim: "Wei-Cheng learned to avoid direct confrontation."
    grounding: EXPLICIT
  - id: E2
    claim: "Conflict avoidance is HIGH."
    grounding: EXPLICIT
  - id: E3
    claim: "His father frequently made decisions regarding Wei-Cheng's education, work, and personal relationships."
    grounding: EXPLICIT
  - id: E4
    claim: "Attachment, resentment, desire for approval, and unresolved conflict in the relationship with his father are HIGH."
    grounding: EXPLICIT
  - id: E5
    claim: "Doctors indicate that his father's condition may deteriorate rapidly."
    grounding: EXPLICIT
  - id: E6
    claim: "Wei-Cheng is told this may be his last meaningful opportunity to speak with his father."
    grounding: EXPLICIT

baseline_conflict:
  established_pattern: "Wei-Cheng avoids direct confrontation."
  candidate_action: "Wei-Cheng directly confronts his father about years of control."

derived_claims:
  - id: D1
    claim: "The current opportunity for a meaningful conversation with his father may soon disappear."
    grounding: DERIVED
    depends_on: [E5, E6]
  - id: D2
    claim: "A direct confrontation about the father's control can address supplied unresolved conflict concerning that control."
    grounding: DERIVED
    depends_on: [E3, E4]

ungrounded_claims: []

speculative_interpretations: []

behavioral_bridge:
  required: true
  bridge_origin: "Wei-Cheng's established avoidance of direct confrontation. (E1, E2)"
  difference_making_condition: "His father's possible rapid deterioration and the possible last meaningful opportunity to speak. (E5, E6)"
  character_meaning: "That narrowing opportunity is specifically relevant to the supplied high attachment and unresolved conflict in the father-son relationship. (E4, D1)"
  action_link: "Because the unresolved conflict concerns the father's repeated control, directly confronting him about that control is an action-specific way of addressing that supplied conflict before the opportunity may disappear. (E3, E4, D1, D2)"
  substitution_test: "Replacing confrontation with an unrelated action would not preserve this link without revision, because the link depends on addressing the supplied conflict about control."
  status: BRIDGE ESTABLISHED
  gaps: []

unresolved_tensions:
  - claims: [E1, E2, E4]
    tension: "Established conflict avoidance remains active alongside high attachment, resentment, desire for approval, and unresolved conflict with his father."

open_unknowns:
  - "Wei-Cheng's precise emotional state."
  - "His father's attitude when Wei-Cheng enters the room."
  - "Whether another family member is present."
  - "Wei-Cheng's exact conscious motive."

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: PLAUSIBLE DEVIATION

non_inevitability_statement: "This result describes current interpretive support. It does not predict the action, rank it as most likely, or exhaust other possible actions."
author_questions: []
authorial_decision_reserved: true
```

```yaml
target:
  type: expression
  candidate: "Wei-Cheng delivers a calm, uninterrupted four-minute monologue using precise therapeutic terms about attachment style, intergenerational trauma, emotional enmeshment, and conditioned avoidance."

explicit_claims:
  - id: E1
    claim: "Direct emotional disclosure is LOW."
    grounding: EXPLICIT
  - id: E2
    claim: "During prior family conflict, Wei-Cheng speaks in short fragments or stops speaking."
    grounding: EXPLICIT
  - id: E3
    claim: "Wei-Cheng has never used therapeutic terminology."
    grounding: EXPLICIT
  - id: E4
    claim: "His father's condition may deteriorate rapidly, and this may be Wei-Cheng's last meaningful opportunity to speak with him."
    grounding: EXPLICIT

baseline_conflict:
  established_pattern: "During prior family conflict, Wei-Cheng uses short fragments or stops speaking; direct emotional disclosure is low, and he has never used therapeutic terminology."
  candidate_action: "A calm, uninterrupted four-minute monologue using precise therapeutic terminology."

derived_claims:
  - id: D1
    claim: "The immediate context makes a conversation with his father time-limited."
    grounding: DERIVED
    depends_on: [E4]

ungrounded_claims:
  - claim: "The supplied material establishes a basis for Wei-Cheng to use the specified precise therapeutic terminology."
    grounding: UNGROUNDED
  - claim: "The supplied material establishes a basis for the specified calm, uninterrupted four-minute delivery during family conflict."
    grounding: UNGROUNDED

speculative_interpretations: []

behavioral_bridge:
  required: true
  bridge_origin: "Low direct emotional disclosure, prior fragmentary or stopped speech under family conflict, and no prior therapeutic terminology. (E1, E2, E3)"
  difference_making_condition: "The conversation may be a final meaningful opportunity. (E4)"
  character_meaning: "The time-limited opportunity makes speaking presently relevant. (D1)"
  action_link: "No grounded link establishes the particular sustained, calm, terminology-heavy delivery."
  substitution_test: "Not passed: the available time-limited-conversation link does not specifically explain this expression form."
  status: BRIDGE NOT ESTABLISHED
  gaps:
    - "A necessary basis for the specified therapeutic vocabulary is not supplied."
    - "A necessary basis for the specified calm, uninterrupted four-minute delivery is not supplied."

unresolved_tensions:
  - claims: [E1, E2, E4]
    tension: "The immediate opportunity to speak is present while the established family-conflict expression pattern remains fragmentary or withdrawn."

open_unknowns:
  - "Wei-Cheng's precise emotional state."
  - "His father's attitude when Wei-Cheng enters the room."
  - "Whether another family member is present."

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: UNSUPPORTED

non_inevitability_statement: "This result describes current interpretive support. It does not predict the expression, rank it as most likely, or exhaust other possible expressions. Final interpretation remains with the author."
author_questions: []
authorial_decision_reserved: true
```