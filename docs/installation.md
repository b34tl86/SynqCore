# Installing SynqCore

## Download

Download `SynqCore-Setup-v1.0.0.exe` from the [latest release](https://github.com/b34tl86/SynqCore/releases/latest). Each release also lists a `SHA256SUMS.txt` file. To confirm your download is intact, compare its hash with the one in that file:

```powershell
Get-FileHash .\SynqCore-Setup-v1.0.0.exe -Algorithm SHA256
```

## Windows SmartScreen

The installer is not yet signed with a commercial code-signing certificate, so Windows may show **"Windows protected your PC"**. Choose **More info**, check that the app name is `SynqCore-Setup-v1.0.0.exe`, then choose **Run anyway**.

## Install

1. Run the installer and approve the administrator prompt. The program is installed for every user of the PC, but your media, screens, and settings belong to the Windows account that runs SynqCore. Install and run it from the account that will operate your signage. See [one account per server](faq.md#can-several-windows-users-share-the-synqcore-pc).
2. Accept the Terms and Conditions.
3. Choose your options. Both are on by default:
   - **Create a desktop shortcut**
   - **Start SynqCore when Windows signs in.** Recommended for a signage server, so screens keep working after a restart.
4. Finish. SynqCore starts and opens the dashboard at `http://localhost:8787`.

The installer also adds a Windows Firewall rule so screens on your network can reach SynqCore on port 8787. See [network profiles](faq.md#my-screens-cannot-connect) if screens cannot connect.

## First sign-in

Sign in with username `admin`. On the first start, SynqCore creates a random password and saves it in:

```
%LOCALAPPDATA%\SynqCore\data\admin-bootstrap.txt
```

Paste that path into File Explorer's address bar to open the folder. Sign in, then change the password from the account menu and delete `admin-bootstrap.txt`.

## The tray icon

SynqCore runs in the background with an icon in the notification area (next to the clock):

- **Open dashboard** opens SynqCore in your browser. Double-clicking the icon does the same.
- **Pair screens at http://…:8787** shows the address your displays use.
- **Quit SynqCore** stops the server. Screens show their last content until SynqCore starts again.

## Updating

Download the newer installer and run it. It replaces the program and keeps all your data.

## Uninstalling

Open **Settings → Apps → Installed apps**, find **SynqCore**, and choose **Uninstall**. This removes the program, shortcuts, and firewall rule. Your media, schedules, and settings stay in `%LOCALAPPDATA%\SynqCore` in case you reinstall. Delete that folder to remove them too.
