# Promotion policy

**Status:** EC 1.0 companion. Governs how a claim may move toward `E5_ESTABLISHED`. Does not itself promote any claim.

## Authority

Humans retain authority over promotion. An agent, model, registry, or this document cannot override a contradictory reproducible observation (E-10).

This policy is itself subject to review. Landing it on `reality-artifact-pipeline-v0.1` and proposing it by pull request is intentional: the constitution is not exempt from the discipline it establishes.

## State mapping

The charter speaks in four states. The schemas already speak in `E0`–`E5` plus `HOLD`. Both are kept. They map as follows:

| Charter | Machine state | Meaning |
| --- | --- | --- |
| not yet in hand | `E0_UNSEEN` | Not inspected. |
| EXISTS | `E1_DRAFT` | The claim or artifact exists. Not tested. |
| EXECUTED | `E2_LOCAL_VERIFIED` | A defined procedure ran against a named input. |
| REPRODUCED | `E3_REPRODUCED` | An independent execution reproduced the stated result. |
| — | `E4_CORROBORATED` | Independent evidence supports the result beyond a single replay. |
| ESTABLISHED | `E5_ESTABLISHED` | The defined claim boundary has met this policy. |
| HOLD | `HOLD` | A required gate is open. The claim stays available and is not represented as established. |

`E4_CORROBORATED` has no shorter charter synonym. Do not collapse it into REPRODUCED or ESTABLISHED.

Claim `state` remains the existing enum: `OBSERVED`, `CONTEXT`, `HYPOTHESIS`, `TEST`, `CONCLUSION`. A tested computational procedure uses `TEST`. That word does not mean the claim was promoted.

## Gates

Promotion of a claim boundary requires, as applicable:

1. **Provenance.** Source identity, acquisition path, and transformation history are sufficient to know what was examined (E-08). Unresolved provenance blocks promotion.
2. **Test.** A defined procedure was executed. The specification of the procedure is not the execution (E-03, E-04).
3. **Replay.** An independently controlled rerun, or an equivalent verification path, reproduced the relevant result (E-04, E-07).
4. **Independence.** Agreement has been examined for shared upstream sources (E-05, E-06). Multiplicity is not independence.
5. **Controls.** Where a pattern is being claimed, negative controls or an explicit statement that they are inapplicable is on the record (E-09).
6. **Receipt.** `schemas/evidence-receipt.schema.json` is satisfied for that run (E-02).
7. **Boundary.** The promoted sentence is no wider than the test. A computational mapping does not promote a physical-causality sentence.
8. **Human act.** A person records the promotion decision. `promotion_status: PROMOTED` without that act is a defect.

If any required gate fails, the state is `HOLD`.

## What may not be used as a promotion token

- Model confidence, fluency, or agreement among correlated models.
- Presence in this repository.
- A diagram, a Figma board, a video, or a public essay.
- A person's reputation.
- A single reading with no baseline and no procedure.
- A successful local execution offered as if it were reproduction.

## CP8-PEPTIDE-24

The worked example `examples/claims/cp8-peptide-24.claim.json` is `state: TEST` and `evidence_state: HOLD`.

The declared 2-bit mapping and standard genetic code are a computational hypothesis with a defined procedure. They are not, on this record, an established physical encoding.

Promotion stays blocked until all of the following exist as separate evidence, not as prose:

- **Physical source.** A frozen artifact, with a hash, that is the thing actually examined.
- **Blind reconstruction.** The procedure reaches the stated string without being shown the target.
- **Independent witness.** A second implementation or observer outside the original reasoning path.
- **Cross-artifact validation.** A procedure that could fail, connecting physical marks to the code. Until that procedure exists and survives, the domains stay separate.

No field in that example may be edited to `E5_ESTABLISHED` in order to make a narrative easier.
