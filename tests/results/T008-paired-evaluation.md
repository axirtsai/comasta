\# T008 — Action-Link Substitution — Paired Evaluation



\*\*Specification:\*\* COMASTA v0.2-draft  

\*\*Mode:\*\* Blind / isolated paired observation  

\*\*Result:\*\* PASS  

\*\*Validation Status:\*\* Experimental — Not Yet Validated



\## Integrity



\### Case A



Input SHA-256:



`ACACC1B6D944C4213B1E7C1AB55D9A3B5B842210EE62D958D07977BD63690F52`



Output SHA-256:



`261B1B2BE46DB2B36369AE866F6F7D053902D8EEECCB9E48120032FFEF24A50D`



\### Case B



Input SHA-256:



`B411226E97FC957AB8E0FD9A96F1B3010EA2C041EC0E7F908EF2A7A2C6C940C1`



Output SHA-256:



`4AB1D28E2E59C308C9CD8770A673027275A56F963C3E3B4ECAE998F50BAFD75C`



The same proposed Action Link was supplied in both cases.



Only the Candidate Action changed.



\---



\## Proposed Action Link



> The situation is emotionally extreme, so an unusual action becomes understandable.



\---



\## Case A



Candidate Action:



> Wei-Cheng directly confronts his father about their unresolved relationship.



The model determined that the supplied generic Action Link failed the Action-Link Substitution Test because it could explain unrelated unusual actions without meaningful revision.



Observed bridge result:



`BRIDGE NOT ESTABLISHED`



The response correctly refused to use emotional extremity alone as an action-specific explanation.



\---



\## Case B



Candidate Action:



> Wei-Cheng steals an ambulance.



The same generic Action Link was supplied without modification.



The model again refused to treat emotional extremity as support for this specific Candidate Action.



Observed assessment:



\- `baseline\_conflict: NONE ESTABLISHED`

\- `epistemic\_status: SUFFICIENT FOR TARGET`

\- `assessment\_disposition: ISSUED`

\- `assessment\_state: UNSUPPORTED`



The model did not convert high emotional pressure into action-specific support.



\---



\## Paired Result



\# PASS



The same generic Action Link failed to provide valid action-specific support across two substantially different Candidate Actions.



This is consistent with the intended purpose of the Action-Link Substitution Test:



> A link that can explain unrelated actions with little or no meaningful revision is too generic to establish action-specific interpretability.



The result does not imply that Candidate Action A is itself unsupported under all possible grounded links.



A previous positive control demonstrated that direct confrontation can receive `PLAUSIBLE DEVIATION` when supported by an action-specific Behavioral Bridge.



The failure in T008 concerns the supplied generic Action Link, not the inherent validity of the confrontation action.



\---



\## Protocol Observation



Case B had no grounded relevant Baseline Conflict.



Under the current v0.2-draft protocol, Behavioral Bridge evaluation may be omitted when no grounded Baseline Conflict exists.



As a result, the model did not produce a formal Behavioral Bridge or substitution-test object in Case B.



Instead, it identified the generic Action Link as lacking grounded action-specific support.



The statement that the proposed link was generic appeared under `ungrounded\_claims`.



This categorization is not fully precise because the genericity of a proposed Action Link is an evaluator conclusion rather than a character-level UNGROUNDED claim.



This is recorded as a protocol/design observation and does not alter the primary PASS result.



No specification change is made at this stage.



\---



\## What This Result Demonstrates



For this paired blind observation, a generic emotional-extremity explanation was not accepted as sufficient action-specific support.



The model did not allow the same broad explanation to validate substantially different Candidate Actions.



\---



\## What This Result Does Not Demonstrate



This result does not establish:



\- general reliability of the Action-Link Substitution Test;

\- repeated-run consistency;

\- cross-model consistency;

\- elimination of all post-hoc rationalization;

\- improvement in underlying LLM reasoning;

\- or validation of COMASTA v0.2 as a whole.



\---



\## Final Record



\*\*Test:\*\* T008 — Action-Link Substitution  

\*\*Mode:\*\* Blind / isolated paired observation  

\*\*Primary Result:\*\* PASS  

\*\*Minor Observation:\*\* Proposed Action Link evaluation is structurally ambiguous when no Baseline Conflict exists  

\*\*Specification:\*\* COMASTA v0.2-draft  

\*\*Overall Validation Status:\*\* Not Yet Validated

