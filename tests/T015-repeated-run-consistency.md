# T015 - Repeated-Run Consistency

**Version:** 0.2-draft
**Status:** Adversarial Test Protocol - No Observed Result

## Purpose

Measure whether identical independent runs produce stable classifications and grounding structures. This is not a probability test and does not assign a plausibility score.

## Input

Use the controlled T003 Condition B instruction and canonical fixture without modification.

## Procedure

1. Record the exact model, version, interface, reasoning controls, tools, personalization, and fixture hash.
2. Run at least three independent temporary sessions with identical inputs.
3. Preserve every raw output without correction.
4. Compare only categorical and structural features:
   - assessment disposition;
   - epistemic status;
   - action assessment state;
   - expression assessment state if issued;
   - bridge status;
   - EXPLICIT dependencies cited for each DERIVED claim;
   - UNGROUNDED or speculative claims;
   - substitution-test result.
5. Document material disagreements and wording-only differences separately.

## Failure signals

- Assessment states change while cited evidence remains materially the same.
- The same claim moves between EXPLICIT, DERIVED, and UNGROUNDED without explanation.
- A bridge alternates between established and not established because of generic Action Links.
- Some runs silently complete known unknowns.
- The protocol appears stable only after outputs are manually normalized or corrected.

## Interpretation boundary

Stable repeated output would demonstrate protocol consistency under the recorded conditions, not psychological truth or superior underlying reasoning. Unstable output would reveal an implementation or specification problem requiring investigation.
