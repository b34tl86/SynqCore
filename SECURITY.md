# Security

## Reporting a vulnerability

Please report security issues privately to **security@techtrust.ae** rather than opening a public issue. Include the SynqCore version (shown in the dashboard), what you found, and how to reproduce it. We will acknowledge your report and keep you updated on the fix.

## Keeping your installation secure

- Change the `admin` password right after your first sign-in.
- Turn on multi-factor authentication for every admin account.
- Keep SynqCore on your local network. Do not forward port 8787 from your router to the internet. If you need remote access, use a VPN or a reverse proxy with HTTPS.
- Keep Windows updated on the SynqCore server and back up `%LOCALAPPDATA%\SynqCore` regularly (see the [FAQ](docs/faq.md#how-do-i-back-up-synqcore)).
