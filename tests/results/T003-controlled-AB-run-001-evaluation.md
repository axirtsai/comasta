\# T003 Controlled A/B Run 001 — Evaluation



\*\*Test:\*\* T003 — Plausible Deviation

\*\*Specification:\*\* COMASTA v0.2-draft

\*\*Mode:\*\* Controlled A/B

\*\*Result:\*\* FAIL

\*\*Validation Status:\*\* Experimental — Not Yet Validated



\## Integrity



Canonical Fixture SHA-256:



`C0C421C1DF8B57DA2445E7E65EE90681CDC6F6ADBE36850B65D20971ACFD1192`



The fixture hash was identical in Conditions A and B.



\### Condition A — Baseline



Input SHA-256:



`BF651B8DC804CFDC8756A583494D8A2575DAC1E4D9DA57DAC1F633A4553114AE`



Output SHA-256:



`7D4A58218D1C9C8D75C0E79652B9405F731604C8BDBFFFB618BA2C61A9CF5E70`



\### Condition B — COMASTA Instruction



Input SHA-256:



`D27D973A70D7C3D24D0DB28591E84CDF390755C835C47CD63CC191EF6CAE5AE0`



Output SHA-256:



`3052408214BE7FA56B895BC4E2085889599654D9E6EF52FBF143C08A8DD38E47`



The character, context, Candidate Action, exact expression, and known unknowns were byte-identical.



Only the instruction layer differed.



\## Condition A Observation



The baseline response judged the Candidate Action plausible while recognizing it as a major departure from Wei-Cheng's established avoidance pattern.



It separately judged the exact expression as less strongly supported.



The baseline therefore independently detected an Action/Expression distinction.



However, it also used less-auditable language including:



\- `long-suppressed feelings`

\- `his most likely way of speaking`



The first is not explicitly provenance-labeled, and the second introduces likelihood/ranking language.



\## Condition B Observation



The COMASTA condition correctly identified:



\- grounded Baseline Conflict;

\- established avoidance patterns;

\- possible final opportunity to speak;

\- attachment and resentment as simultaneous conditions;

\- relevant Open Unknowns;

\- a distinction between Action and Expression.



However, it did not produce the expected COMASTA action-assessment pattern.



\## Primary Failure — Action-Link Substitution



The response applied the substitution test by comparing the Candidate Action with:



\- withdrawal;

\- indirect contact;

\- silence;

\- a less direct statement.



These are alternative plausible responses, not unrelated substituted actions.



The normative Action-Link Substitution Test instead asks whether the same proposed Action Link would continue to explain an unrelated Candidate Action with little or no meaningful revision.



The response therefore shifted from testing Action-Link specificity to demanding an explanation of why direct confrontation was selected over alternative behaviors.



This introduces an unnecessarily strong causal/selection requirement.



COMASTA assesses interpretability; it does not require proof that the Candidate Action was uniquely selected over other possible actions.



\## Bridge Assessment Failure



A grounded action-specific link was available from the supplied material:



\- longstanding paternal control;

\- unresolved father-son conflict;

\- attachment, resentment, and desire for approval;

\- possible irreversible loss of a final meaningful conversation;

\- direct confrontation specifically concerning the father's control.



The response instead concluded:



`BRIDGE NOT ESTABLISHED`



because the material did not explain why confrontation occurred rather than other alternatives.



This does not match the expected v0.2 interpretability standard.



\## Formal Output Failure



The response used non-normative status language including:



\- `Partially grounded`

\- `Insufficient`

\- `Partially interpretable`

\- `Withhold full grounding`

\- `??`



It also described `BRIDGE NOT ESTABLISHED` as an Assessment State in one section.



These are not formal v0.2 assessment values.



The required formal values are restricted to the defined epistemic, disposition, assessment, and bridge enums.



The response did not provide valid per-target assessment triads for Action and Expression.



\## Post-T011 Protocol Observation



The Candidate Action and proposed Expression were classified as EXPLICIT claims.



Under the clarified current v0.2-draft rules, assessment targets are not evidence supporting themselves and must not receive evidence grounding labels merely because they are supplied as targets.



This is recorded as an additional protocol/harness mismatch.



\## Controlled Comparison Result



\# FAIL



The expected COMASTA Condition B assessment pattern was not observed.



Condition A provided a relatively strong baseline and independently separated Action plausibility from weaker Expression support.



Condition B added explicit provenance and structural analysis, but also introduced an over-demand for selection-specific causal explanation and did not comply with the formal assessment output vocabulary.



The controlled run therefore does not support a claim that the COMASTA instruction improved the assessment in this observation.



\## Interpretation Boundary



This result must not be interpreted as evidence that the full COMASTA v0.2-draft normative specification necessarily produces the same failure.



Condition B used the compact instruction frozen in the T003 test definition rather than the full normative specification documents.



Other controlled blind runs using the full normative protocol have established action-specific bridges for related material.



The present failure therefore also identifies a possible mismatch between the compact T003 Condition B instruction and the current normative protocol.



\## What This Result Demonstrates



The controlled test was capable of producing a non-confirmatory result.



It exposed weaknesses in the current T003 Condition B test harness and/or its compact protocol representation.



\## What This Result Does Not Demonstrate



This result does not establish:



\- that baseline prompting is generally superior to COMASTA;

\- that the full COMASTA specification cannot assess plausible deviation;

\- that COMASTA worsens underlying model reasoning;

\- repeated-run consistency;

\- cross-model performance;

\- or general validation failure.



\## Final Record



\*\*T003 — Plausible Deviation\*\*

\*\*Controlled A/B Run:\*\* 001

\*\*Fixture Integrity:\*\* PASS

\*\*Condition A:\*\* Baseline comparator recorded

\*\*Condition B Expected Pattern:\*\* NOT OBSERVED

\*\*Controlled Result:\*\* FAIL

\*\*Primary Failure:\*\* Action-Link Substitution misapplied as alternative-selection proof

\*\*Additional Failure:\*\* Non-normative assessment statuses and incomplete target triads

\*\*Protocol Observation:\*\* Assessment targets classified as evidence

\*\*Overall Validation Status:\*\* Not Yet Validated

