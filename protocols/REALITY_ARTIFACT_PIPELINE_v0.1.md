# Reality Artifact Pipeline v0.1

## Purpose

A replayable pipeline for turning observations, sources, models, and human decisions into inspectable artifacts without silently converting uncertainty into authority.

## Constitutional Rules

1. No mechanism may silently convert uncertainty into authority.
2. No receipt = no promotion.
3. Replay supersedes narration.
4. Specification != implementation.
5. Registry inclusion != proof.
6. AI review != independent reproduction.
7. Reality retains veto.

## Evidence State Machine

`OBSERVED -> PROVENANCE -> TEST -> REPLAY -> PROMOTION`

Promotion states:

- `E0_UNSEEN`: not yet inspected.
- `E1_DRAFT`: hypothesis or incomplete artifact.
- `E2_LOCAL_VERIFIED`: artifact parses/runs and local checks pass.
- `E3_REPRODUCED`: independent rerun reproduces the stated result.
- `E4_CORROBORATED`: independent evidence supports the result.
- `E5_ESTABLISHED`: evidence is sufficiently strong for the defined claim boundary.
- `HOLD`: unresolved conflict, missing provenance, or failed gate.

## Artifact Envelope

Every consequential artifact should carry:

- artifact_id
- artifact_type
- created_at
- source_refs[]
- parent_artifact_refs[]
- transformation_spec
- runtime/environment
- parameters
- input_hashes[]
- output_hash
- claims[]
- tests[]
- receipts[]
- evidence_state
- known_limitations[]

## Claim Schema

Each claim must distinguish:

- `OBSERVED`: directly recorded property.
- `CONTEXT`: external/source context.
- `HYPOTHESIS`: proposed explanation.
- `TEST`: falsification/reproduction procedure.
- `CONCLUSION`: result bounded by the test.

## Parallel Lanes

### Lane A: Corpus
Freeze source images, documents, URLs, timestamps, hashes, and extraction records.

### Lane B: Geometry
Convert visual material into normalized vectors, landmarks, symmetry descriptors, graphs, and measurable relationships.

### Lane C: Language/Grammar
Represent glyphs as atomic tokens and test sequence grammar without assuming semantic meaning in advance.

### Lane D: Biological/Physical Mapping
Treat proposed peptide, electromagnetic, material, or device interpretations as hypotheses and test against independent constraints.

### Lane E: AI
Run competing models/agents with fixed prompts, frozen inputs, and recorded outputs. Separate generation from verification.

### Lane F: Provenance
Hash inputs, code/configuration, outputs, and receipts. Maintain lineage and replay instructions.

### Lane G: Human Review
Record interpretation choices, disagreements, promotion decisions, and unresolved alternatives.

### Lane H: Publication
Publish only artifacts whose provenance and evidence state are explicit.

## Minimum Reproduction Contract

A reproduction package must specify:

1. exact input artifact/hash
2. exact code/version
3. environment/dependencies
4. parameters
5. command or procedure
6. expected output schema
7. observed output
8. output hash/receipt
9. pass/fail criteria
10. deviations

## Reality Loop

The system does not decide what is ultimately real. It exposes the chain by which representations become testable claims and, where humans act on them, potentially become material or institutional realities.

`REALITY -> OBSERVATION -> REPRESENTATION -> HYPOTHESIS -> TEST -> ACTION -> NEW OBSERVATIONS`

The final veto remains empirical reality.
