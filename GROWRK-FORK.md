# @growrk/node-forge (temporary security fork)

This is upstream `node-forge` v1.4.0 plus digitalbazaar/forge PR #1152 (commit ceba344), which fixes
**GHSA-86w9-cpqp-85rv** (RSA PKCS#1 v1.5 signature forgery via nested DigestAlgorithm garbage).
At fork time (2026-10-21) no patched node-forge release existed.

- Consumed in growrk/link through a pnpm override: `node-forge: npm:@growrk/node-forge@1.4.1-grk.0`.
- **Drop this fork** once upstream publishes node-forge ≥ 1.4.1 with the fix.
- Upstream test suite: 829 passing (828 on v1.4.0 + the new regression test). Upstream's `describe.only` in
  tests/unit/jsbn.js hides the rest of the suite, so the run removes it first.
- License: unchanged upstream LICENSE (BSD-3-Clause / GPL-2.0).
