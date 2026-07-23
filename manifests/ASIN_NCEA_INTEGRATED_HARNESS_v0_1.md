# ASIN-NCEA Integrated Harness v0.1 — Artifact Registry Card

```text
artifact: ASIN-NCEA_INTEGRATED_HARNESS_v0.1
source_bundle: ASIN_NCEA_TEXT_SNAPSHOTS_20260706.zip
integrated_bundle_sha256: 14e3eaaf71461e35d31f185ed3c84083c516539a057e66c1bb3f5485da7c9807
status: PASS_WITH_HOLD
evidence_level: E3_LOCAL_INTEGRATION
promotion_verdict: HOLD
witness_class: MACHINE_EXECUTION_UNATTESTED
```

## Purpose

This registry card records the public artifact status of the ASIN-NCEA integrated harness v0.1. The harness converts the preserved ASIN-NCEA text snapshot lineage into a clean local integration test around standard cryptographic primitives and evidence-boundary receipts.

## Local run anchors

```text
source_entries: 13
source_hashes_ok: true
source_syntax_ok: true
raw_v2_runtime_ready: false
integrated_core_pass: true
deterministic_core_hash: ee93c43c62eccb6dd9eaf14787bdfe6af2965f66763216221f504af282447274
ledger_merkle_root: ffc27df9d1d33a454e858284b19694c5c7513a9833e25113550f0acd8ec68405
```

## Artifact boundary

This is an artifact card, not a production security certification. The ASIN-NCEA snapshots are preserved as lineage evidence. The integrated harness demonstrates a local architecture run, not external reproduction, production cryptography, live token issuance, or monetary authority.

## Placement

Core implementation PR lives in:

```text
dbottrader/Holbrook-CP8-HHC
branch: agent/asin-ncea-integrated-harness-v0-1
```

This repo keeps the public artifact registry pointer only.