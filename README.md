# CSVBOSS Chrome Extension

A Chrome extension for bulk managing Steam nicknames and friends — built for Rust clan Electricians.

---

## Features

**Nickname Manager**
Paste a CSV of Steam IDs and names, optionally add a clan tag prefix, and apply all nicknames in one click. Progress bar and per-entry log included.

**Remove All Nicknames**
Fetches your full friends list and clears every nickname at once — useful at the end of a wipe.

**Language Filter**
Filter CSV entries by language column before applying. Supports `ru`, `en`, and `cn` — useful when you only want to nickname a specific region's players.

**Friend Manager**
Use the same CSV to send bulk friend requests or unfriend players in bulk.

---

## CSV Format

```
steamid64,nickname
76561198000000001,PlayerOne,en
76561198000000002,PlayerTwo,ru
76561198000000003,PlayerThree
```

- `steamid64` — 17-digit Steam ID (required)
- `nickname` — the name to set (required)
- `language` — `ru`, `en`, or `cn` (optional, used for language filter)

---

## Installation

1. Go to the [Releases](https://github.com/kiaa-qp/csvboss-chrome-extension/releases) page and download the latest zip, or clone the repo
2. Open Chrome and go to `chrome://extensions`
3. Enable **Developer Mode** (toggle in the top right)
4. Click **Load unpacked** and select the `extension` folder (unzip the zipped folder you downloaded first)
5. Navigate to `https://steamcommunity.com/my/friends` — the panel will appear automatically

> The extension only works on `steamcommunity.com/*/friends*` pages and requires you to be logged into Steam in the same browser.

---

## Notes

- Nicknames are applied at ~1.5 seconds each due to Steam rate limits
- Your CSV and prefix are saved between sessions automatically
- The panel is draggable — click the header and drag it anywhere on the page
- **Error code 8** — already friends or request already pending
- **Error code 84** — their profile restricts incoming friend requests
