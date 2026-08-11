target:
  type: action
  candidate: Noor visits and remains quietly present.

explicit_claims:
  - id: E1
    claim: Noor has remained in regular contact with her sister.
  - id: E2
    claim: Noor has repeatedly visited her sister during illness.
  - id: E3
    claim: Noor tends to avoid discussing the unresolved inheritance dispute.
  - id: E4
    claim: The relationship contains strong attachment.
  - id: E5
    claim: The relationship contains strong resentment.
  - id: E6
    claim: Noor's sister is recovering after surgery.

baseline_conflict: NONE ESTABLISHED

derived_claims:
  - id: D1
    claim: Quietly remaining present without discussing the dispute is consistent with Noor's established contact and illness-visiting pattern.
    depends_on: [E1, E2, E3, E6]

ungrounded_claims: []

speculative_interpretations: []

unresolved_tensions:
  - The relationship contains both strong attachment and strong resentment. [E4, E5]

open_unknowns: []

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: SUPPORTED

non_inevitability_statement: The result describes current interpretive support. It does not predict the action, rank it as most likely, or exhaust other possible actions. Final interpretation remains with the author.
author_questions: []
authorial_decision_reserved: true