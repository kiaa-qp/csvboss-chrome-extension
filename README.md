CSVBOSS Nickname Manager

A Chrome extension that bulk applies Steam nicknames from a CSV,built to work with the CSVBOSS Discord bot.
---------------------------------------------------------
A Discord bot paired with a Chrome extension designed for Rust clan management. Lets you collect and manage your members' Steam accounts directly through Discord, export them for use in-game, and bulk apply Steam nicknames without doing it manually one by one.

Bot commands:

/setsteamcsv — Link your Steam account to your Discord profile
/getcsv — Export all linked members as a Steam64 ID CSV, filterable by role or server
/farmstats — Pull VitalRust farm & combat stats for any member, filter by server and wipe
/mysteam — Check your own currently linked Steam account
/stats — See overall registration stats for your server
/notlinked — List every member in a role who hasn't linked yet
/remindunlinked — Automatically DM all unlinked members in a role to register
/adminadd / /adminremove — Manually add or remove Steam links on behalf of members
/lookupsteam — Look up any member's linked Steam account and profile
Chrome extension:

Paste the CSV from /getcsv directly into the panel on your Steam friends page
Bulk apply Steam nicknames to all your members in one click
Add a clan tag prefix to every nickname — useful for turret and TC authorization in large clans
Strip all Steam nicknames at once when a wipe ends
Saves your last CSV between sessions so you don't have to paste it every time
