# Technical Architecture — METAMASK_EXTENSION

**Upstream:** [https://github.com/MetaMask/metamask-extension](https://github.com/MetaMask/metamask-extension)
**License:** MIT
**Category:** CRYPTOCURRENCY
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Browser wallet for crypto

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B local market analysis and risk modeling — air-gapped wallet
2. AIOSS append-only transaction audit chain with cryptographic proof
3. AES-256 hardware wallet integration for key storage
4. Single-binary cold wallet software for air-gapped machines
5. Zero-cloud: all signing, verification, and analytics run locally
6. Zero-telemetry: removes all upstream analytics and address tracking
7. Open protocol: integrates with Bitcoin, Ethereum, and Antichain ledger natively
8. Offline price feed with local OHLCV database, no API key required

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_metamask_extension.spec` or `go build -o metamask_extension`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |