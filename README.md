# Helenite

By **Egress**. Independently developed encrypted vault sync for Obsidian.
Helenite is not an official Obsidian product and is not affiliated with Obsidian.

**Release status: development alpha; community listing and paid service are not yet available.**
This repository contains built plugin release assets. Source development takes place in a separate private repository.
Obsidian supports a [separate private source repository](https://docs.obsidian.md/community-directory/manage-entry) for build verification through its Community directory GitHub App.
Closed-source community submissions are reviewed by Obsidian case by case; this document does not indicate approval.

## Install and connect

After the community listing is approved:

1. In Obsidian, open **Settings → Community plugins → Browse**, search for **Helenite**, then install and enable it in the vault you want to connect.
2. Open Helenite on your host computer and select its vault. Keep the host computer and its Obsidian vault running.
3. On your phone, create an empty local vault in Obsidian with the same name shown on the PC, then install and enable Helenite in that vault. Scan the computer's connection QR, choose the target vault if Obsidian asks, and confirm the connection.
4. Compare the displayed confirmation on both devices and approve the phone on your computer.

The QR connects a plugin that is already installed; it does not install a plugin or create an Obsidian vault. Use an empty local vault for the first test. An Android phone does not need access to the host's iCloud folder.

Setup, troubleshooting and recovery: [English guide](docs/USER-GUIDE.md) · [한국어 가이드](docs/USER-GUIDE.ko.md).

Until listing approval, invited testers can install the three files from the matching [GitHub release](https://github.com/Jinhojeong/helenite-plugin/releases) in their vault's plugin folder and enable Helenite. General users should wait for the community installation route. Obsidian manages plugin updates; Helenite does not install or update itself or its dependencies.

## Payment and accounts

**Community payment category: Paid.** Downloading and installing the plugin is free; Helenite synchronization requires an active subscription or an explicitly offered trial. Existing local notes remain readable, copyable and exportable after the subscription ends. Development-only local testing is not a permanent free synchronization plan.

The planned commercial service costs **USD 3 per month or USD 24 per year** and will require a Helenite account. The desktop app implements account sign-in, PC registration, subscription eligibility renewal and connection recovery. These features have not opened as a public production service: live payments, public account enrollment and production connectivity remain unavailable. Do not treat this build as a purchased or activated subscription. Invited tests use isolated test accounts or a locally configured host; the plugin itself has no account login screen. Final subscription enforcement across the offered connection modes still requires release acceptance.

Your computer provides the vault host. A subscription is not hosted vault storage. Final included relay traffic and release limits must be published before paid access is enabled.

## Network and privacy disclosures

- **Your configured host/relay:** the plugin sends and receives encrypted sync records, pairing requests and connection status using HTTP(S) and WebSocket connections. Connection credentials and keys are retained in this vault's local plugin data. Production external connections require HTTPS/WSS; loopback HTTP is available for local development.
- **Helenite-managed connectivity, when configured:** Cloudflare Workers and Durable Objects carry encrypted note records and manage routing, device authorization and usage limits. The service also processes routing/account/device identifiers, connection timing, traffic volumes, protocol authorization headers and pairing metadata. Content encryption does not hide all transport metadata. Operational authorization, quota and accounting records are retained. Traffic can be buffered briefly for delivery; the service is not a backup or permanent vault store. Host availability is still required.
- **Obsidian and GitHub:** Obsidian obtains installation/update assets from this public GitHub repository. There is no separate plugin self-updater.
- **Client telemetry:** this plugin does not send analytics, advertising or crash-report telemetry. Server-side operational records are separate from client analytics. Read the [pre-release privacy notice](https://helenite.net/privacy) for the current test handling, providers and remaining operational limits. A complete operational policy is required before public service activation.
- **Files:** the plugin works within the currently opened vault, including its local plugin settings and recovery copies under `.helenite/backups`. It does not request access outside that vault. Local plugin settings can contain encryption keys and credentials; local notes and recovery copies are not separately encrypted at rest by Helenite. Protect the device and its backups. The separately installed desktop host application also keeps local service configuration and is not part of this plugin package. Hidden files and Obsidian configuration are excluded from sync.

Do not post connection QRs, connection codes, plugin data files, keys or vault contents in public issues. A connection code grants access to begin pairing and is private.

## Current alpha limits

- Individual synced files can be up to **64 MiB** only after every approved device has announced large-file support; otherwise the compatibility limit remains **8 MiB**. Update the relay and all paired plugins, and let each device sync before sending larger files. This release does not support unlimited file sizes or whole-vault streaming.
- Nonoverlapping Markdown edits can merge automatically within a **128 KiB** text limit when a shared version is available. Overlapping or otherwise unmergeable edits preserve both versions for review. You can choose a version or provide merged text; there is no promise that every simultaneous edit will merge automatically.
- Existing binary replacements and remote deletions require an explicit review decision. Choices apply to the versions shown; if either version changes, review again. Interrupted writes or unexpected edits remain held for recovery, while other eligible files can continue syncing.
- Recovery copies stay outside the synchronized file list. The plugin's recovery view restores a separate file into **Helenite Recovered** for inspection. These local copies do not replace an independent backup and cannot recover a lost encryption key or notes missing from every device.
- Mobile sync runs while Obsidian is active. Continuous background synchronization on iOS or Android is not guaranteed.
- Declared minimum Obsidian version: **1.7.2**. Full minimum-version and physical-device release acceptance are still pending.
- Start with a disposable test vault and retain your own backups. Automated test results do not replace Windows, macOS, Linux, Android and iPhone acceptance.

## Source and license

Helenite was independently implemented and does not include or depend on the Obsidian LiveSync repository. Bundled code remains readable; there is no source map or private monorepo archive in the release.

The LICENSE in this repository governs use of the distributed plugin. Source is private; public binaries do not imply an open-source license.

The bundle currently contains first-party Helenite runtime code only; Obsidian is supplied by the host application. The build review rejects added bundled third-party dependencies until their notices and license obligations are explicitly reviewed.

Product information: [helenite.net](https://helenite.net). Privacy and support contact: **admin@egress.llc**. This public artifact repository may be used for non-sensitive installation issues after it is created. Do not post credentials or personal vault contents.
