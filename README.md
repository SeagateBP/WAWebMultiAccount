# WhatsApp Web Multi Account

Unofficial portable Windows app for using multiple WhatsApp Web accounts in one window. All accounts stay active at once, with privacy blur, PIN lock.

## Download

Go to **[Releases](../../releases/latest)** and download `WAWebMultiAcc-<version>-x64.zip`. Extract it to a folder of its own (a USB drive works too), then run `WAWebMultiAcc.exe`.

Then scan the QR code with your phone (WhatsApp → Linked devices → Link a device). Use **+** in the sidebar to add more accounts.

Updates install themselves from version 1.0.2 on. Coming from 1.0.0 or 1.0.1 (zip or portable .exe)? Extract the new zip into the old app folder once; the `Data` folder with your accounts is kept.

Windows SmartScreen may show a warning the first time. Click **More info → Run anyway**.

## Features

- Every account stays connected and receives notifications, even while the window is hidden in the tray.
- Unread badges per account, with the total shown in the taskbar.
- Privacy: choose exactly what to blur in the chat list, the chat header, the messages (text, photos, videos, documents, group sender names and photos), the text being typed, and the contact info panel (`Ctrl+Shift+B`). Notification content can be hidden.
- PIN lock, with auto-lock when idle or when Windows locks.
- Memory saver that reloads background accounts without signing out.
- Automatic updates: the app tells you when a new version is available and installs it only with your consent. The previous version is kept and can be restored.

## Verifying your download

- Each release includes `SHA256SUMS.txt`. To check a file, run this in PowerShell:
  ```
  Get-FileHash .\WAWebMultiAcc-<version>-x64.zip
  ```
  The result must match that file's line in `SHA256SUMS.txt`.
- Automatic updates install only files digitally signed by the developer. The app rejects anything that was altered.
- Download only from this repository's Releases page.

## Privacy

The app connects only to WhatsApp Web and, for updates, to the files in this repository (`update/latest.json` and `update/privacy-rules.json`). It does not send account data, messages, or usage information anywhere.

The `Data` folder next to the app holds your login sessions. Anyone who copies it may be able to open your accounts:

- Protect it with BitLocker, or BitLocker To Go on a USB drive.
- If you think it was copied, open WhatsApp on your phone → **Linked devices** and log out any device you do not recognize.

## What is in this repository

- `update/latest.json`: information about the latest version (signed).
- `update/privacy-rules.json`: the latest privacy (blur) rules for version 1.0.2 and later (signed and encrypted).
- `update/blur-rules.json`: the same for versions 1.0.0–1.0.1.

The source code is not published.

## License

Free to use, for personal and business purposes, under the [WhatsApp Web Multi Account Freeware License](LICENSE.txt). The app may not be modified, sold, or redistributed. To share it, share a link to the Releases page.

---

This is an independent app. It is not affiliated with, endorsed by, or sponsored by WhatsApp LLC or Meta Platforms, Inc.
