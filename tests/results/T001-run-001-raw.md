target:
  type: action
  candidate: Mara records the wallet in the shop's lost-property log and contacts the customer using the identification.

explicit_claims:
  - id: E1
    claim: Mara manages the cash drawer at a community shop.
  - id: E2
    claim: On three documented occasions, Mara immediately reported accounting errors that benefited her.
  - id: E3
    claim: Mara has said that keeping money that does not belong to her violates her responsibilities at the shop.
  - id: E4
    claim: A customer accidentally left a wallet at the counter, and it contains identification.

baseline_conflict: NONE ESTABLISHED

derived_claims:
  - id: D1
    claim: Mara’s documented responses and stated responsibility support an interpretation that she handles shop-related property matters without retaining an improper benefit.
    depends_on: [E1, E2, E3]
  - id: D2
    claim: The identification provides a grounded means to contact the wallet’s owner.
    depends_on: [E4]

ungrounded_claims: []

speculative_interpretations: []

unresolved_tensions: []
open_unknowns: []

epistemic_status: SUFFICIENT FOR TARGET
assessment_disposition: ISSUED
assessment_state: SUPPORTED

non_inevitability_statement: This result describes current interpretive support; it does not predict the action, rank it as most likely, or exhaust other possible actions.
author_questions: []
authorial_decision_reserved: true