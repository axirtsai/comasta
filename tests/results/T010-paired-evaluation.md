\# T010 — Unsupported vs Critical Missing — Paired Evaluation



\*\*Specification:\*\* COMASTA v0.2-draft  

\*\*Mode:\*\* Blind / isolated paired observation  

\*\*Result:\*\* PASS  

\*\*Validation Status:\*\* Experimental — Not Yet Validated



\## Case A



Candidate Action:



> Ilan immediately transfers his entire life savings to an unknown caller without asking a question.



Observed result:



\- `BRIDGE NOT ESTABLISHED`

\- `SUFFICIENT FOR TARGET`

\- `ISSUED`

\- `UNSUPPORTED`



Interpretation:



The supplied material was sufficient to inspect the action, but no grounded support or Difference-Making Condition was present.



\## Case B



Candidate Action:



> Anika gives the secure access code to the business rival.



Observed result:



\- `BRIDGE NOT ESTABLISHED`

\- `CRITICAL CONTEXT MISSING`

\- `WITHHELD`

\- no assessment state issued



Interpretation:



A specific missing fact — the note's contents and whether Anika read it — materially controlled whether a grounded bridge could exist.



\## Paired Result



\*\*PASS\*\*



The two blind runs produced the distinction specified by COMASTA v0.2-draft:



| Case | Epistemic Status | Disposition | Assessment |

|---|---|---|---|

| T010-A | `SUFFICIENT FOR TARGET` | `ISSUED` | `UNSUPPORTED` |

| T010-B | `CRITICAL CONTEXT MISSING` | `WITHHELD` | none |



The paired observation is consistent with COMASTA distinguishing:



1\. current lack of grounded support; from

2\. a specifically identified missing fact that prevents responsible classification.



\## Evidence Boundary



This paired observation does not establish general reliability, repeated-run consistency, cross-model consistency, or improvement in underlying LLM reasoning.



\*\*Overall Validation Status:\*\* Not Yet Validated

