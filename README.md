# CSVBOSS

A Discord bot and Chrome extension for managing Steam accounts in Rust clans. Collect your members' Steam IDs through Discord, export them as a CSV, and bulk apply Steam nicknames without doing it one by one.

---

## Bot Commands

| Command | Description |
|---|---|
| `/setsteamcsv` | Link your Steam account to your Discord profile |
| `/mysteam` | View your currently linked Steam account |
| `/getcsv` | Export linked members as a Steam64 CSV, filterable by role or server |
| `/farmstats` | Check VitalRust farm & combat stats for any member, by server and wipe |
| `/stats` | See registration stats for your server |
| `/notlinked` | List members in a role who haven't linked yet |
| `/remindunlinked` | DM all unlinked members in a role to register |
| `/lookupsteam` | Look up any member's linked Steam account |
| `/adminadd` | Manually add a Steam link for a member |
| `/adminremove` | Remove a member's linked Steam account |

---

## Chrome Extension

- Paste the CSV from `/getcsv` into the panel on your Steam friends page
- Bulk apply Steam nicknames to all members in one click
- Add a clan tag prefix to every nickname (useful for TC and turret auth)
- Remove all Steam nicknames at once when a wipe ends
- Saves your CSV between sessions

**Install:**
1. Download `extension.zip` and extract it
2. Go to `chrome://extensions` and enable Developer Mode
3. Click **Load unpacked** and select the folder
4. Go to `https://steamcommunity.com/my/friends` — the panel will appear

**Use:**
1. Have members run `/setsteamcsv` in Discord
2. Run `/getcsv` and copy the output
3. Paste into the panel, add a prefix if needed, hit Apply

Nicknames take ~1.5 seconds each due to Steam rate limits. 27 users takes around 40 seconds.

---

