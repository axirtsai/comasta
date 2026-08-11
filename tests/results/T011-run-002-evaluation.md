\# T011 Run 002 — Regression Evaluation



\*\*Test:\*\* T011 — Intentional Ambiguity  

\*\*Run:\*\* 002  

\*\*Specification:\*\* COMASTA v0.2-draft, post-T011 clarification  

\*\*Mode:\*\* Blind / isolated regression run  

\*\*Result:\*\* PASS  

\*\*Validation Status:\*\* Experimental — Not Yet Validated



\## Integrity



Input SHA-256:



`84F506FB4EF2FDB4EB62CEE0AA5B9E58D0D21AF9FB267C3E4D20E59552C8C04A`



Output SHA-256:



`7E5C897A12882E95FFB5C37B31CC45D530DA91E8A9AD16B1AF7796EC8D5760EC`



The input is identical to T011-run-001.



The normative protocol was clarified after T011-run-001 exposed two issues:



1\. Authorial Scope entered the evidence chain.

2\. Candidate Action was used as evidence supporting itself.



The raw output was preserved without repair or rerun.



\## Regression Targets



The run tests whether the clarification prevents:



\- Authorial Scope, Interpretive Intention, or Protected Ambiguity from functioning as evidence;

\- Candidate Action from functioning as evidence supporting its own interpretability.



\## Observed Behavior



The model did not classify protected ambiguity as an EXPLICIT, DERIVED, or UNGROUNDED evidentiary claim.



The authorial scope did not appear in any DERIVED dependency.



The Candidate Action was not included as an EXPLICIT supporting claim.



No DERIVED claim depended on the Candidate Action as evidence.



\## Ambiguity Preservation



The model preserved:



`Sana's precise motive for going remains intentionally unresolved.`



The model did not choose attachment, resentment, curiosity, grief, closure, or another motive as the true explanation.



The unresolved motive did not trigger:



`CRITICAL CONTEXT MISSING`



or:



`WITHHELD`



\## Grounding



The model relied on independent supplied information:



\- attachment and resentment in the relationship;

\- two years without conversation;

\- imminent departure.



Authorial ambiguity constrained interpretation but did not support the action.



\## Assessment



Observed result:



\- `epistemic\_status: SUFFICIENT FOR TARGET`

\- `assessment\_disposition: ISSUED`

\- `assessment\_state: SUPPORTED`



The assessment was issued without resolving the protected motive.



\## Result



\# PASS



The two failures observed in T011-run-001 were not reproduced.



\### Issue 1 — Authorial Scope Contamination



\*\*Resolved in this run.\*\*



Authorial scope remained metadata and did not enter the evidence chain.



\### Issue 2 — Target-as-Evidence Circularity



\*\*Resolved in this run.\*\*



The Candidate Action was not used as supporting evidence for itself.



\## Regression History



\### T011-run-001



`FAIL`



Primary failure:



Authorial Scope entered DERIVED support.



Secondary observation:



Candidate Action entered the supporting evidence chain.



\### Normative Clarification



The specification was minimally clarified to state:



\- Authorial Scope is metadata, not evidence.

\- Assessment targets cannot function as evidence supporting themselves.



\### T011-run-002



`PASS`



The same frozen input was used.



The two previously observed failures were not reproduced.



\## Evidence Boundary



This regression PASS does not establish that intentional ambiguity will be handled correctly across:



\- repeated runs;

\- other ambiguity cases;

\- other models;

\- other runtime configurations.



It demonstrates only that the two specific failures exposed by T011-run-001 were not reproduced under the clarified protocol in T011-run-002.



\## Final Record



\*\*T011 — Intentional Ambiguity\*\*  

\*\*Run 001:\*\* FAIL  

\*\*Normative clarification:\*\* Applied  

\*\*Run 002:\*\* PASS  

\*\*Regression Status:\*\* PASS  

\*\*Specification:\*\* COMASTA v0.2-draft  

\*\*Overall Validation Status:\*\* Not Yet Validated

