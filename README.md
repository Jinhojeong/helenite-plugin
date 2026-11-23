# Helenite

By **Egress**. Independently developed encrypted vault sync for Obsidian.
Helenite is not an official Obsidian product and is not affiliated with Obsidian.

**Development alpha. The plugin is available in the [Obsidian community directory](https://community.obsidian.md/plugins/helenite). Installation is free. Sync through Helenite is currently by invitation. New subscriptions are closed.** [Current availability and setup](https://helenite.net/guide?lang=en)
This repository contains built plugin release assets. Source development takes place in a separate private repository.
Obsidian supports a [separate private source repository](https://docs.obsidian.md/community-directory/manage-entry) for build verification through its Community directory GitHub App.

## Install and connect

1. In the Helenite desktop app, select your computer’s Obsidian vault and install the plugin there. Enable Helenite in Obsidian and keep the host app and vault open.
2. On your phone, create and open an empty local Obsidian vault with the same name shown on the computer.
3. In that vault, open **Settings → Community plugins → Browse**, search for **Helenite**, select **Install**, then **Enable**. The directory lists Jinho Jeong. The installed plugin credits Egress.
4. Scan the computer's connection QR and choose the target vault if prompted. Approve the phone on the computer when all four English words match in order. If one device shows a long code, expand **Full fingerprint for older versions** on the other device and compare the complete codes.

The QR connects a plugin that is already installed; it does not install a plugin or create an Obsidian vault. Use an empty local vault for the first test. An Android phone does not need access to the host's iCloud folder.

Setup, troubleshooting and recovery: [English guide](docs/USER-GUIDE.md) · [한국어 가이드](docs/USER-GUIDE.ko.md).

Obsidian manages plugin updates through the directory. The three files for a specific release are also available in [GitHub releases](https://github.com/Jinhojeong/helenite-plugin/releases).

## Payment and accounts

**Community payment category: Paid.** Downloading and installing the plugin is free; Helenite synchronization requires an active subscription or an explicitly offered trial. Existing local notes remain readable, copyable and exportable after the subscription ends. Development-only local testing is not a permanent free synchronization plan.

The listed prices are **USD 3 per month or USD 24 per year**. The public account page offers email sign-in. Paid checkout is closed during this test. Invited testers can use the connection details supplied with their invitation.

Your computer hosts the vault. The listed plan includes **10 GB of relay transfers per account per UTC calendar month**. An available direct connection can continue after that allowance is used. The relay allowance resets on the first of the month at 00:00 UTC. Read the [service terms](https://helenite.net/terms?lang=en).

## Network and privacy disclosures

- **Your configured host/relay:** the plugin sends and receives encrypted sync records, pairing requests and connection status using HTTP(S) and WebSocket connections. Connection credentials and keys are retained in this vault's local plugin data. Production external connections require HTTPS/WSS; loopback HTTP is available for local development.
- **Helenite-managed connectivity, when configured:** Cloudflare Workers and Durable Objects carry encrypted note records and manage routing, device authorization and usage limits. The service also processes routing/account/device identifiers, connection timing, traffic volumes, protocol authorization headers and pairing metadata. Content encryption does not hide all transport metadata. Operational authorization, quota and accounting records are retained. Traffic can be buffered briefly for delivery; the service is not a backup or permanent vault store. Host availability is still required.
- **Obsidian and GitHub:** Obsidian obtains installation/update assets from this public GitHub repository. There is no separate plugin self-updater.
- **Client telemetry:** this plugin does not send analytics, advertising or crash-report telemetry. Server-side operational records are separate from client analytics. The [privacy notice](https://helenite.net/privacy) describes how Egress and its providers handle these records.
- **Files:** the plugin works within the currently opened vault, including its local plugin settings and recovery copies under `.helenite/backups`. It does not request access outside that vault. Local plugin settings can contain encryption keys and credentials; local notes and recovery copies are not separately encrypted at rest by Helenite. Protect the device and its backups. The separately installed desktop host application also keeps local service configuration and is not part of this plugin package. Hidden files and Obsidian configuration are excluded from sync.

Do not post connection QRs, connection codes, plugin data files, keys or vault contents in public issues. A connection code grants access to begin pairing and is private.

## Current alpha limits

- Individual synced files can be up to **64 MiB** only after every approved device has announced large-file support; otherwise the compatibility limit remains **8 MiB**. Update the relay and all paired plugins, and let each device sync before sending larger files. This release does not support unlimited file sizes or whole-vault streaming.
- Nonoverlapping Markdown edits can merge automatically within a **128 KiB** text limit when a shared version is available. Overlapping or otherwise unmergeable edits preserve both versions for review. You can choose a version or provide merged text; there is no promise that every simultaneous edit will merge automatically.
- Existing binary replacements and remote deletions require an explicit review decision. Choices apply to the versions shown; if either version changes, review again. Interrupted writes or unexpected edits remain held for recovery, while other eligible files can continue syncing.
- Recovery copies stay outside the synchronized file list. The plugin's recovery view restores a separate file into **Helenite Recovered** for inspection. These local copies do not replace an independent backup and cannot recover a lost encryption key or notes missing from every device.
- Mobile sync runs while Obsidian is active. Continuous background synchronization on iOS or Android is not guaranteed.
- Helenite 0.1.7 requires **Obsidian 1.7.4** or later. Version 0.1.5 was tested on desktop Obsidian 1.7.4 for settings persistence and two-way sync with a local test client. Physical-device testing of the four-word comparison is pending.
- Start with a disposable test vault and retain your own backups. Automated test results do not replace Windows, macOS, Linux, Android and iPhone acceptance.

## Source and license

Helenite was independently implemented and does not include or depend on the Obsidian LiveSync repository. Bundled code remains readable; there is no source map or private monorepo archive in the release.

The LICENSE in this repository governs use of the distributed plugin. Source is private; public binaries do not imply an open-source license.

The English words used for pairing come from the BIP-39 word list supplied by python-mnemonic. Its MIT license and copyright notice are included in the distributed main.js. The host application supplies Obsidian.

Product information: [helenite.net](https://helenite.net). Privacy and support contact: **admin@egress.llc**. Do not post credentials or personal vault contents.
