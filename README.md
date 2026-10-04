# WhatsApp Web Multi Account

Unofficial portable Windows app for using multiple WhatsApp Web accounts in one window. All accounts stay active at once, with privacy blur, PIN lock.

## Download

Go to **[Releases](../../releases/latest)** and pick one:

- `WAWebMultiAcc-<version>-portable.exe`: a single file. Run it from any folder or a USB drive.
- `WAWebMultiAcc-<version>-x64.zip`: extract it, then run `WAWebMultiAcc.exe`. Starts faster than the portable version.

Then scan the QR code with your phone (WhatsApp → Linked devices → Link a device). Use **+** in the sidebar to add more accounts.

Windows SmartScreen may show a warning the first time. Click **More info → Run anyway**.

## Features

- Every account stays connected and receives notifications, even while the window is hidden in the tray.
- Unread badges per account, with the total shown in the taskbar.
- Privacy: blur messages, chat previews, media, names, photos, or the text being typed (`Ctrl+Shift+B`). Notification content can be hidden.
- PIN lock, with auto-lock when idle or when Windows locks.
- Memory saver that reloads background accounts without signing out.
- Automatic updates: the app tells you when a new version is available and installs it only with your consent. The previous version is kept and can be restored.

## Verifying your download

- Each release includes `SHA256SUMS.txt`. To check a file, run this in PowerShell:
  ```
  Get-FileHash .\WAWebMultiAcc-<version>-portable.exe
  ```
  The result must match that file's line in `SHA256SUMS.txt`.
- Automatic updates install only files digitally signed by the developer. The app rejects anything that was altered.
- Download only from this repository's Releases page.

## Privacy

The app connects only to WhatsApp Web and, for updates, to the files in this repository (`update/latest.json` and `update/blur-rules.json`). It does not send account data, messages, or usage information anywhere.

The `Data` folder next to the app holds your login sessions. Anyone who copies it may be able to open your accounts:

- Protect it with BitLocker, or BitLocker To Go on a USB drive.
- If you think it was copied, open WhatsApp on your phone → **Linked devices** and log out any device you do not recognize.

## What is in this repository

- `update/latest.json`: information about the latest version (signed).
- `update/blur-rules.json`: the latest blur rules (signed and encrypted).

The source code is not published.

## License

Free to use, for personal and business purposes, under the [WhatsApp Web Multi Account Freeware License](LICENSE.txt). The app may not be modified, sold, or redistributed. To share it, share a link to the Releases page.

---

This is an independent app. It is not affiliated with, endorsed by, or sponsored by WhatsApp LLC or Meta Platforms, Inc.
