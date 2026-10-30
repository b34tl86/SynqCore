# Pairing screens

Every display shows SynqCore content through the player page, a web page served by your SynqCore PC.

## 1. Find your server address

Right-click the SynqCore tray icon. The menu shows **Pair screens at http://192.168.1.20:8787**, with your PC's own address. Displays use that address, never `localhost`.

## 2. Create the screen

In the dashboard, go to **Screens → Add Screen** and copy the 6-digit pairing code.

## 3. Open the player on the display

On the display's browser, open:

```text
http://YOUR-SERVER-ADDRESS:8787/player?code=ABC123
```

The screen pairs immediately and starts playing whatever you assign to it. The same code can be opened on several browsers or devices, and each one shows the same content.

## Video resolution

SynqCore makes smaller copies of every uploaded video. Each screen downloads only one size, chosen in **Screens → Edit screen → Video resolution**:

- **Auto** (default): matches the size the screen reports. A Full HD screen gets the 1080p copy.
- **720p**, **1080p**, or **4K**: always this size. A screen gets the next smaller copy when its size isn't available, for example a 4K setting on a 1080p video.
- **Original**: the file exactly as uploaded.

A screen switches to a new setting, or to a copy that has just finished, the next time it checks for updates.

## Keep screens running unattended

For displays that should start playing on their own after a power cut, use a managed player:

- **Raspberry Pi:** run the kiosk installer in [`players/raspberry-pi`](../players/raspberry-pi/install-kiosk.sh). It opens your player URL full-screen at boot.
- **Android TV, Google TV, Fire TV:** see [Android TV runtime](../players/android-tv/README.md).
- More options are in [Player devices](../players/README.md).

## Screens cannot connect?

- Make sure the display and the SynqCore PC are on the same network.
- Check that Windows treats that network as **Private**. See [the FAQ](faq.md#my-screens-cannot-connect).
- Confirm SynqCore is running: the tray icon should be visible on the server.
