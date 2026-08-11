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