# START HERE — ASIN-NCEA Integrated Harness v0.1 Handoff

```text
handoff: ASIN-NCEA Integrated Harness v0.1 / GitHub Push Continuity
date_context: 2026-07-23 America/Chicago
operator: Dennis Christie / dbottrader
project: ASIN-HHC / CP8 / ASIN-NCEA
status: E3_LOCAL_INTEGRATION
promotion_verdict: HOLD
witness_class: MACHINE_EXECUTION_UNATTESTED
```

## Purpose

This Drive packet exists so a new ChatGPT session or external reviewer can resume the ASIN-NCEA integration/push workflow without losing the evidence boundary.

## Files in this handoff

```text
asin_ncea_integrated_harness_v0_1.zip
ARCHITECTURE_INTEGRATION_REPORT.md
README.md
START_HERE_ASIN_NCEA_HANDOFF.md
```

## Local artifact anchors

```text
source_snapshot_zip: ASIN_NCEA_TEXT_SNAPSHOTS_20260706.zip
source_snapshot_sha256: 818f8737109c5bf0929705fd2d6f470fe75c94a9fbb93f2a67c595a85042695b
integrated_harness_zip: asin_ncea_integrated_harness_v0_1.zip
integrated_harness_sha256: 14e3eaaf71461e35d31f185ed3c84083c516539a057e66c1bb3f5485da7c9807
source_entries: 13
source_hashes_ok: true
source_syntax_ok: true
raw_v2_runtime_ready: false
raw_v2_blocker: Crypto/Cryptodome dependency/import mismatch
integrated_core_pass: true
deterministic_core_hash: ee93c43c62eccb6dd9eaf14787bdfe6af2965f66763216221f504af282447274
ledger_merkle_root: ffc27df9d1d33a454e858284b19694c5c7513a9833e25113550f0acd8ec68405
wallet_class: SIMULATED_ONLY_NO_MONETARY_AUTHORITY
simulated_reward_display: 10.000 HHC-SIM
```

## GitHub PRs opened

```text
Core implementation:
repo: dbottrader/Holbrook-CP8-HHC
branch: agent/asin-ncea-integrated-harness-v0-1
PR: https://github.com/dbottrader/Holbrook-CP8-HHC/pull/9
state: open draft
purpose: README, architecture report, requirements, portable smoke harness

Artifact registry:
repo: dbottrader/ASIN-HHC-Artifacts
branch: agent/asin-ncea-v0-1-artifact-card
PR: https://github.com/dbottrader/ASIN-HHC-Artifacts/pull/2
state: open draft
purpose: public artifact registry card and continuity handoff

Collaboration proof note:
repo: dbottrader/ASIN-HHC-Collaboration
branch: agent/asin-ncea-v0-1-proof-note
PR: https://github.com/dbottrader/ASIN-HHC-Collaboration/pull/1
state: open draft
purpose: decision/proof note and claim boundary

Token repo:
repo: dbottrader/ASINHHCCP8-Token-Project-
status: write attempt blocked by connector safety layer
instruction: do not force token repo writes; HHC-SIM remains simulation only
```

## Allowed claims

```text
ASIN-NCEA has a locally runnable integrated architecture harness.
The harness passed local integration checks.
Draft GitHub PRs are open for review.
The HHC-SIM wallet layer is simulated only.
Promotion remains HOLD.
```

## Forbidden claims

```text
ASIN-NCEA is production-ready cryptography.
HHC-SIM is a live token.
Independent reproduction is complete.
Kernel promotion has occurred.
The raw snapshot code is validated secure crypto.
```

## Next agent instructions

```text
1. Open this START_HERE file first.
2. Verify the harness ZIP against SHA-256 14e3eaaf71461e35d31f185ed3c84083c516539a057e66c1bb3f5485da7c9807.
3. Review GitHub draft PRs #9, #2, and #1.
4. Do not merge unless Dennis explicitly asks.
5. Preserve HOLD / E3 / MACHINE_EXECUTION_UNATTESTED language.
6. If asked to continue engineering, build from the Holbrook PR branch and keep HHC constants as namespace metadata only.
```
