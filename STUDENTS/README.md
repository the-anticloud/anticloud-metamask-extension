# Students — METAMASK_EXTENSION

**Project:** METAMASK_EXTENSION  
**Category:** CRYPTOCURRENCY  
**Upstream:** https://github.com/MetaMask/metamask-extension  
**Pinned commit:** `a6765b12ed73e0c18eace82d1f0ead55226c64ec`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `398ca6532f3a60e38ec7f3cd2b2528f2e67459647272c4ad361909c0c9921f25`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `a6765b12ed73e0c18eace82d1f0ead55226c64ec`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `398ca6532f3a60e38ec7f3cd2b2528f2e67459647272c4ad361909c0c9921f25`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
