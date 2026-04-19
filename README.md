CSVBOSS Nickname Manager

A Chrome extension that bulk applies Steam nicknames from a CSV,built to work with the CSVBOSS Discord bot.
---------------------------------------------------------
# CSVBOSS — Discord Bot & Steam Nickname Manager

A Discord bot paired with a Chrome extension designed for Rust clan management. Lets you collect and manage your members' Steam accounts directly through Discord, export them for use in-game, and bulk apply Steam nicknames without doing it manually one by one.

---

## Bot Commands

| Command | Description |
|---|---|
| `/setsteamcsv` | Link your Steam account to your Discord profile |
| `/mysteam` | Check your own currently linked Steam account |
| `/getcsv` | Export all linked members as a Steam64 ID CSV, filterable by role or server |
| `/farmstats` | Pull VitalRust farm & combat stats for any member, filter by server and wipe |
| `/stats` | See overall registration stats for your server |
| `/notlinked` | List every member in a role who hasn't linked yet |
| `/remindunlinked` | Automatically DM all unlinked members in a role to register |
| `/lookupsteam` | Look up any member's linked Steam account and profile |
| `/adminadd` | Manually add a Steam link on behalf of a member |
| `/adminremove` | Remove a member's linked Steam account |

---

## Chrome Extension

- Paste the CSV from `/getcsv` directly into the panel on your Steam friends page
- Bulk apply Steam nicknames to all your members in one click
- Add a clan tag prefix to every nickname — useful for turret and TC authorization in large clans
- Strip all Steam nicknames at once when a wipe ends
- Saves your last CSV between sessions so you don't have to paste it every time

### How to install

1. Download `extension.zip` and extract it
2. Open Chrome and go to `chrome://extensions`
3. Enable **Developer Mode** in the top right
4. Click **Load unpacked** and select the extracted folder
5. Go to `https://steamcommunity.com/my/friends` and the panel will appear

### How to use

1. Have your members run `/setsteamcsv` in your Discord server
2. Run `/getcsv` to get the CSV output
3. Paste it into the panel, add a prefix if needed, and click **Apply**

> **Note:** Nicknames take around 1.5 seconds each to apply due to Steam rate limits. For 27 users that's roughly 40 seconds.

---

## ⚙️ Setup

### 1. Install dependencies
```bash
npm install
```

### 2. Create a Discord bot
1. Go to [discord.com/developers/applications](https://discord.com/developers/applications)
2. Create a new application → Bot tab → reset token to copy it
3. Under **OAuth2 → URL Generator**, select:
   - Scopes: `bot`, `applications.commands`
   - Bot permissions: `Send Messages`, `Attach Files`, `Manage Members`
4. Use the generated URL to invite the bot to your server

### 3. Set environment variables

Edit `restartbot.bat` with your values:
```bat
set DISCORD_TOKEN=your_bot_token
set CLIENT_ID=your_application_client_id
set DATABASE_URL=your_postgres_connection_string
node bot.js
```

### 4. Run the bot
```bat
restartbot.bat
```

---

## Database

Steam accounts are stored in a PostgreSQL database (tested with [Supabase](https://supabase.com)).  
Run the following in your SQL editor to create the required table:

```sql
CREATE TABLE steam_data (
  discord_id TEXT PRIMARY KEY,
  discord_name TEXT,
  steam_id TEXT,
  steam_name TEXT,
  steam_avatar TEXT,
  linked_at TEXT
);

ALTER TABLE steam_data ADD CONSTRAINT steam_data_discord_id_key UNIQUE (discord_id);
```
