target:
  type: action
  candidate: Wei-Cheng directly confronts his father about their unresolved relationship.

explicit_claims:
  - id: E1
    claim: Wei-Cheng learned to avoid direct confrontation.
  - id: E2
    claim: Conflict avoidance is HIGH.
  - id: E3
    claim: Wei-Cheng has high attachment, resentment, desire for approval, and unresolved conflict with his father.
  - id: E4
    claim: His father's condition may deteriorate rapidly.
  - id: E5
    claim: This may be Wei-Cheng's last meaningful opportunity to speak with his father.

baseline_conflict:
  established_pattern: Wei-Cheng avoids direct confrontation.
  candidate_action: Wei-Cheng directly confronts his father.

derived_claims:
  - id: D1
    claim: The opportunity for direct conversation may soon disappear.
    depends_on: [E4, E5]

ungrounded_claims: []

speculative_interpretations: []

behavioral_bridge:
  required: true
  bridge_origin: E1, E2
  difference_making_condition: E4, E5
  character_meaning: The potentially final opportunity makes the established unresolved relationship immediately relevant. [E3, E4, E5]
  action_link: The proposed link states only that emotional extremity can make an unusual action understandable.
  substitution_test: Fails; the same link could explain unrelated unusual actions without meaningful revision.
  status: BRIDGE NOT ESTABLISHED
  gaps:
    - No action-specific link connects the grounded conditions to direct confrontation.

unresolved_tensions:
  - Wei-Cheng's conflict avoidance conflicts with his high attachment, desire for approval, and unresolved conflict with his father. [E2, E3]

open_unknowns: []

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: UNSUPPORTED

non_inevitability_statement: This result describes current interpretive support; it does not predict, rank, or exhaust possible actions.
author_questions: []
authorial_decision_reserved: true