# Changelog

## v1.1.1 — 2026-10-30

### Sign-in

- The sign-in screen now explains why sign-in failed or why you were signed out: a wrong password (with hints about Caps Lock and old saved passwords), a missing or wrong MFA code, a browser that did not keep the sign-in cookie, or a session that expired, ended, or timed out after 10 minutes without activity.
- The username stays filled in after a wrong password.
- New installations start with username `admin` and password `admin`. Change the password after your first sign-in. Existing installations keep their current password.

### Third-party software

- The installation folder now includes the license text of every library built into the bundled FFmpeg, in `ffmpeg\licenses`. FFmpeg in SynqCore is distributed under the GPL version 3, because one of those libraries (FFTW) is GPL-licensed. SynqCore runs FFmpeg as a separate program.

## v1.1.0 — 2026-10-29

### Automatic video optimization

- Every uploaded video gets smaller H.264 copies in 720p and 1080p, plus 4K when the upload is 4K. Videos are never scaled up, and a copy is kept only when it is at least 20% smaller than the original.
- Compression uses the PC's graphics card (NVIDIA, Intel, or AMD) when available, and Windows' built-in encoder otherwise.
- Videos can be scheduled as soon as they are uploaded. Screens play the original until their copy is ready, then switch on their next update.
- Videos uploaded before this release are compressed automatically in the background. Originals are always kept.
- The media library shows each video's status, and **Settings → Video compression** shows the encoder, the queue, the disk used by copies, and an on/off switch.

### Screens

- New **Video resolution** setting for each screen: Auto, 720p, 1080p, 4K, or Original. Auto matches the size the screen reports, so a small player never downloads a 4K file.
- Players now store each video once instead of twice, and remove older versions of a video when a smaller copy replaces it.

### Third-party software

- SynqCore now includes FFmpeg. See `THIRD-PARTY-NOTICES.txt` in the installation folder for its license.

## v1.0.0 — 2026-10-28

The first public release of SynqCore.

### Windows installer

- Installs for all users to `C:\Program Files\SynqCore` and adds Start Menu and desktop shortcuts.
- Starts SynqCore in the background when Windows signs in. A tray icon opens the dashboard, shows the address screens pair with, and quits SynqCore.
- Opens port 8787 in Windows Firewall for Private and Domain networks so screens can connect.
- Upgrades a previous per-user installation automatically. Your data is kept.
- Uninstalling removes the program and its firewall rule and keeps your media, schedules, and settings.

### Platform

- Screen pairing with 6-digit codes, live connection status, and groups.
- Media library for images, video, audio, PDF, Office files, YouTube, IPTV/HLS streams, web pages, RSS, text slides, and countdowns.
- Multi-zone layouts with 8 presets and up to 4 zones per screen.
- Time-based scheduling with priorities and default playlists.
- Emergency alerts and live tickers, targeted to screens, groups, or everything.
- Admin, Manager, and Viewer roles with optional multi-factor authentication.
- Seven themes, custom branding, proof-of-play logging, live screen sharing, and network discovery.
