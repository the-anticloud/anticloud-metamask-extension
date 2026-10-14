# Educators — METAMASK_EXTENSION

**Project:** METAMASK_EXTENSION  
**Category:** CRYPTOCURRENCY  
**Upstream:** https://github.com/MetaMask/metamask-extension  
**Pinned commit:** `a6765b12ed73e0c18eace82d1f0ead55226c64ec`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `398ca6532f3a60e38ec7f3cd2b2528f2e67459647272c4ad361909c0c9921f25`  
**Date:** October 2026

## Teaching with METAMASK_EXTENSION

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `398ca6532f3a60e38ec7f3cd2b2528f2e67459647272c4ad361909c0c9921f25` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
