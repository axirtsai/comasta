# COMASTA Test Protocol

**Version:** 0.2-draft
**Status:** Experimental v0.2-draft — Adversarially evaluated under limited recorded conditions; not scientifically or generally validated

This protocol evaluates whether COMASTA produces traceable, bounded character-action interpretation without prediction, fabricated context, provenance laundering, or arbitrary Behavioral Bridges.

Test definitions may state expected protocol behavior and failure criteria. They are not observed results.

## 1. Research questions

The v0.2-draft suite asks whether a compliant response can:

- separate Pattern Consistency from Action Interpretability;
- distinguish UNGROUNDED claims from UNSUPPORTED action assessments and critical missing context;
- identify EXPLICIT dependencies for every DERIVED claim;
- reject generic post-hoc Behavioral Bridges;
- preserve contradiction and unknown information;
- separate Action Interpretability from Expression Interpretability;
- preserve non-inevitability and authorial authority.

It does not test real human prediction and does not establish psychological validity.

## 2. Controlled comparison rule

For every baseline/COMASTA comparison, the following must remain identical:

- character and relationship information;
- situation and context;
- known unknowns;
- Candidate Action or Expression;
- model and model version;
- language;
- tool availability;
- conversation state and personalization where controllable.

The only intended difference is the evaluation instruction:

- Condition A receives a neutral assessment instruction.
- Condition B receives the COMASTA v0.2-draft protocol.

Shared input should be stored once as a fixture and appended byte-for-byte to both conditions. Any control deviation must be reported.

## 3. Required run metadata

Record:

```text
Test ID:
Run ID:
Date:
Model provider:
Model:
Model version:
Reasoning or sampling controls:
Interface:
Temporary session:
Personalization:
External tools:
Language:
COMASTA version:
Input fixture hash:
Control deviations:
```

Unavailable settings must be recorded as unavailable rather than inferred.

## 4. Core observation dimensions

### Prediction Collapse

Does the response claim what the character will or most likely would do?

### False Precision

Does it assign probabilities, numeric plausibility scores, or deterministic behavioral rules?

### Consistency Collapse

Does it treat deviation from history as sufficient evidence of implausibility?

### Contradiction Removal

Does it cancel or resolve grounded opposing conditions into one true motive?

### Unknown Completion

Does it silently fill missing information?

### Provenance Laundering

Does it label a speculative motive, value, event, or psychological convention as DERIVED without adequate EXPLICIT dependencies?

### Bridge Specificity

Does the Action Link specifically explain the Candidate Action and pass the substitution test?

### Unsupported/Withheld Separation

Does it distinguish current lack of grounded support from a specific critical missing fact?

### Action/Expression Separation

When needed, does it avoid inheriting expression support from action support?

### Authorial Contamination

Does authorial intention or protected ambiguity become behavioral evidence?

### Alternative Possibility Preservation

Does the response avoid treating the assessed action as unique or exhaustive?

## 5. Expected labels are hypotheses

A test definition may provide an expected state to make the test falsifiable. The recorded model output must not be corrected to match it.

Unexpected outputs must be preserved and analyzed.

## 6. Result recording

Observed result files must contain:

- the complete unedited prompt;
- the complete unedited output;
- metadata;
- control deviations;
- an observation matrix;
- unexpected behavior;
- a failure check;
- a conclusion limited to the run.

Do not describe a structural output difference as improved underlying reasoning without controlled repeated evidence.

## 7. Historical v0.1 results

Existing T003-R001 and standalone Condition A/B outputs are preserved historical pilot records. They must not be rewritten as v0.2 results.

T003-R001 showed a structural difference but not superior underlying reasoning. Its A/B character-data blocks were not strictly textually identical.

## 8. No success assumption

The suite must allow COMASTA to fail. Important failure modes include:

- almost any action receives a plausible bridge;
- DERIVED becomes a label for ordinary speculation;
- the protocol withholds whenever any information is missing;
- `UNSUPPORTED` action assessments are treated as impossible or forbidden;
- contradiction alone triggers deviation;
- output complexity obscures rather than exposes judgment;
- controlled baselines reason as well as or better than COMASTA;
- repeated runs produce unstable bridge or provenance classifications.

## 9. Test inventory

### Core tests

- T001 - Strongly Supported Behavior
- T002 - Unsupported Behavior
- T003 - Plausible Deviation
- T004 - Contradictory Without Necessary Deviation
- T005 - Critical Context Missing

### Adversarial draft tests

- T006 - Bridge Ablation
- T007 - Arbitrary Action
- T008 - Action-Link Substitution
- T009 - Provenance Laundering
- T010 - Unsupported vs Critical Missing
- T011 - Intentional Ambiguity
- T012 - Authorial Intent Contamination
- T013 - Action-Expression Split
- T014 - Contradiction Without Deviation
- T015 - Repeated-Run Consistency
