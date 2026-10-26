# Helenite user guide

[한국어](USER-GUIDE.ko.md)

**Alpha user guide · updated 26 October 2026.** The latest prepared desktop installers are 0.1.9 and bundle plugin 0.1.3. Desktop and plugin version numbers are separate. Helenite is an independent Egress product, not an official Obsidian product. General desktop downloads, payments and the Community plugins listing are not open yet. A separately published plugin alpha is for invited testing and review, not an activated public service. The steps below distinguish the planned public route from the current invited test route. The complete, unaided first-use journey on the final physical devices is still awaiting acceptance.

## What you need

- Obsidian on your computer and phone, and enough free storage for a local copy on each device.
- One computer to host the vault. Keep **Helenite and Obsidian with the Helenite plugin running** on that computer. The desktop app alone does not synchronize its local notes.
- A separate test vault and a backup of any notes you plan to bring over. Do not run iCloud, Obsidian Sync or another sync tool on that same vault during the current test.

Your phone still uses Obsidian. It receives a local copy of the notes; it does not browse a remote disk. A USB cable is **not needed for everyday sync**. An approved external connection is needed to sync away from the host's network. The current test requires an invitation from the test organizer; installing the app does not by itself activate public service.

## 1. Set up the host computer

1. For now, use only the installer supplied for your invited test. When public downloads open, use the matching download at [helenite.net](https://helenite.net/).
2. Install and open Helenite. Current candidates are **macOS Apple Silicon (ARM64)**, **Windows x64**, and an **Ubuntu 22.04 x64 DEB**. They do not establish support for Intel Macs, Windows ARM or every Linux distribution. Mac is signed and notarized; Linux has a signed package. Windows signing is still pending, so its current installer is a test build, not the final public release.
3. Open your test vault in Obsidian. In Helenite choose **Find my vault**, select that same folder, then **Install Helenite**. This adds the plugin to that vault only; merely installing the desktop app does not add it to every vault.
4. In Obsidian open **Settings → Community plugins** and enable **Helenite — By Egress**. Allow community plugins only after checking the supplied plugin. If it does not appear, refresh the installed list or reopen Obsidian; make sure you opened the selected vault.
5. Once Helenite detects the running plugin, choose **Next → Start on this computer → Start with this computer**. Confirm that the server shows **Running**.

Under **Connection settings**, you can enable **Keep running when the window closes** and **Start at login**. These keep/start Helenite, not Obsidian. Continue to keep the host vault open in Obsidian when you want changes to transfer. Background operation does not keep a sleeping computer awake.

## 2. Enable external access

**Public route, once released:** sign in from Helenite using **Sign in with browser**, enter the emailed code in the browser, and approve the app connection. Check the account shown there. Choose **Register this PC** when the account panel offers it. Registration requires an eligible subscription; account login alone does not grant relay access.

**Current invited test:** follow the organizer's test-account and connection instructions. If the app says **PC registration is not available yet**, public registration is closed. Do not guess server addresses, buy another subscription, or change developer settings to bypass that message.

After a PC is registered, access renewal is automatic. Ordinary sign-in expiry does not require repeatedly entering email codes for that registered PC. If access expires or the service cannot confirm eligibility, external transfer pauses and local notes remain available. Follow the displayed account/connection action.

## 3. Prepare Obsidian on the phone

1. Check the vault name shown under **Connect phone** in the PC's Helenite app. In Obsidian on the phone, create and open an **empty local vault with that exact name**. For example, if the PC shows `My research`, use `My research` on the phone too. This prepares the local copy of the same connected vault; the PC's notes will download into it. On iPhone/iPad, turn off **Store in iCloud** for this new vault; on Android choose device storage available to Obsidian.
2. **After listing approval:** open **Settings → Community plugins → Browse**, search for **Helenite**, check **By Egress**, then **Install → Enable**.
3. **Until approval:** Helenite cannot be found through that search. Use only the vault/plugin package and device-specific instructions supplied for your invited test, then enable Helenite in that vault. Do not extract a test package over an existing personal vault. If no installation instructions were supplied, stop here and ask your test organizer.

You install and enable the plugin separately in each vault that uses Helenite. The QR does not install a plugin or create/open a phone vault for you. Obsidian's **Set up Obsidian Sync** option is for Obsidian's own service.

**Already connected with another name?** Keep that vault and its connection. Use Obsidian's vault manager to rename that existing phone vault to the name shown on the PC. If that name is already taken, check which existing vault you want to use before renaming; do not overwrite it. Helenite does not rename the Obsidian folder for you. A matching name alone does not connect two vaults: the existing approved connection identifies the shared vault. There is no need to delete files, clear Helenite's settings or pair again just to fix a name.

## 4. Connect with the QR or a copied code

1. On the host, choose **Connect phone** and create a fresh connection code after external access is ready. Keep that screen open and check its expiry time.
2. On the phone, keep the local vault with the matching name open with Helenite enabled. Scan the PC's QR with the camera and allow it to open Obsidian.
3. If scanning or opening fails, use **Copy connection link** or copy the code on the PC, and transfer it privately to your own phone. In Obsidian open the command palette and run **Helenite: Open sync panel**. Choose **Paste received code**, or **Enter manually**, paste the full code/link and choose **Next**.
4. Review the destination vault and its name. If it contains files, Helenite asks whether to also sync them. Use an empty test vault unless you deliberately want those existing files included. Choose **Request connection to computer**.
5. Compare the verification phrases on both devices and approve that phone on the PC **only if they match**. A familiar device name alone is not enough. Keep the phone in Obsidian while the initial transfer finishes.

Treat a connection link/code as private. Do not post it in a screenshot or support request. If it expires, create a fresh code on the host. If you see **Finish the open connection dialog first**, return to the existing dialog and complete or close it before opening another invitation; do not keep scanning or delete connection settings.

When a shared vault is first created with the latest plugin candidate, Helenite records its name. With the updated desktop server and plugins on both devices, subsequent approved connections also receive that name in encrypted form. Helenite displays it while each device retains its own local files. Obsidian's local vault name is managed separately, so changing a folder name does not automatically rename every device. Existing connections without a shared name continue working and keep their local labels; follow the matching-name guidance above without deleting or reconnecting them. An older server or plugin can still connect, but may not transfer the name.

## 5. Confirm the first sync

The initial connection transfers the vault's supported files. Later passes send changes and reuse encrypted chunks where possible; the whole vault is not downloaded on every edit.

1. Keep the host and phone vaults open. Wait for **Sync complete** and check for deferred items or conflict copies.
2. Create a disposable note on the PC and wait for it on the phone.
3. Add a different line on the phone and check it appears on the PC. Add further devices only after this works.

**Connected** means a connection is ready; it does not prove that every file has arrived. Check the actual test note and **Last synced**. Large initial transfers can take longer. Hidden files and `.obsidian` settings, themes and plugins are excluded; device setup does not copy through note synchronization.

## Everyday use, offline changes and sleep

On mobile, keep **Obsidian in the foreground** for synchronization. Locking the phone or switching apps can suspend the plugin. Background sync is not guaranteed.

When the host sleeps, shuts down or loses internet, you can continue editing notes already on the phone. Pending local changes are retained. On return, wake the host, restore its network and open the same vaults; allow automatic retries to reconnect. Retry delays depend on the error and service response, so there is no guaranteed fixed delivery interval. If you paused sync yourself, select **Resume**. A connection or eligibility error needs the action shown in the app.

Do not reset the vault, remove the plugin's settings or repeatedly generate new pairings just because a transfer is delayed. The saved state is needed to resume safely.

## Conflicts, deletion and recovery

Edits to different parts of a Markdown note can merge automatically within the supported size. Overlapping changes are not guaranteed to merge: Helenite holds them for review and preserves copies.

1. In the sync panel or command palette choose **Review changes**.
2. Compare **this device's** and **the other device's** versions. Choose **Keep this device's version**, **Use the other version**, or **Merge manually → Use merged content** when available.
3. Read the confirmation, then **Confirm and apply**. The result will sync to other devices. If the note changed while you were reviewing it, refresh and compare again.

Remote deletions and replacement of existing attachments also wait for review. Confirming **Apply deletion** can remove the file on other devices; it is not a local-only cleanup action.

For a previous or incomplete file, open **Help · Recovery → Recovery copies → View copies**, then **Restore as a separate file**. Helenite writes a new file in **Helenite Recovered**, leaving the current file alone. The recovered file joins the next sync. Inspect it before moving its content back.

If a write was interrupted, first restore and inspect a separate copy. Use **Keep current file/state** only after checking the current content: it can accept a partial file or an absent file as the state to sync. Keep recovery copies until you are satisfied.

Sync and recovery copies are not an independent backup. Keep a separate, protected backup of your vault, including the private Helenite settings needed for recovery. Do not manually delete hidden Helenite state or share `.obsidian/plugins/helenite/data.json`; it contains connection keys. A lost encryption key cannot be recovered from an email login.

## Account or host recovery

- **Same PC, access revoked:** use **Check PC registration** and follow **Confirm account again → Recover PC registration** if offered. Logging in alone does not undo revocation. This path needs the PC's saved credentials.
- **Lost or replaced PC:** when registration reports another PC, **Replace the previous PC** requires a recent email-code login and explicit confirmation. It transfers connection authority, not notes or encryption keys. You need a surviving vault copy and a paired device. Do not erase the surviving copies to start over.
- **Payment pending/needs review:** do not pay again to clear it. Preserve the displayed status and contact the person/channel that supplied your test access. Public customer support and live payment recovery are not yet available in this draft.

Downloading and installing Helenite is free; synchronization requires a subscription or an explicitly offered trial. The planned price is USD 3/month or USD 24/year. Existing local notes remain readable, copyable and exportable after expiry. Developer-only local testing is not a permanent free sync plan.

When public billing opens, ordinary cancellation stops the next renewal while preserving the paid period. The final service, refund and relay-allowance terms must be published before payment opens; this guide is not a billing agreement. Final release acceptance of subscription enforcement remains pending.

## Updates and getting help

Egress's designated support and privacy contact is **admin@egress.llc**. For an invited test, continue using the test organizer's instructions. No response-time or production-support availability is promised by this draft.

The desktop's **Connection help** includes **Helenite updates**. Once a verified public feed is available, the flow is **Check for updates → Download update → Open installer**. Installation starts only when you choose it; there is no silent installation or automatic rollback. The public feed is currently unpublished, so an unavailable/failed check does not mean your installation is current.

After community approval, update the Obsidian plugin through **Settings → Community plugins** on each device. Before approval, use the update instructions from your test organizer and preserve existing connection settings. Desktop and plugin versions are separate; update all paired devices when a feature requires it.

For an issue, record what you did, the device/OS, the time, and the exact visible message. On the desktop use **Connection help → View diagnostics → Copy diagnostics** and inspect the preview before sharing it privately with your test organizer. Nothing is automatically uploaded. The report excludes notes, vault names/paths, account emails, URLs/IPs and connection secrets. It cannot prove that a phone received a note. Never send passwords, email codes, connection links or plugin `data.json`.

## Current limits

| Area | Current boundary |
| --- | --- |
| Plugin compatibility | Obsidian **1.7.2 or later** is declared; minimum-version and complete final-device acceptance remain pending. |
| File size | Up to **64 MiB** per file once every approved device and the host support large files. Otherwise the **8 MiB** compatibility limit remains. Oversized files are retained locally and deferred, not silently uploaded. |
| Text merging | Automatic merging and manual review text are bounded to **128 KiB**. Overlapping edits may require your choice. |
| Storage | Each device needs room for its local notes, pending changes and recovery copies. Available device storage is not unlimited relay traffic. |
| Relay service | Included transfer allowance and limit behavior are not finalized for public sale. |
| Availability | Host awake/online with Helenite and Obsidian running; phone Obsidian in foreground. No USB requirement. |
| Validation | Mac signing, Linux signed-package/VM checks and Windows VM checks do not complete ordinary-user physical-device acceptance. Windows signing and public release remain pending. |

