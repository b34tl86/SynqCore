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

## Keep screens running unattended

For displays that should start playing on their own after a power cut, use a managed player:

- **Raspberry Pi:** run the kiosk installer in [`players/raspberry-pi`](../players/raspberry-pi/install-kiosk.sh). It opens your player URL full-screen at boot.
- **Android TV, Google TV, Fire TV:** see [Android TV runtime](../players/android-tv/README.md).
- More options are in [Player devices](../players/README.md).

## Screens cannot connect?

- Make sure the display and the SynqCore PC are on the same network.
- Check that Windows treats that network as **Private**. See [the FAQ](faq.md#my-screens-cannot-connect).
- Confirm SynqCore is running: the tray icon should be visible on the server.
