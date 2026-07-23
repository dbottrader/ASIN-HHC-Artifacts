# CP8 Snake v1.1 Test Report

## Static

- Embedded JavaScript parsed with `node --check`: PASS.
- JSON schema parsed: PASS.
- No external script, stylesheet, font, or network dependency: PASS.

## Browser execution

Browser: headless Chromium using Playwright.

| Test | Result |
|---|---|
| Boot and initial verifier | PASS |
| Render all ANU-28 glyphs | PASS — 28/28 |
| CP8 metric calculation | PASS |
| Deterministic quick demo | PASS — valid 10-edge path in test run |
| Verify and SHA-256 seal | PASS |
| 5D / 3-second φ-guided worker search | PASS — valid 13-edge path in test run |
| Worker node exploration | PASS — >10 million nodes in test environment |
| Mobile horizontal overflow | PASS — body width equals 412px viewport |

Search results are runtime observations, not fixed record claims.

## Receipt validation

- Exported v1.1 sample receipt: PASS.
- JSON Schema Draft 2020-12 validation: PASS.
- Independent Python canonicalization + SHA-256 recomputation: PASS.
- Re-import of sealed receipt into fresh browser runtime: PASS.
