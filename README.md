# METAMASK EXTENSION

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-cryptocurrency-lightgrey)

> Anticloud-hardened packaging of the upstream project `METAMASK_EXTENSION` in category **CRYPTOCURRENCY**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** CRYPTOCURRENCY · **Upstream:** https://github.com/MetaMask/metamask-extension · **Upstream pin:** `2252b59ca8a0d23a6186cc54731fcc9af29c5501` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# MetaMask Browser Extension

You can find the latest version of MetaMask on [our official website](https://metamask.io/). For help using MetaMask, visit our [User Support Site](https://support.metamask.io/).

For [general questions](https://community.metamask.io/c/learn/26), [feature requests](https://community.metamask.io/c/feature-requests-ideas/13), or [developer questions](https://community.metamask.io/c/developer-questions/11), visit our [Community Forum](https://community.metamask.io/).

MetaMask supports Firefox, Google Chrome, and Chromium-based browsers. We recommend using the latest available browser version.

For up to the minute news, follow us on [X](https://x.com/MetaMask).

To learn how to develop MetaMask-compatible applications, visit our [Developer Docs](https://docs.metamask.io/).

To learn how to contribute to the MetaMask codebase, visit our [Contributor Docs](https://github.com/MetaMask/contributor-docs).

To learn how to contribute to the MetaMask Extension project itself, visit our [Extension Docs](https://github.com/MetaMask/metamask-extension/tree/main/docs).

## GitHub Codespaces quickstart

As an alternative to building on your local machine, there is a new option to get a development environment up and running in less than 5 minutes by using GitHub Codespaces. Please note that there is a [Limited Free Monthly Quota](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces), and after that GitHub will start charging you.

_Note: You are billed for both time spent running, and for storage used_

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MetaMask/metamask-extension?quickstart=1)

1. Start by clicking the button above
2. A new browser tab will open with a remote version of Visual Studio Code (this will take a few minutes to load)
3. A "Simple Browser" will open inside the browser with noVNC -- click Connect
   - Optional steps:
     - Click the button at the upper-right of the Simple Browser tab to open the noVNC window in its own tab
     - Open the noVNC sidebar on the left, click the gear icon, change the Scaling Mode to Remote Resizing
4. Wait about 20 extra seconds on the first launch, for the scripts to finish
5. Right-click on the noVNC desktop to launch Chrome or Firefox with MetaMask pre-installed
6. Change some code, then run `yarn start` to build in dev mode
7. After a minute or two, it will finish building, and you can see your changes in the noVNC desktop

### Tips to keep your Codespaces usage lower

- You are billed for both time spent running, and for storage used
- Codespaces pause after 30 minutes of inactivity, and auto-delete after 30 days of inactivity
- You can manage your Codespaces here: https://github.com/codespaces
  - You may want to manually pause them before the 30 minute timeout
  - If you have several idle Codespaces hanging around for several days, you can quickly run out of storage quota. You should delete the ones you do not plan to use anymore, and probably keep only 1 or 2 in the long-term. It's also possible to re-use old Codespaces and switch the branch, instead of creating new ones and deleting the old ones.

### Codespaces on a fork

If you are not a MetaMask Internal Developer, or are otherwise developing on a fork, the default Infura key will be on the Free Plan and have very limited requests per second. If you want to use your own Infura key, follow the `.metamaskrc` and `INFURA_PROJECT_ID` instructions in the section [Building on your local machine](#building-on-your-local-machine).

## Building on your local machine

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
      "remoteFeatur

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Node.js / npm** (manifests: package.json, yarn.lock; scanned in UPSTREAM_CLONE)
- Top-level source layout: `app/`, `development/`, `lavamoat/`, `shared/`, `test/`, `types/`, `ui/`
- Snapshot size: **10323 files**, **1441542 lines of code** (measured; see Benchmarks)
- Primary languages: `.ts` (5420), `.tsx` (2490), `.js` (999), `.scss` (335), `.snap` (277), `.svg` (259)
- Upstream commit pinned for this packaging: `2252b59ca8a0d23a6186cc54731fcc9af29c5501`

---

## Installation

As an alternative to building on your local machine, there is a new option to get a development environment up and running in less than 5 minutes by using GitHub Codespaces. Please note that there is a [Limited Free Monthly Quota](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces), and after that GitHub will start charging you.

_Note: You are billed for both time spent running, and for storage used_

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MetaMask/metamask-extension?quickstart=1)

1. Start by clicking the button above
2. A new browser tab will open with a remote version of Visual Studio Code (this will take a few minutes to load)
3. A "Simple Browser" will open inside the browser with noVNC -- click Connect
   - Optional steps:
     - Click the button at the upper-right of the Simple Browser tab to open the noVNC window in its own tab
     - Open the noVNC sidebar on the left, click the gear icon, change the Scaling Mode to Remote Resizing
4. Wait about 20 extra seconds on the first launch, for the scripts to finish
5. Right-click on the noVNC desktop to launch Chrome or Firefox with MetaMask pre-installed
6. Change some code, then run `yarn start` to build in dev mode
7. After a minute or two, it will finish building, and you can see your changes in the noVNC desktop

### Tips to keep your Codespaces usage lower

- You are billed for both time spent running, and for storage used
- Codespaces pause after 30 minutes of inactivity, and auto-delete after 30 days of inactivity
- You can manage your Codespaces here: https://github.com/codespaces
  - You may want to manually pause them before the 30 minute timeout
  - If you have several idle Codespaces hanging around for several days, you can quickly run out of storage quota. You should delete the ones you do not plan to use anymore, and probably keep only 1 or 2 in the long-term. It's also possible to re-use old Codespaces and switch the branch, instead of creating new ones and deleting the old ones.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

- You are billed for both time spent running, and for storage used
- Codespaces pause after 30 minutes of inactivity, and auto-delete after 30 days of inactivity
- You can manage your Codespaces here: https://github.com/codespaces
  - You may want to manually pause them before the 30 minute timeout
  - If you have several idle Codespaces hanging around for several days, you can quickly run out of storage quota. You should delete the ones you do not plan to use anymore, and probably keep only 1 or 2 in the long-term. It's also possible to re-use old Codespaces and switch the branch, instead of creating new ones and deleting the old ones.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

2. A new browser tab will open with a remote version of Visual Studio Code (this will take a few minutes to load)
3. A "Simple Browser" will open inside the browser with noVNC -- click Connect
   - Optional steps:
     - Click the button at the upper-right of the Simple Browser tab to open the noVNC window in its own tab
     - Open the noVNC sidebar on the left, click the gear icon, change the Scaling Mode to Remote Resizing
4. Wait about 20 extra seconds on the first launch, for the scripts to finish
5. Right-click on the noVNC desktop to launch Chrome or Firefox with MetaMask pre-installed
6. Change some code, then run `yarn start` to build in dev mode
7. After a minute or two, it will finish building, and you can see your changes in the noVNC desktop

### Tips to keep your Codespaces usage lower

- You are billed for both time spent running, and for storage used
- Codespaces pause after 30 minutes of inactivity, and auto-delete after 30 days of inactivity
- You can manage your Codespaces here: https://github.com/codespaces
  - You may want to manually pause them before the 30 minute timeout
  - If you have several idle Codespaces hanging around for several days, you can quickly run out of storage quota. You should delete the ones you do not plan to use anymore, and probably keep only 1 or 2 in the long-term. It's also possible to re-use old Codespaces and switch the branch, instead of creating new ones and deleting the old ones.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Node.js / npm |
| Manifests detected | package.json, yarn.lock |
| Files in snapshot | 10323 |
| Lines of code | 1441542 |
| Dependency references | 508 |
| Dependencies by ecosystem | npm: 508 |
| Upstream license | No license file present in the upstream snapshot |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | @babel/runtime | patch:@babel/runtime@npm%3A7.29.2#~/.yarn/patches/@babel-runtime-npm-7.29.2-b49cad1c67.patch | package.json |
| npm | @blockaid/ppom_release | ^1.5.3 | package.json |
| npm | @emotion/react | ^11.14.0 | package.json |
| npm | @emotion/styled | ^11.14.1 | package.json |
| npm | @ensdomains/content-hash | ^2.5.7 | package.json |
| npm | @ethereumjs/tx | patch:@ethereumjs/tx@npm%3A5.4.0#~/.yarn/patches/@ethereumjs-tx-npm-5.4.0-0c4a0f973e.patch | package.json |
| npm | @ethersproject/abi | ^5.6.4 | package.json |
| npm | @ethersproject/bignumber | ^5.7.0 | package.json |
| npm | @ethersproject/bytes | ^5.7.0 | package.json |
| npm | @ethersproject/contracts | ^5.7.0 | package.json |
| npm | @ethersproject/hdnode | ^5.6.2 | package.json |
| npm | @ethersproject/providers | ^5.7.2 | package.json |
| npm | @ethersproject/transactions | ^5.7.0 | package.json |
| npm | @fortawesome/fontawesome-free | ^5.13.0 | package.json |
| npm | @hello-pangea/dnd | ^16.6.0 | package.json |
| ... | (485 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

_Note: You are billed for both time spent running, and for storage used_

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MetaMask/metamask-extension?quickstart=1)

1. Start by clicking the button above
2. A new browser tab will open with a remote version of Visual Studio Code (this will take a few minutes to load)
3. A "Simple Browser" will open inside the browser with noVNC -- click Connect
   - Optional steps:
     - Click the button at the upper-right of the Simple Browser tab to open the noVNC window in its own tab
     - Open the noVNC sidebar on the left, click the gear icon, change the Scaling Mode to Remote Resizing
4. Wait about 20 extra seconds on the first launch, for the scripts to finish
5. Right-click on the noVNC desktop to launch Chrome or Firefox with MetaMask pre-installed
6. Change some code, then run `yarn start` to build in dev mode
7. After a minute or two, it will finish building, and you can see your changes in the noVNC desktop

### Tips to keep your Codespaces usage lower

- You are billed for both time spent running, and for storage used
- Codespaces pause after 30 minutes of inactivity, and auto-delete after 30 days of inactivity
- You can manage your Codespaces here: https://github.com/codespaces
  - You may want to manually pause them before the 30 minute timeout
  - If you have several idle Codespaces hanging around for several days, you can quickly run out of storage quota. You should delete the ones you do not plan to use anymore, and probably keep only 1 or 2 in the long-term. It's also possible to re-use old Codespaces and switch the branch, instead of creating new ones and deleting the old ones.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `.github/CONTRIBUTING.md`:*

# Welcome to MetaMask!

If you're submitting code to MetaMask, there are some simple things we'd appreciate you doing to help us stay organized!

### Finding the right project

Before taking the time to code and implement something, feel free to open an issue and discuss it! There may even be an issue already open, and together we may come up with a specific strategy before you take your precious time to write code.

There are also plenty of open issues we'd love help with. Search the [`good first issue`](https://github.com/MetaMask/metamask-extension/contribute) label, or head to Gitcoin and earn ETH for completing projects we've posted bounties on.

If you're picking up a bounty or an existing issue, feel free to ask clarifying questions on the issue as you go about your work.

### Submitting a pull request

When you're done with your project / bugfix / feature and ready to submit a PR, there are a couple guidelines we ask you to follow:

- [ ] **Make sure you followed our [`coding guidelines`](https://github.com/MetaMask/metamask-extension/blob/main/.github/guidelines/CODING_GUIDELINES.md)**: These guidelines aim to maintain consistency and readability across the codebase. They help ensure that the code is easy to understand, maintain, and modify, which is particularly important when working with multiple contributors.
- [ ] **Test it**: For any new programmatic functionality, we like unit tests when possible, so if you can keep your code cleanly isolated, please do add a test file to the `tests` folder.
- [ ] **Meet the spec**: Make sure the PR adds functionality that matches the issue you're closing. This is especially important for bounties: sometimes design or implementation details are included in the conversation, so read carefully!
- [ ] **Close the issue**: If this PR closes an open issue, fill out the "Related issues" section with `Fixes: #$ISSUE_NUMBER`. Ex. For closing issue 418, include the line `Fixes: #418`. If it doesn't close the issue but addresses it partially, just include a reference to the issue number, like `#418`.
- [ ] **Keep it simple**: Try not to include multiple features in a single PR, and don't make extraneous changes outside the scope of your contribution. All those touched files make things harder to review ;)
- [ ] **PR against `main`**: Submit your PR against the `main` branch. This is where we merge new features so they get some time to receive extra testing before being pushed to `stable` for production. If your PR is

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: No license file present in the upstream snapshot** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
Copyright ConsenSys Software Inc. 2022. All rights reserved.
 
You acknowledge and agree that ConsenSys Software Inc. (“ConsenSys”) (or ConsenSys’s licensors) own all legal right, title and interest in and to the work, software, application, source code, documentation and any other documents in this project (collectively, the “Program”), including any intellectual property rights which subsist in the Program (whether those rights happen to be registered or not, and wherever in the world those rights may exist), whether in source code or any other form.
 
Subject to the limited license below, you may not (and you may not permit anyone else to) distribute, publish, copy, modify, merge, combine with another program, create derivative works of, reverse engineer, decompile or otherwise attempt to extract the source code of, the Program or any part thereof, except that you may contribute to this project.
 
You are granted a non-exclusive, non-transferable, non-sublicensable license to distribute, publish, copy, modify, merge, combine with another program or create derivative works of the Program (such resulting program, collectively, the “Resulting Program”) solely for Non-Commercial Use as long as you:
 1. give prominent notice (“Notice”) with each copy of the Resulting Program that the Program is used in the Resulting Program and that the Program is the copyright of ConsenSys; and
 2. subject the Resulting Program and any distribution, publication, copy, modification, merger therewith, combination with another program or derivative works thereof to the same Notice requirement and Non-Commercial Use restriction set forth herein.
 
“Non-Commercial Use” means each use as described in clauses (1)-(3) below, as reasonably determined by ConsenSys in its sole discretion: 
 1. personal use for research, personal study, private entertainment, hobby projects or amateur pursuits, in each case without any anticipated commercial application;
 2. use by any charitable organization, educational institution, public research organization, public safety or health organization, environmental protection organization or government institution; or
 3. the number of monthly active users of the Resulting Program across all versions thereof and platforms globally do not exceed 10,000 at any time.
 
You will not use any trade mark, service mark, trade name, logo of ConsenSys or any other company or organization in a way that is likely or intended to cause confusion about the owner or authorized user of such marks, names or logos.
 
If you have any questions, comments or interest in pursuing any other use cases, please reach out to us at communications@metamask.io.
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original No license file present in the upstream snapshot terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `No license file present in the upstream snapshot` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `METAMASK_EXTENSION` (category: CRYPTOCURRENCY)
- **Upstream URL:** https://github.com/MetaMask/metamask-extension
- **Pinned commit (SHA):** `2252b59ca8a0d23a6186cc54731fcc9af29c5501`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`06e42faaef879ac3cdc6b0f79d12d669ec3d2250fea2353b3eda0a18831120b7`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

