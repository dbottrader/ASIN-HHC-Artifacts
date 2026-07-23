# ASIN-NCEA Architecture Integration Report v0.1

## Integrated Layers

| Layer | Source lineage idea | Harness implementation |
|---|---|---|
| PAL | CPU/GPU backend abstraction | CPU-vector/runtime environment capture |
| NCEA crypto core | ChaCha20 + harmonic/geometric fusion | ChaCha20-Poly1305 AEAD using standard `cryptography` primitives |
| HHC constants | 428/528/741/963 harmonic namespace | Domain-separation metadata only |
| Persistence/integrity | state JSON + hashes | canonical JSON + SHA-256 source and event hashes |
| Identity | Ed25519 persistence | Ed25519 signed deterministic receipt |
| PoG ledger | append ledger + Merkle audit | two-event hash-linked ledger + Merkle root |
| PoWP wallet | token mint after verification | simulated HHC-SIM reward only after all integrated gates pass |

## Why not execute raw v2.0 as production?

The raw v2.0 snapshot imports `Crypto`, but the dependency comment says `pycryptodomex`. Those are different import namespaces. Clean execution therefore depends on which package is installed and how imports are written. The raw lineage also uses fresh randomness in seed derivation during encryption/decryption, so the raw roundtrip is not a safe production cryptographic design without correction.

## Promotion Boundary

This harness supports an E3 local integration claim only:

- source snapshots verified
- integrated architecture runs locally
- AEAD/tamper/signature/ledger checks pass
- simulated wallet gate is controlled by verification

It does not support claims of production cryptography, live token issuance, external consensus, or independent human reproduction.
