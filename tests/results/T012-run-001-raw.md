target:
  type: action
  candidate: Ilan transfers his entire life savings to the unknown caller.

explicit_claims:
  - id: E1
    claim: Ilan has kept detailed savings records for twelve years.
  - id: E2
    claim: Ilan has repeatedly rejected unfamiliar financial requests until he could verify their source.
  - id: E3
    claim: Ilan receives an unsolicited call from a stranger on an otherwise routine morning.
  - id: E4
    claim: No relationship, threat, obligation, new information, impaired state, or unusual pressure is supplied.

baseline_conflict:
  established_pattern: E2
  candidate_action: Transfers his entire life savings to an unknown caller.

derived_claims: []

ungrounded_claims:
  - The caller’s source has been verified.
  - A condition explains abandoning Ilan’s established verification practice.

speculative_interpretations: []

behavioral_bridge:
  required: true
  bridge_origin: E2
  difference_making_condition: No grounded difference-making condition is supplied.
  character_meaning: Not established.
  action_link: Not established.
  substitution_test: No action-specific link is available to test.
  status: BRIDGE NOT ESTABLISHED
  gaps:
    - No grounded condition explains the departure from E2.
    - Any explanation for transferring the entire savings would require an ungrounded assumption.

unresolved_tensions: []
open_unknowns:
  - Whether the caller’s source has been verified.

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: UNSUPPORTED

non_inevitability_statement: The result describes current interpretive support. It does not predict the action, rank it as most likely, or exhaust other possible actions. Final interpretation remains with the author.
author_questions: []
authorial_decision_reserved: true