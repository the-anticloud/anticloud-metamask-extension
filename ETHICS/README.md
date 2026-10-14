# Ethics — METAMASK_EXTENSION

**Project:** METAMASK_EXTENSION  
**Category:** CRYPTOCURRENCY  
**Upstream:** https://github.com/MetaMask/metamask-extension  
**Pinned commit:** `a6765b12ed73e0c18eace82d1f0ead55226c64ec`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `398ca6532f3a60e38ec7f3cd2b2528f2e67459647272c4ad361909c0c9921f25`  
**Date:** October 2026

## Position

METAMASK_EXTENSION is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
