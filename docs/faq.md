# Frequently asked questions

## Where does SynqCore keep my data?

In `%LOCALAPPDATA%\SynqCore` for the Windows user who runs SynqCore. It contains the database (`data`), uploaded media (`uploads`), and logs (`logs`). The program itself is in `C:\Program Files\SynqCore`.

## Which port does SynqCore use?

Port **8787**, for both the dashboard and the player pages. If another program already uses it, SynqCore shows a message when it starts. Close that program and start SynqCore again.

## My screens cannot connect

Windows only opens port 8787 on networks it treats as **Private** or **Domain**. If your network is set to **Public**, screens cannot reach SynqCore. To change it:

1. Open **Settings → Network & internet**.
2. Select your connection (Wi-Fi or Ethernet) and open its **Properties**.
3. Under **Network profile type**, choose **Private network**.

Also check that the display uses the address from the tray menu (**Pair screens at …**), not `localhost`.

## Does SynqCore keep running when nobody is signed in?

SynqCore starts when a Windows user signs in, and keeps running while that user stays signed in, even with the screen locked. For an always-on signage server, set Windows to sign in automatically, or leave the user signed in and locked.

## Can several Windows users share the SynqCore PC?

They can sign in to it, but SynqCore should always run under one dedicated account. Each Windows account keeps its own SynqCore data, and only one copy of SynqCore can serve your screens at a time. If another person signs in to the server PC first, their SynqCore starts with an empty setup and your paired screens show the pairing page until the dedicated account runs SynqCore again.

For a signage server:

- Create one Windows account for signage, install SynqCore while signed in to it, and set Windows to sign in to that account automatically, so it is always the first account signed in after a restart.
- Other people can still sign in, for example with **Switch user**. While the signage account is signed in and SynqCore is running there, SynqCore in their session sees it and stays out of the way.

## How do I update SynqCore?

Download the newer installer from the [releases page](https://github.com/b34tl86/SynqCore/releases) and run it. Your data is kept.

## How do I back up SynqCore?

Quit SynqCore from the tray menu, copy the whole `%LOCALAPPDATA%\SynqCore` folder somewhere safe, then start SynqCore again. To restore, quit SynqCore and copy the folder back.

## Can I present PowerPoint and Word files?

Yes. SynqCore converts them using Microsoft Office or LibreOffice, whichever is installed on the SynqCore PC.

## Is my content sent to the cloud?

No. Media, schedules, and logs stay on your SynqCore PC. Screens only load content from it, except for online sources you add yourself, such as YouTube videos, web pages, or RSS feeds.
