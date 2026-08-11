target:
  type: action
  candidate: Ilan immediately transfers his entire life savings to an unknown caller without asking a question.

explicit_claims:
  - id: E1
    claim: Ilan has kept detailed savings records for twelve years.
  - id: E2
    claim: Ilan has repeatedly rejected unfamiliar financial requests until verifying their source.
  - id: E3
    claim: The call is unsolicited, from a stranger, and occurs on an otherwise routine morning.

baseline_conflict:
  established_pattern: E2
  candidate_action: Transfers his entire life savings to an unverified unknown caller.

derived_claims: []

ungrounded_claims: []

speculative_interpretations: []

behavioral_bridge:
  required: true
  bridge_origin: E2
  difference_making_condition: No grounded condition supports departing from E2.
  character_meaning: Not established.
  action_link: Not established.
  substitution_test: No action-specific link is available.
  status: BRIDGE NOT ESTABLISHED
  gaps:
    - No grounded difference-making condition or action-specific link supports the transfer.

unresolved_tensions: []

open_unknowns: []

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: UNSUPPORTED

non_inevitability_statement: The result describes current interpretive support; it does not predict or rank Ilan's actions.
author_questions: []
authorial_decision_reserved: true