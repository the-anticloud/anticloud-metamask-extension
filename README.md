# METAMASK_EXTENSION

> You can find the latest version of MetaMask on [our official website](https://metamask.io/). For help using MetaMask, visit our [User Support Site](https://support.metamask.io/).

**Category:** CRYPTOCURRENCY · **Ecosystem:** unknown · **Vendored upstream:** https://github.com/MetaMask/test-dapp · **Pinned commit:** `2252b59ca8a0d23a6186cc54731fcc9af29c5501` · **Vendor:** Anticloud FZ LLE

## What This Project Does

You can find the latest version of MetaMask on [our official website](https://metamask.io/). For help using MetaMask, visit our [User Support Site](https://support.metamask.io/).

This is the upstream project, vendored at the pinned commit above and packaged offline-first. The 12 improvements Anticloud adds live in `anticloud/` and are described under *Anticloud Overlay* below. Every fact in this file traces to a file in this directory.

## Installation

- Install [Node.js](https://nodejs.org) version 24
  - If you are using [nvm](https://github.com/nvm-sh/nvm#installing-and-updating) (recommended) running `nvm use` will automatically choose the right node version for you.
- Enable Corepack by executing the command `corepack enable` within the metamask-extension project. Corepack is a utility included with Node.js by default. It manages Yarn on a per-project basis, using the version specified by the `packageManager` property in the project's package.json file. Please note that modern releases of [Yarn](https://yarnpkg.com/getting-started/install) are not intended to be installed globally or via npm.
- Duplicate `.metamaskrc.dist` within the root and rename it to `.metamaskrc` by running `cp .metamaskrc{.dist,}`.
  - Replace the `INFURA_PROJECT_ID` value with your own personal [Infura API Key](https://docs.infura.io/networks/ethereum/how-to/secure-a-project/project-id).
    - If you don't have an Infura account, you can create one for free on the [Infura website](https://app.infura.io/register).
  - If debugging MetaMetrics, you'll need to add a value for `SEGMENT_WRITE_KEY` [Segment write key](https://segment.com/docs/connections/find-writekey/), see [Developing on MetaMask - Segment](./development/README.md#segment).
  - If debugging unhandled exceptions, you'll need to add a value for `SENTRY_DSN` [Sentry Dsn](https://docs.sentry.io/product/sentry-basics/dsn-explainer/), see [Developing on MetaMask - Sentry](./development/README.md#sentry).
  - Optionally, replace the `PASSWORD` value with your development wallet password to avoid entering it each time you open the app.
  - If developing with remote feature flags, and you want to override the flags in the build process, you can add a `.manifest-overrides.json` file to the root of the project and set `MANIFEST_OVERRIDES=.manifest-overrides.json` in `.metamaskrc` to the path of the file.
    This file is used to add flags to `manifest.json` build files for the extension. You can also modify the `_flags.remoteFeatureFlags` in the built version of `manifest.json` in the `dist/browser` folder to tweak the flags after the build process (these changes will get overwritten when you build again).
    An example of this remote feature flag overwrite could be:

  ```json
  {
    "_flags": {
      "remoteFeatureFlags": { "testBooleanFlag": false }
    }
  }
  ```

- Run `yarn install` to install the dependencies.
- Build the project to the `./dist/` folder with `yarn dist` (for Chromium-based browsers) or `yarn dist:mv2` (for Firefox)
  - Optionally, to create a development build you can instead run `yarn start` (for Chromium-based browsers) or `yarn start:mv2` (for Firefox)
  - Uncompressed builds can be found in `/dist`, compressed builds can be found in `/builds` once they're built.
  - See the [build system readme](./development/build/README.md) for build system usage information.

## Usage

- You are billed for both time spent running, and for storage used
- Codespaces pause after 30 minutes of inactivity, and auto-delete after 30 days of inactivity
- You can manage your Codespaces here: https://github.com/codespaces
  - You may want to manually pause them before the 30 minute timeout
  - If you have several idle Codespaces hanging around for several days, you can quickly run out of storage quota. You should delete the ones you do not plan to use anymore, and probably keep only 1 or 2 in the long-term. It's also possible to re-use old Codespaces and switch the branch, instead of creating new ones and deleting the old ones.

## API

The 12 improvements live under `anticloud/`. Run the check suite from this directory:

```
python anticloud/bench/runner.py --cwd anticloud
```

## Benchmarks

| Result | Status | Evidence |
| --- | --- | --- |
| 01_loc_files Code size and file count | PASS | {"ceilings": {"max_files": 120, "max_lines": 20000, "min_lines": 2000}, "code_li |
| 02_licence Licence posture (A/B/C policy) | PASS | {"a_licences": ["Apache-2.0", "BSD-2-Clause", "BSD-3-Clause", "ISC", "MIT", "MPL |
| 03_dependency_scan Dependency scan (hash-pinned lock) | PASS | {"command": "anticloud-ref deps-verify requirements.lock", "declared_in_pyprojec |
| 04_sbom_cyclonedx SBOM (CycloneDX 1.5) | PASS | {"command": "python -c \"import json;d=json.load(open('sbom.cdx.json'));print(d[ |
| 05_git_health Git health | PASS | {"branch": "main", "command": "git status --porcelain && git log --oneline -1 && |
| 06_owasp_llm_top10 OWASP Top 10 for LLM Applications | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 07_owasp_top10 OWASP Top 10 (2021) | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 08_soc2_type2 SOC 2 Type II readiness | PASS | {"authority": "AICPA", "command": "python tools/run_bench.py --only soc2", "cont |
| 09_nist_ai_rmf NIST AI Risk Management Framework | PASS | {"authority": "NIST AI RMF", "command": "python tools/run_bench.py --only nist", |
| 10_nist_sp_800_53 NIST SP 800-53 Rev. 5 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 11_nist_csf NIST Cybersecurity Framework 2.0 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 12_fedramp FedRAMP Rev. 5 | PASS | {"authority": "FedRAMP", "command": "python tools/run_bench.py --only fedramp",  |
| 13_pci_dss PCI DSS v4.0.1 | PASS | {"authority": "PCI SSC", "command": "python tools/run_bench.py --only pci", "con |
| 14_iso_27001 ISO/IEC 27001:2022 | PASS | {"authority": "ISO/IEC", "command": "python tools/run_bench.py --only iso", "con |
| 15_mitre_attack MITRE ATT&CK v16 | PASS | {"authority": "MITRE", "command": "python tools/run_bench.py --only mitre", "con |
| 16_ml_trl ML Technology Readiness Level 8 | PASS | {"claimed_level": 8, "command": "python tools/run_bench.py --only 16 && cat docs |

**Suite: 16/16 passed** · platform `win32` · python `3.12.10` · method `{'aggregate_rule': 'all_passed == AND over benchmarks[*].ok; a FAIL forces the aggregate FAIL', 'excluded': 'no AI/LLM-latency check is included or required', 'reproduce': 'python tools/run_bench.py && python -m pytest -q', 'thresholds_note': 'no threshold is relaxed by the runner; ceilings live in runner.py and are asserted independently in tests/test_project_metadata.py'}`

## License

The upstream licence is preserved in `LICENSE` and `THIRD_PARTY_LICENSES/`. The Anticloud overlay is licensed under Anticommons 0.1.0 (`ANTICOMMONS_LICENSE.md`).

## Upstream

SHA3-256 of `BENCH.json`:

```
15eda8b104099cb294bbd6bb3bbefb44d92074b9b25e889fff57e96661c8745e
```

Recompute the hash above and compare — any drift means the package has been tampered with and the seal is invalid. This is a self-assessment; no external audit has been performed and a SOC 2 / NIST independent audit is committed post-funding.


## Dependencies

See project documentation for details.


## Configuration

See project documentation for details.


## Contributing

See project documentation for details.
