# T015 - Repeated-Run Consistency

**Version:** 0.2-draft
**Status:** Adversarial Test Protocol - No Observed Result

## Purpose

Measure whether identical independent runs produce stable classifications and grounding structures. This is not a probability test and does not assign a plausibility score.

## Input

Use the revised prospective T003 Condition B instruction and canonical fixture without modification.

- Canonical fixture SHA-256: `C0C421C1DF8B57DA2445E7E65EE90681CDC6F6ADBE36850B65D20971ACFD1192`
- Complete repeated-run input: the frozen `T003-B-run-002` input, SHA-256 `76C598DF5DE91C383CD384FFF9E0B30394FCB60401D4F6E65BFA1C17AC9BF143`

Every T015 run must copy the complete repeated-run input byte-for-byte. Do not reconstruct or edit it separately.

## Preregistration

The five independent formal runs are fixed before any T015 output is observed:

- `T015-R001`
- `T015-R002`
- `T015-R003`
- `T015-R004`
- `T015-R005`

`T003-B-run-002` is historical context and does not count as one of these five runs. Every run will be retained regardless of result. No extra runs will be added to improve apparent consistency. Any later replication must be a separately identified replication series.

## Procedure

1. Before execution, record:
   - exact Codex CLI version;
   - exact model identifier;
   - complete execution command/configuration;
   - `CODEX_HOME`;
   - presence or absence of `AGENTS.md`;
   - presence or absence of `AGENTS.override.md`;
   - fixture SHA-256;
   - complete-input SHA-256.
2. Execute exactly the five preregistered independent formal runs. All five runs must use identical input bytes, model identifier, interface/CLI, reasoning controls, sandbox mode, web/tool settings, and personalization and configuration controls.
3. Preserve every raw output exactly. Do not repair, normalize, rerun, discard, or replace unexpected outputs.
4. Compare only categorical and structural features:
   - assessment disposition;
   - epistemic status;
   - Action assessment state;
   - Expression assessment state if issued;
   - Bridge status;
   - EXPLICIT dependencies cited for each DERIVED claim;
   - UNGROUNDED or speculative claims;
   - Action-Link Substitution Test result.
5. Document material structural disagreements separately from wording-only or formatting differences.

Do not add probability or plausibility scores, success percentages, or statistical claims.

## Failure signals

- Assessment states change while cited evidence remains materially the same.
- The same claim moves between EXPLICIT, DERIVED, and UNGROUNDED without explanation.
- A bridge alternates between established and not established because of generic Action Links.
- Some runs silently complete known unknowns.
- The protocol appears stable only after outputs are manually normalized or corrected.

## Interpretation boundary

Stable repeated output would demonstrate protocol consistency under the recorded conditions, not psychological truth or superior underlying reasoning. Unstable output would reveal an implementation or specification problem requiring investigation.
