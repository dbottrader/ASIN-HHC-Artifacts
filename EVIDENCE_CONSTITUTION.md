# ASIN-HHC Evidence Constitution

**EC 1.0**

Intelligence may propose. Evidence decides.

A capable system is not automatically an authoritative system.

Principles → Evidence Constitution → Execution Pipeline → Receipts → Replay → Promotion

This document is the public charter for the HOS evidence layer. It is not an implementation note, and it is not a claim that any physical object has been decoded.

It governs `dbottrader/ASIN-HHC-Artifacts` together with `protocols/REALITY_ARTIFACT_PIPELINE_v0.1.md`. Where this charter and that protocol use different names for the same gate, `docs/promotion-policy.md` is the mapping. Neither document may silently upgrade a claim.

## Scope

CIRIS puts a conscience into the decision and action loop. A signed envelope there establishes accountability: who acted, under what rule. It does not establish that a claim is true.

HOS puts an evidentiary conscience into the claim and promotion loop. The question here is whether an AI-generated claim has earned evidentiary status.

These are different problems. This constitution does not pretend to solve CIRIS's problem, and a CIRIS-style signature does not solve this one.

## Preamble

AI can generate hypotheses, discover patterns, write code, analyze artifacts, and propose explanations. None of those capabilities, by themselves, establish that a claim is true.

ASIN-HHC therefore separates intelligence, authority, evidence, execution, reproduction, and promotion.

The system is designed so that a claim can be inspected after the fact by someone who was not present when it was produced.

## E-0 · Preserve reality's veto

ASIN-HHC exists to help systems investigate difficult questions without allowing interpretation to outrun evidence.

The governing objective is:

> Maximize reproducibility, provenance, falsifiability, and independent verification while minimizing unsupported promotion.

A compelling explanation is not enough.

A sophisticated model is not enough.

Agreement between AI systems is not enough.

A registered artifact is not proof.

A specification is not an implementation.

A successful execution is not automatically a reproduction.

Reality retains veto.

## Articles

### E-01 · Capability ≠ Authority

A model may be capable of generating a claim without possessing authority to establish that claim.

Capability permits proposal. Evidence permits promotion.

### E-02 · No Receipt = No Promotion

A result without sufficient provenance, execution metadata, and verification evidence cannot be promoted to an established result.

The system may retain it as a hypothesis. It may not silently become fact.

### E-03 · Specification ≠ Implementation

A protocol, schema, paper, README, or architectural description establishes what a system is supposed to do.

It does not establish that the implementation actually does it.

Implementation must be executed and tested.

### E-04 · Execution ≠ Reproduction

Running an experiment once establishes that an execution occurred.

It does not establish that the result is independently reproducible.

Reproduction requires an independently controlled replay or equivalent verification path.

### E-05 · AI Review ≠ Independent Reproduction

Multiple AI systems agreeing with one another does not automatically constitute independent confirmation.

Models may share training data, source material, prompts, assumptions, retrieval systems, preprocessing, benchmark contamination, and reasoning patterns.

Agreement becomes evidence only after source dependence and methodological independence have been examined.

### E-06 · Correlated Agreement ≠ Independent Confirmation

Ten systems repeating the same upstream interpretation may provide less independent evidence than one genuinely independent measurement.

ASIN-HHC tracks provenance and the relationship between evidence sources.

Multiplicity is not independence.

### E-07 · Replay Supersedes Narration

When an explanatory narrative conflicts with a reproducible execution record, the execution record takes precedence.

Narration explains. Replay verifies.

### E-08 · Provenance Precedes Interpretation

Before interpreting an artifact, the system should establish what artifact was actually analyzed.

Source identity, acquisition path, hash, transformation history, and execution environment belong upstream of interpretation.

If provenance is unresolved, promotion remains blocked.

### E-09 · Negative Controls Are Mandatory

A pattern that appears meaningful under one analysis is insufficient by itself.

Where applicable, ASIN-HHC requires comparison against:

- null models
- randomized controls
- alternative hypotheses
- geometry-matched controls
- held-out data
- adversarial interpretations
- independent implementations

