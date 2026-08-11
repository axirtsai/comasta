target:
  type: action
  candidate: Eren begs the parent to say that they are proud of him.

explicit_claims:
  - id: E1
    claim: Eren has documented resentment toward the parent.
  - id: E2
    claim: Eren avoids asking the parent for help.
  - id: E3
    claim: Eren has repeatedly said that he expects nothing from the parent.
  - id: E4
    claim: The parent is briefly visiting the city.
  - id: E5
    claim: No desire for the parent’s approval, recognition, affection, dependency, or hidden longing is supplied.

baseline_conflict:
  established_pattern: Eren repeatedly says that he expects nothing from the parent.
  candidate_action: Eren begs the parent for an expression of pride.

derived_claims:
  - id: D1
    claim: The visit makes a direct request to the parent presently possible.
    depends_on: [E4]

ungrounded_claims:
  - Eren wants the parent’s approval or recognition.
  - The visit changes Eren’s expectation of the parent.
  - The visit specifically makes begging for pride interpretable.

speculative_interpretations: []

behavioral_bridge:
  required: true
  bridge_origin: E3
  difference_making_condition: D1
  character_meaning: No grounded claim explains why the visit matters to Eren in a way that departs from E3.
  action_link: No grounded link explains begging for this specific affirmation.
  substitution_test: No action-specific grounded link is available to test.
  status: BRIDGE NOT ESTABLISHED
  gaps:
    - A necessary explanation of why Eren seeks the parent’s pride is ungrounded.

unresolved_tensions: []
open_unknowns: []

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: UNSUPPORTED

non_inevitability_statement: This result describes current interpretive support; it does not predict the action, rank it as most likely, or exhaust other possible actions.
author_questions: []
authorial_decision_reserved: true