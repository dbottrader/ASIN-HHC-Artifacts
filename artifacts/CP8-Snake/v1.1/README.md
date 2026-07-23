# CP8 Snake // Hypercube Lab v1.1

A dependency-free, mobile-first single-file application that joins the original CP8 Snake game to a working **Snake-in-a-Box induced-path laboratory**.

## What is live

- Classic Snake with keyboard, swipe, and touch-pad controls.
- Hypercube dimensions 3–10.
- Manual one-bit state transitions.
- Immediate rejection of revisits, non-adjacent moves, and induced-path chords.
- Background Web Worker search.
- CP8 φ-guided candidate ordering.
- Golden-angle hypercube projection.
- Transparent 428 / 528 / 963 path metrics.
- ANU-28 semantic routing display.
- Independent local verifier.
- Canonical JSON receipt export/import.
- SHA-256 content sealing with a pure-JavaScript offline fallback.

No server, dependency install, account, or network connection is required.

## Structural mathematics

For a path `P = (v_0, …, v_k)` in the `n`-dimensional hypercube graph `Q_n`:

1. `d_H(v_i, v_{i+1}) = 1` for every consecutive pair.
2. `d_H(v_i, v_j) >= 2` whenever `|i-j| > 1`.
3. Every vertex is unique.

The verifier enforces these rules directly. This is the operative Snake-in-a-Box proof condition.

## CP8 Math Core

The interface adds a transparent auxiliary metric:

```text
S_CP8 = 100 × (428·C + 528·F + 963·I) / 1919
```

Where:

- `C` — **428 Core**: `1` when the induced-path verifier passes, otherwise `0`.
- `F` — **528 Fusion**: Shannon entropy of the flipped-bit distribution, normalized by `log2(n)`.
- `I` — **963 Integration**: path coverage `|P| / 2^n`.

This score does **not** prove optimality. It measures structural validity, distribution across dimensions, and state-space coverage in one explicit expression.

## φ-guided search

The worker first applies onward-degree ordering, then uses the CP8 golden-angle parameter `137.507764°` as a deterministic tie break. The projection basis uses the same angular increment.

The search remains heuristic and time-limited. A valid result proves that the exported path is induced; it does not prove that no longer path exists.

## ANU-28

The full 28-glyph protocol is used as a semantic routing layer indexed by path depth. The glyph state is included in exported receipts. Glyphs and frequency labels are metadata only; they do not assert physical, neurological, or cryptographic effects.

## A → S → I → N runtime

- **A — Anchor:** all-zero origin state.
- **S — Search:** atomic one-bit transitions.
- **I — Integrity:** induced-path verification.
- **N — Network:** canonical receipt and SHA-256 seal.

## Run on Android

1. Download `CP8_SNAKE_HYPERCUBE_LAB_v1_1.html`.
2. Open the Android **Files** app.
3. Tap the HTML file and choose Chrome or another modern browser.
4. Use **Add to Home screen** for app-like access.

## Proof boundary

```text
evidence_status: LOCAL_BROWSER_VERIFIED
authority_status: HOLD
attestation: MACHINE_EXECUTION_UNATTESTED
optimality_claim: false
independent_reproduction: false
```

Structural verification and SHA-256 are the operative proof mechanisms. CP8 scoring, glyph routing, and harmonic labels remain auxiliary metadata.

## Canonical lineage

The v1.1 math layer is based on existing repository concepts:

- `engines/asin-handshake-engine/docs/ENGINE_SPEC.md` — deterministic golden-angle geometry.
- `docs/HARMONIC_ALGEBRA_SPEC.md` — 428 / 528 / 963 namespace concepts and cryptographic boundary.
- `docs/ANU28_PROTOCOL_SCHEMA_V1.md` — 28-glyph semantic coordination grammar.

## Verification completed

- JavaScript syntax: PASS.
- Headless browser boot: PASS.
- ANU-28 rendered glyph count: 28.
- Deterministic quick demo: PASS.
- Structural verifier after demo: PASS.
- SHA-256 proof seal: PASS.
- 3-second 5D φ-guided worker search: PASS.
- Mobile width overflow check: PASS (`body.scrollWidth = viewport width`).
