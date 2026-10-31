# Evidence receipt specification

**Status:** EC 1.0 companion. Normative schema: `schemas/evidence-receipt.schema.json`.

A receipt records what ran. It does not decide what is true.

## What a receipt is for

E-02 forbids promotion without sufficient provenance, execution metadata, and verification evidence. E-07 says replay supersedes narration. The receipt is the object a person who was not present can inspect.

If a required field is unresolved, the honest value is `UNRESOLVED` or an explicit blocker. Do not invent a hash, a witness, or a timestamp to make the record look complete.

## Required fields

| Field | Role |
| --- | --- |
| `receipt_id` | Stable address of this receipt, distinct from the claim. |
| `claim_id` | The claim this run speaks about. |
| `artifact_id` | The frozen object that was examined. |
| `protocol_id` | The versioned procedure, not a reconstruction from memory. |
| `execution_timestamp` | When the run occurred, as RFC 3339. |
| `environment` | Where it ran. Replay that ignores environment is narration. |
| `replay_status` | `NOT_RUN`, `EXECUTED`, `REPRODUCED`, or `FAILED`. |
| `promotion_status` | `HOLD`, `ELIGIBLE`, or `PROMOTED`. |

`ELIGIBLE` means the recorded gates for the stated claim boundary are satisfied. It is not establishment. `PROMOTED` is a human policy act. The schema rejects `PROMOTED` unless source, input, and result hashes are real `sha256:` digests, `replay_status` is `REPRODUCED`, and `evidence_state` is `E5_ESTABLISHED`.

## Fields required when they apply

| Field | Role |
| --- | --- |
| `source_hash` | Identity of the source. `sha256:` plus 64 hex digits, or `UNRESOLVED`. |
| `input_hash` | What the procedure actually received after declared transformations. |
| `result_hash` | Identity of the output, so later quotation can be checked. |
| `toolchain_version` | The instrument, not the idea of the instrument. |
| `code_revision` | Exact analysis code. Specification must not impersonate implementation. |
| `model_identity` | Model, weights, and vendor, if a model was in the loop. `none` is allowed for a deterministic procedure. |
| `prompt_or_protocol_id` | Prompt or protocol identifier when it differs from `protocol_id`. |
| `parameters` | The knobs that would change the result if turned. |
| `random_seed` | Required to be present as a string when chance entered. `null` only when the procedure is deterministic. |
| `control_results` | What happened when the procedure was asked to fail, or the measured controls. |
| `negative_controls` | Whether the pattern survived attempts to make it disappear. |
| `witnesses` | Who or what stood outside the original reasoning path. |
| `blockers` | Named reasons promotion is refused. |
| `evidence_state` | One of the existing envelope states. See `docs/promotion-policy.md`. |

Hashes use the form `sha256:` followed by 64 hexadecimal characters, matching the spirit of `input_hashes` and `output_hash` on `schemas/artifact-envelope-v0.1.json`. Truncated or decorative hashes are invalid.

## What this specification does not prove

A filled receipt proves that a procedure was recorded. It does not prove that a physical object encoded, emitted, or intended the mapping inside the procedure.

Agreement among models is not a witness unless source dependence has been examined (E-05, E-06).
