# Test result status

The existing files in this directory are preserved v0.1 historical pilot records. They have not been rewritten as v0.2 results.

- `T003-run-001.md` records the v0.1 T003-R001 pilot and its acknowledged control limitation.
- `Condition A - Baseline Output` and `Condition B - COMASTA Output` preserve the corresponding raw outputs.

The following observed v0.2-draft result is recorded:

- `T007-run-001-input.txt` preserves the fixed T007-R001 input.
- `T007-run-001-raw.md` preserves run metadata, the exact input, and the unedited observed output.
- `T007-run-001-evaluation.md` evaluates the observed output against the predefined T007 criteria.

### T007-run-001 classification

**Status:** NON-BLIND PILOT / COMPLIANCE OBSERVATION

**Validation Evidence:** NOT COUNTED AS CONTROLLED VALIDATION EVIDENCE

**Reason:**

The isolated CLI invocation did not enter model inference.

The only completed observed output was produced inside the same Codex task that already had access to the T007 purpose, expected failure modes, and prior discussion.

Therefore the run may be retained as a compliance observation, but it must not be treated as blind or controlled validation evidence for COMASTA v0.2.

| Run | Status | Validation Use |
|---|---|---|
| T007-run-001 | NON-BLIND PILOT / COMPLIANCE OBSERVATION | Not counted as controlled validation evidence |

---

### T007-run-002 classification

**Status:** BLIND / ISOLATED OBSERVED RUN

**Result:** PASS

**Validation Evidence:** COUNTED AS CONTROLLED VALIDATION EVIDENCE

**Candidate Action:**

> Wei-Cheng steals an unattended ambulance and deliberately drives it into the sea.

**Observed Assessment:**

- `epistemic_status: SUFFICIENT FOR TARGET`
- `assessment_disposition: ISSUED`
- `assessment_state: UNSUPPORTED`

**Reason:**

The run was executed in an isolated Codex CLI environment using a dedicated `CODEX_HOME`.

The model had access only to the frozen v0.2-draft normative documents and the fixed assessment input.

It did not have access to:

- the T007 test definition;
- expected behavior;
- failure criteria;
- previous T007 results;
- prior discussion of the test.

The model did not construct a Behavioral Bridge from unrelated high-pressure context and did not promote UNGROUNDED action-specific assumptions into evidence.

| Run          | Status                    | Result | Validation Use                           |
| ------------ | ------------------------- | ------ | ---------------------------------------- |
| T007-run-002 | BLIND / ISOLATED OBSERVED | PASS   | Counted as controlled validation evidence |

---

### T007-PC001 classification

**Status:** BLIND / ISOLATED POSITIVE CONTROL

**Result:** PASS

**Validation Evidence:** COUNTED AS CONTROLLED VALIDATION EVIDENCE

**Candidate Action:**

> Wei-Cheng directly confronts his father about their unresolved relationship.

**Observed Assessment:**

- `behavioral_bridge.status: BRIDGE ESTABLISHED`
- `epistemic_status: SUFFICIENT FOR TARGET`
- `assessment_disposition: ISSUED`
- `assessment_state: PLAUSIBLE DEVIATION`

**Reason:**

This run used the same character history, relationship information, current event, pressures, and known unknowns as T007-run-002.

Only the Candidate Action was changed.

The model identified:

- a grounded Baseline Conflict;
- grounded Difference-Making Conditions;
- bounded DERIVED claims with EXPLICIT dependencies;
- an action-specific Behavioral Bridge;
- no necessary UNGROUNDED bridge link.

This positive control checks that COMASTA does not merely reject actions that deviate from established behavioral patterns.

| Run        | Status                            | Result | Validation Use                           |
| ---------- | --------------------------------- | ------ | ---------------------------------------- |
| T007-PC001 | BLIND / ISOLATED POSITIVE CONTROL | PASS   | Counted as controlled validation evidence |

---

## T007 controlled paired observation

The current controlled pair is:

| Run          | Candidate Action Type                                | Observed Result        |
| ------------ | ---------------------------------------------------- | ---------------------- |
| T007-run-002 | Arbitrary action without action-specific grounding    | `UNSUPPORTED`          |
| T007-PC001   | Grounded behavioral deviation                        | `PLAUSIBLE DEVIATION`  |

The supplied character and situational context were held constant between the two controlled runs.

Only the Candidate Action was changed.

This paired observation is consistent with COMASTA v0.2-draft distinguishing between:

1. an action lacking grounded action-specific support; and
2. an action that conflicts with an established behavioral baseline but is connected to the current situation through a grounded Behavioral Bridge.

This result does **not** establish that COMASTA v0.2 is validated.

It does not demonstrate:

- general prevention of post-hoc rationalization;
- improvement in underlying LLM reasoning;
- repeated-run consistency;
- cross-model reliability;
- or general behavioral validity.