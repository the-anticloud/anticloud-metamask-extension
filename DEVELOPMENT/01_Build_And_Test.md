# Build and Test

**Project:** `METAMASK_EXTENSION`
**Upstream:** https://github.com/MetaMask/metamask-extension
**License:** MIT

## Quick Start

```bash
git clone https://github.com/MetaMask/metamask-extension
cd metamask-extension
pip install -r requirements-anticloud.txt
python anticloud_main.py --offline --pax-local
```

## Anticloud Improvements Applied

1. PAX L5 Narrow L2 General 27B local market analysis and risk modeling — air-gapped wallet
2. AIOSS append-only transaction audit chain with cryptographic proof
3. AES-256 hardware wallet integration for key storage
4. Single-binary cold wallet software for air-gapped machines
5. Zero-cloud: all signing, verification, and analytics run locally
6. Zero-telemetry: removes all upstream analytics and address tracking
7. Open protocol: integrates with Bitcoin, Ethereum, and Antichain ledger natively
8. Offline price feed with local OHLCV database, no API key required

## Benchmark Targets

| Metric | Target |
| --- | --- |
| Latency | Primary inference task: <5s on CPU, <1s on GPU |
| Throughput | Batch processing: >100 items/hour on single CPU server |
| Memory | <8GB RAM for standard deployment |
| Accuracy | Task-specific accuracy within 5% of cloud-API baseline |

## Build Status

Not yet measured. Run verified build and record actual figures above.
