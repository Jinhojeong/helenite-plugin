# Helenite user guide

[한국어](USER-GUIDE.ko.md)

**Helenite user guide · 27 November 2026.** Download the Apple silicon Mac or Ubuntu x64 installer from the [Helenite website](https://helenite.net/?lang=en). Contact Egress for the unsigned Windows x64 test installer. Install the [Helenite plugin](https://community.obsidian.md/plugins/helenite) in Obsidian. Check your access in your [Helenite account](https://helenite.net/account?lang=en).

## What you need

- Obsidian on your computer and phone, and enough free storage for a local copy on each device.
- One computer to host the vault. Keep **Helenite and Obsidian with the Helenite plugin running** on that computer. The desktop app alone does not synchronize its local notes.
- A separate test vault and a backup of any notes you plan to bring over. Do not run iCloud, Obsidian Sync or another sync tool on that same vault during the current test.

Your phone still uses Obsidian. It receives a local copy of the notes; it does not browse a remote disk. A USB cable is **not needed for everyday sync**. An approved external connection is needed to sync away from the host's network.

## 1. Set up the host computer

1. Choose your operating system on the [Helenite download page](https://helenite.net/?lang=en). For the Windows x64 test installer, [contact Egress](mailto:admin@egress.llc?subject=Helenite%20Windows%20x64).
2. On Windows, run `Get-FileHash -Algorithm SHA256` in PowerShell with the path to the downloaded installer. Before opening it, compare the output with the SHA-256 supplied by Egress for that version.
3. Install and open the build for your system. The supported builds are for **Apple silicon Macs (ARM64)**, **Windows x64** and **Ubuntu 22.04 x64 (DEB)**.
4. Open your test vault in Obsidian. In Helenite choose **Find my vault**, select that same folder, then **Install Helenite**. This adds the plugin to that vault only; merely installing the desktop app does not add it to every vault.
5. In Obsidian open **Settings → Community plugins** and enable **Helenite — By Egress**. Allow community plugins only after checking the supplied plugin. If it does not appear, refresh the installed list or reopen Obsidian; make sure you opened the selected vault.
6. Once Helenite detects the running plugin, choose **Next → Start on this computer → Start with this computer**. Confirm that the server shows **Running**.

Under **Connection settings**, you can enable **Keep running when the window closes** and **Start at login**. On desktop versions that offer this option, turn on **Start at login** and then **Also open this vault in Obsidian at login** to open the selected vault. This choice is off by default and applies only to that vault. Continue to keep the host vault open in Obsidian when you want changes to transfer. Background operation does not keep a sleeping computer awake.

## 2. Enable external access

**Try sync without a card.** When a free trial is available on the account page, sign in with your email and choose the trial. Your seven days start when your first PC registers successfully. When the trial ends, external sync pauses and you can still open your local notes. To continue with a subscription, choose a plan on the same account.

**Register your PC.** In Helenite, select **Sign in with browser**. Use the email you enrolled or subscribed with, confirm the account, and approve the app connection. Then choose **Register this PC**. If the app says **PC registration is not available yet**, keep your account and vault and check again later.

After a PC is registered, access renewal is automatic. Ordinary sign-in expiry does not require repeatedly entering email codes for that registered PC. If access expires or the service cannot confirm eligibility, external transfer pauses and local notes remain available. Follow the displayed account/connection action.

## 3. Prepare Obsidian on the phone

1. Check the vault name shown under **Connect phone** in the PC's Helenite app. In Obsidian on the phone, create and open an **empty local vault with that exact name**. For example, if the PC shows `My research`, use `My research` on the phone too. This prepares the local copy of the same connected vault; the PC's notes will download into it. On iPhone/iPad, turn off **Store in iCloud** for this new vault; on Android choose device storage available to Obsidian.
2. In **Settings → Community plugins → Browse**, search for **Helenite** and open its [official listing](https://community.obsidian.md/plugins/helenite). Select **Install**, then **Enable**.

The directory lists **Jinho Jeong**, and the installed plugin identifies **Egress** as its author. Use Obsidian 1.7.4 or later.

You install and enable the plugin separately in each vault that uses Helenite. The QR does not install a plugin or create/open a phone vault for you. Obsidian's **Set up Obsidian Sync** option is for Obsidian's own service.

**Already connected with another name?** Keep that vault and its connection. Use Obsidian's vault manager to rename that existing phone vault to the name shown on the PC. If that name is already taken, check which existing vault you want to use before renaming; do not overwrite it. Helenite does not rename the Obsidian folder for you. A matching name alone does not connect two vaults: the existing approved connection identifies the shared vault. There is no need to delete files, clear Helenite's settings or pair again just to fix a name.

## 4. Connect with the QR or a copied code

1. On the host, choose **Connect phone** and create a fresh connection code after external access is ready. Keep that screen open and check its expiry time.
2. On the phone, keep the local vault with the matching name open with Helenite enabled. Scan the PC's QR with the camera and allow it to open Obsidian.
3. If scanning or opening fails, use **Copy connection link** or copy the code on the PC, and transfer it privately to your own phone. In Obsidian open the command palette and run **Helenite: Open sync panel**. Choose **Paste received code**, or **Enter manually**, paste the full code/link and choose **Next**.
4. Review the destination vault and its name. If it contains files, Helenite asks whether to also sync them. Use an empty test vault unless you deliberately want those existing files included. Choose **Request connection to computer**.
5. Compare the four English words on the phone and PC. Approve the phone on the PC **only if all four match in order**. If an older version displays a long code, expand **Full fingerprint for older versions** on the other device and compare the complete codes. Keep Obsidian open on the phone until the initial transfer finishes.

Treat a connection link/code as private. Do not post it in a screenshot or support request. If it expires, create a fresh code on the host. If you see **Finish the open connection dialog first**, return to the existing dialog and complete or close it before opening another invitation; do not keep scanning or delete connection settings.

When a shared vault is first created with the latest plugin candidate, Helenite records its name. With the updated desktop server and plugins on both devices, subsequent approved connections also receive that name in encrypted form. Helenite displays it while each device retains its own local files. Obsidian's local vault name is managed separately, so changing a folder name does not automatically rename every device. Existing connections without a shared name continue working and keep their local labels; follow the matching-name guidance above without deleting or reconnecting them. An older server or plugin can still connect, but may not transfer the name.

## 5. Confirm the first sync

The initial connection transfers the vault's supported files. Later passes send changes and reuse encrypted chunks where possible; the whole vault is not downloaded on every edit.

With desktop 0.1.18 and plugin 0.1.13 on both devices, approve the QR request, then look for the newly paired phone under **My vault** on the PC. Keep the same vault open in Obsidian on both devices.

1. **Connection approved** means the PC accepted this device’s pairing request.
2. The **first note** is confirmed when the phone has saved a Markdown note from this PC. Attachments and other notes may still be transferring.
3. The **whole vault** is confirmed when the PC checks that both devices have confirmed the same set of syncable files. The row shows when the PC checked. Edits made on an offline phone become visible after it reconnects. If a change is held or a newer change still needs confirmation, this row shows a pending state. An empty or attachment-only vault can finish while the first-note row still waits.

Hidden files and `.obsidian` settings, themes and plugins are excluded. Update Helenite on the PC and both Obsidian plugins if an older version cannot report these confirmations. With the current public release you can also check both directions directly: keep both vaults open, create a disposable note on the PC, open it on the phone, add a line there and check that it returns to the PC.

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

In version 0.1.11 the list shows up to 50 entries, with incomplete work first. A missing entry does not by itself mean the copy was deleted. Keep hidden Helenite state and plugin settings intact, and contact **admin@egress.llc** or your test organizer.

With plugin 0.1.13, choose **Recovery copies for this note** in a Markdown file’s menu or command palette. The list shows the saved copies for that path by date, with incomplete writes first. For a deleted note, open the full recovery list and search its original file path. Use **Next page** for older copies. Choose **Preview** to read a small Markdown copy, then **Restore as a separate file**. When reviewing simultaneous edits, choose each changed section and select **Merge selected sections → Confirm and apply**. Full versions and manual editing remain available.

If a write was interrupted, first restore and inspect a separate copy. Use **Keep current file/state** only after checking the current content: it can accept a partial file or an absent file as the state to sync. Keep recovery copies until you are satisfied.

Sync and recovery copies are not an independent backup. Keep a separate, protected backup of your vault, including the private Helenite settings needed for recovery. Do not manually delete hidden Helenite state or share `.obsidian/plugins/helenite/data.json`; it contains connection keys. A lost encryption key cannot be recovered from an email login.

## Usage details and automatic connection recovery

**This describes the local candidate as of November 12, 2026. Production policy activation and public launch are separate.**

When a current subscription is verified on the first PC connection request, Helenite applies the management policy to that account automatically. Signing up or signing in does not grant paid access. Keep your existing account, PC, phone connections and usage history.

Open usage details on the account page to see the remaining percentages for **management requests** and **automatic connection renewal**. Requests have different processing costs, so these percentages are not a count of remaining requests. Details load only when opened or refreshed. The monthly accounting reset is not a promised synchronization recovery time.

- **Automatic recovery / retry shortly:** keep the same account and vault and wait for the displayed delay. Do not erase plugin settings or register a new PC to clear a wait. Local notes stay on your devices and transfers resume when the connection recovers. Timing depends on the server and network.
- **Management allowance reached:** ordinary management work may pause, while sign-in status, subscription management, account export, deletion and connection recovery have separate paths. Repeated attempts may require a short wait. Existing identity and billing requirements still apply to cancellation and deletion.
- **New PC registration capacity reached:** preserve your vault and connections and use the displayed support channel. Creating duplicate accounts or paying again does not resolve this state.

Account export is not a note backup. Reading and copying existing local notes does not require an active Helenite subscription.

## Account or host recovery

For **the same PC**, follow the buttons actually shown under its external connection status:

| What you see | What to do |
| --- | --- |
| **Recover PC registration** | Choose it and confirm **Recover registration**. If **Confirm account again** appears, complete that step first. Signing in alone does not restore access. |
| **Check this PC’s connection** with **Check PC registration** | Check the registration, then follow the updated status. Keep the saved connection information. |
| **Start new recovery** | The earlier recovery was canceled. Confirm a new recovery on this same PC. |

These recovery steps need the PC's saved credentials. If a button is absent or the state remains unclear, keep your files/settings and contact **admin@egress.llc** or your test organizer.

- **Lost or replaced PC:** when registration reports another PC, **Replace the previous PC** requires a recent email-code login and explicit confirmation. It transfers connection authority, not notes or encryption keys. You need a surviving vault copy and a paired device. Do not erase the surviving copies to start over.
- **Lost phone or exposed connection code:** on the host PC using managed external access, run Helenite and Obsidian with the current plugin, with that vault connected to the running host. Open **Connected devices**, choose **Disconnect** for the device or **Cancel invitation** for an unused invitation, and confirm. **Refresh** the list and check for **Disconnected**. **Connection blocked · Relay cleanup pending** means the device is blocked but cleanup remains; use **Retry cleanup**. Disconnection blocks the next sync; already received notes remain. It does not remotely erase files. If the controls are absent or the result cannot be confirmed, preserve files/settings and contact support.
- **Payment pending/needs review:** Keep the status shown in your account. If it persists, contact **admin@egress.llc** with the time and the message you saw. Repeating the payment could create another transaction.

Downloading and installing Helenite is free; synchronization requires a subscription or an explicitly offered trial. Plans are USD 3 per month or USD 24 per year. Existing local notes remain readable, copyable and exportable after expiry. Developer-only local testing is not a permanent free sync plan.

**Which emails will I receive?** When you request a six-digit sign-in code, **Helenite by Egress** sends it from `auth.helenite.net`. The card-free trial creates no charge or receipt. When you pay for a new subscription or a renewal, **Paddle** processes the payment and emails your receipt. Open **Manage subscription** in your [Helenite account](https://helenite.net/account?lang=en) to check your subscription, view past payments, and download PDF invoices.

**Ordinary cancellation.** Turn off renewal in **Manage subscription** on your account page. Your account shows when paid sync access ends. You can keep syncing until then and open your local notes afterwards.

**Full refund.** You can keep syncing while a refund request is under review if your paid access is still active. Once a full refund for the current paid period is approved, sync access for that period ends. Helenite requests that Paddle stop the next renewal if it is still active. Your account shows whether Paddle has confirmed the change. To check the latest status, open **Manage subscription**. Your local notes remain available.

Both plans include 10 GB of relayed data per account each UTC calendar month. That total includes uploads, downloads, each receiving device and any retransmission. Direct transfers use no relay bytes. The [service terms](https://helenite.net/terms?lang=en) explain how relay messages, events and connections are counted. Check your [Helenite account](https://helenite.net/account?lang=en) for current subscription availability.

## Save account data or delete an account

Open your [Helenite account](https://helenite.net/account?lang=en) in a browser to see the available data and deletion controls. Sandbox accounts and the desktop connection approval screen do not show these controls. If a control is unavailable, contact **admin@egress.llc**.

1. Keep a separate backup of your local vault. Under **Account data and deletion**, **Save my account data** downloads account information only. It does **not** back up notes or encryption keys.
2. To stop future renewals, use **Manage subscription**. Account deletion does not cancel a subscription. If cancellation is scheduled, use the remaining paid period and request deletion after the subscription actually ends; pending payments or billing review must also be resolved.
3. Choose **Verify my email again** and complete the email-code login. Within 10 minutes, choose **Delete account**, check the displayed email and choose **Confirm deletion**.
4. If deletion is in progress or the result cannot be confirmed, use **Check deletion status**; follow the displayed retry instruction for the same request. Only **Account deleted** confirms completion. If it remains pending, contact support.

Deletion ends account sign-in and external access. Local notes remain readable, copyable and exportable; billing, security and usage records may remain as described in the [privacy notice](https://helenite.net/privacy). Never send support your password, email code, connection link, encryption keys or vault backup.

## Updates and getting help

For help with Helenite or a privacy request, email **admin@egress.llc**.

In **Connection help → Helenite updates**, choose **Check for updates → Download update → Open installer**. Finish syncing first. The **You are using the latest version** message confirms that the check succeeded.

On Ubuntu with Helenite 0.1.13 or later, leave Helenite open and approve Ubuntu’s request to install the update. When Helenite confirms the new version was installed, quit and reopen the app. If installation fails or you cancel, choose **Open installer** to retry or **Show installer in folder** to locate the verified download. The recovery message also shows the file’s full location. Earlier versions use Ubuntu’s default package installer. If its window closes before you can approve the first upgrade, open Files, press Ctrl+L and enter `~/.local/share/app.helenite.sync/verified-updates` (or `$XDG_DATA_HOME/app.helenite.sync/verified-updates` if you use a custom data folder). Open the newest download folder and choose **Open With** on the Helenite `.deb` to select your package installer. [Download the Ubuntu x64 0.1.16 installer](https://downloads.helenite.net/releases/0.1.16/linux-x64/Helenite-0.1.16-linux-x64.deb)

If an older plugin bundled with the desktop app says sync is by invitation, open **Settings → Community plugins → Check for updates** in Obsidian on each device. Choose **Update** for Helenite. Your vault and connection settings stay in place. Check your [Helenite account](https://helenite.net/account?lang=en) for your sync access.

For an issue, record what you did, the device/OS, the Helenite desktop version, the Obsidian and Helenite plugin versions on each device, the time, and the exact visible message. On the desktop use **Connection help → View diagnostics → Copy diagnostics** and inspect the preview before sharing it privately with your test organizer. The report does not identify the running plugin version, so include it separately. Nothing is automatically uploaded. The report excludes notes, vault names/paths, account emails, URLs/IPs and connection secrets. It cannot prove that a phone received a note. Never send passwords, email codes, connection links or plugin `data.json`.

## Current limits

| Area | Current boundary |
| --- | --- |
| Plugin compatibility | Four-word comparison is available in Helenite **0.1.7+**. Obsidian **1.7.4** was used to verify installation and restart of 0.1.7. In **Settings → Community plugins**, check the current Helenite release and its minimum Obsidian version. |
| File size | Up to **64 MiB** per file once every approved device and the host support large files. Otherwise the **8 MiB** compatibility limit remains. Oversized files are retained locally and deferred, not silently uploaded. |
| Text merging | Automatic merging and manual review text are bounded to **128 KiB**. Overlapping edits may require your choice. |
| Storage | Each device needs room for its local notes, pending changes and recovery copies. Available device storage is not unlimited relay traffic. |
| Relay service | 10 GB per account and UTC calendar month. If a monthly limit is reached, use an available direct connection or wait until 00:00 UTC on the first of next month. No automatic overage charge. |
| Availability | Host awake/online with Helenite and Obsidian running; phone Obsidian in foreground. No USB requirement. |
| Desktop builds | Get the signed Mac and Ubuntu installers from the [Helenite website](https://helenite.net/?lang=en). Contact Egress for the unsigned Windows x64 test installer and its SHA-256. |

