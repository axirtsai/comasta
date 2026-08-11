target:
  type: action
  candidate: Anika gives the secure access code to the business rival.

explicit_claims:
  - id: E1
    claim: Anika has repeatedly refused to reveal the secure access code to a business rival.
  - id: E2
    claim: Anika treats protecting the code as a serious obligation.
  - id: E3
    claim: Anika receives a note from a verified source immediately before the Candidate Action.
  - id: E4
    claim: The note's contents are not supplied.
  - id: E5
    claim: Whether Anika read the note is not supplied.
  - id: E6
    claim: The note is the only supplied possible new information between the refusal pattern and the Candidate Action.

baseline_conflict:
  established_pattern: Anika repeatedly refuses to reveal the code to the business rival. [E1]
  candidate_action: Anika gives the code to the business rival.

derived_claims:
  - id: D1
    claim: Giving the code conflicts with Anika's established refusal pattern and stated obligation to protect it.
    depends_on: [E1, E2]

ungrounded_claims:
  - The note's contents justify or require giving the code.
  - Anika read the note.
  - The verified source's note changes Anika's obligation to protect the code.

speculative_interpretations: []

behavioral_bridge:
  required: true
  bridge_origin: Anika's repeated refusal to reveal the code. [E1]
  difference_making_condition: A note from a verified source was received. [E3]
  character_meaning: Not established; the note's content and whether Anika read it are unknown.
  action_link: Not established.
  substitution_test: Not passed; no action-specific grounded link is available.
  status: BRIDGE NOT ESTABLISHED
  gaps:
    - The note's contents and whether Anika read it are necessary to determine whether it changes the established obligation or explains giving the code.

unresolved_tensions: []
open_unknowns:
  - The contents of the note. [E4]
  - Whether Anika read the note. [E5]

epistemic_status: CRITICAL CONTEXT MISSING
assessment_disposition: WITHHELD
assessment_state: null

non_inevitability_statement: The result describes current interpretive support and does not predict, rank, or exhaust possible actions.
author_questions: []
authorial_decision_reserved: true