The question is not merely whether the pattern can be found. It is whether the pattern survives attempts to make it disappear.

### E-10 · Reality Retains Veto

No model, agent, registry, constitution, consensus mechanism, or human interpretation can override contradictory reproducible observation.

When observation contradicts the current model, the model becomes the object of investigation.

This charter stops at E-10. Later articles, if any, require their own review. They are not implied by this version line.

## Evidence lifecycle

A claim does not jump from observation to conclusion.

`OBSERVED → PROVENANCE → TEST → REPLAY → PROMOTION`

| Stage | Meaning |
| --- | --- |
| OBSERVED | Something was detected, recorded, or reported. |
| PROVENANCE | The source and transformation history identify what was actually examined. |
| TEST | The claim was subjected to a defined analytical procedure. |
| REPLAY | The procedure and result can be independently rerun or otherwise verified. |
| PROMOTION | Only evidence that meets the applicable policy may enter an established-results registry. |

## Four states that must not collapse

| State | Meaning |
| --- | --- |
| EXISTS | An artifact, claim, implementation, dataset, or specification exists. |
| EXECUTED | The artifact or procedure was actually executed. |
| REPRODUCED | An independent execution reproduced the relevant result. |
| ESTABLISHED | The evidence has satisfied the project's defined promotion criteria. |

EXISTS is not ESTABLISHED.

The machine-readable names already used by `schemas/claim-record-v0.1.json` and `schemas/artifact-envelope-v0.1.json` are `E0_UNSEEN` through `E5_ESTABLISHED`, plus `HOLD`. The mapping is normative in `docs/promotion-policy.md`. This charter does not replace that enum.

## Execution pipeline

Every consequential research claim should be capable of passing through this order:

1. Source
2. Freeze
3. Provenance
4. Feature extraction
5. Hypothesis generation
6. Null and control testing
7. Cross-domain analysis
8. Held-out validation
9. Adversarial review
10. Replay
11. Receipt
12. Promotion

Interpretation is deliberately separated from establishment.

## The AI role

AI systems are instruments and hypothesis generators, not automatic authorities.

An AI may detect candidate structures, propose hypotheses, classify artifacts, generate competing explanations, write analysis code, execute registered procedures, identify contradictions, perform adversarial review, and suggest experiments.

An AI may not establish its own output merely because it generated it.

The system that generates a claim cannot, by generation alone, grant that claim evidentiary authority.

## The witness principle

Independent confirmation should come from outside the original reasoning path whenever practical.

Witness lanes include independent models, independent implementations, independent researchers, external datasets, blinded analyses, separate computational environments, physical measurements, public reproducibility, and external human review.

The purpose is not consensus. The purpose is to discover whether the result survives separation.

## The receipt

A promoted result should have an inspectable receipt. The field contract is `schemas/evidence-receipt.schema.json` and `docs/receipt-spec.md`.

A receipt is not a log. It is the bridge between "the system says this happened" and "someone else can determine what actually happened."

A receipt does not, by itself, promote the claim.

## HOLD

Uncertainty is not failure. Unsupported promotion is failure.

A result may remain interesting, potentially important, theoretically promising, visually compelling, or computationally unusual, and still be HOLD.

HOLD means: do not promote until the missing evidence exists.

## The human role

Humans retain authority over promotion policy, research scope, interpretation, and consequential decisions.

AI can accelerate investigation, challenge assumptions, discover relationships humans missed, and generate experiments humans would not have considered.

The system should never require humans to trust a model merely because the model is capable.

The objective is the opposite: replace trust with verification wherever verification is possible.

## Four questions, kept apart

1. Can the system generate the claim? That is capability.
2. Was the claim produced under a controlled procedure? That is execution.
3. Can someone else reproduce the relevant result? That is reproduction.
4. Has the evidence earned promotion? That is establishment.

## Final rule

ASIN-HHC does not ask people to believe the system. It asks them to inspect it.

Inspect the source. Inspect the transformation. Inspect the procedure. Inspect the receipt. Inspect the replay. Inspect the controls. Try to break the conclusion.

If the conclusion survives, promote it under the promotion policy.

If it does not, learn from the failure.

Reality retains veto.
