# Vantage releases

Signed builds of **Vantage** by AVYR LABS: every machine you look after on one screen, for Mac and
Linux. A small agent runs on each machine and the app talks to it directly over your own network.
No Vantage server, no account, no telemetry. Free during launch.

Site and docs: https://vantage.theavyrlabs.com

## Download

Every version is a [release](https://github.com/TheAvyrLabs/vantage-releases/releases). The latest:
https://github.com/TheAvyrLabs/vantage-releases/releases/latest

| You have | Download |
| --- | --- |
| A Mac (macOS 10.15 or newer, Apple silicon or Intel) | `Vantage_<version>_universal.dmg` |
| Linux on x86_64 | `Vantage_<version>_amd64.deb` or `Vantage-<version>-1.x86_64.rpm` |
| Linux on arm64 | `Vantage_<version>_arm64.deb`, `Vantage-<version>-1.aarch64.rpm` or `Vantage_<version>_aarch64.AppImage` |

The app installs the agent on your machines for you over SSH. To install the agent by hand, read
`install.sh` from the release first, then run it with `sudo sh install.sh`.

## First launch on a Mac

The Mac build is signed by AVYR LABS but not notarized yet. The first time you open it, macOS shows
a warning: open System Settings > Privacy & Security, press Open Anyway, and confirm with your
password. You do this once.

## Check what you downloaded

Each release has `SHA256SUMS` and its signature `SHA256SUMS.sshsig`, made with the AVYR LABS
publisher key:

    0siZga9F6kxooTCOz27/LRlPjWsI1hEzEKYX90JCR9I=

`install.sh` checks the signature and every checksum before it installs anything. The Mac app is
signed with the "AVYR LABS Code Signing" certificate, SHA-256
`41c6135233693e6f8f23fbabbea9d05c9beddbc269bb43f1a38b6cf2fbbb7bab`.

## Licence

Vantage is under the Functional Source License, [FSL-1.1-ALv2](LICENSE). You may use, copy, change
and share it for any purpose except offering it, or something that does the same job, to others as a
commercial product or service. Two years after each version comes out, that version is also yours
under the Apache License 2.0.

This repository holds the releases. Questions and problems: https://vantage.theavyrlabs.com/contact.html
