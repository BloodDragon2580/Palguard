# Palguard v713
 Palworld Anticheat
<br>
ℹ️ Server Administration Information<br>
🖥️ Platform Compatibility:<br>
Windows: Works only on Dedicated Server.<br>
Linux (Wine/Proton): Requires additional setup.<br>
<br>
🔧 Installation:<br>
Windows:<br>
Download & extract version.dll and palguard.dll into your server Pal\Binaries\Win64 folder.<br>
Start your server once to edit configuration in palguard.json. Apply changes with /reloadcfg admin command.<br>
<br>
Linux (Wine/Proton):<br>
Install a PalGuard Proton/Wine server.<br>
Install UE4SS on your server.<br>
Download & extract latest Wine/Proton PalGuard file into your server Pal\Binaries\Win64 folder.<br>
Start your server once, then edit configuration in palguard.json. Apply changes with /reloadcfg admin command.<br>
<br>
🛠️ Features:
Various additional admin commands.
IP banning system.
IP whitelisting for admin commands.
Chat logging.
Unreal Engine networking logging.
Configurable cheating punishments.
PvP damage limiting.
Automatic cheating/exploiting prevention & punishment.

🔒 FAQ:
Q: How to unban someone?
A: Edit palguard.json for IP bans, or remove their SteamID from Pal\Saved\SaveGames\banlist.txt for account bans.

Q: Unable to login as admin?
A: Ensure your IP is whitelisted in palguard.json. Alternatively, set useAdminWhitelist to false, though not recommended.

Q: How to report crashes?
A: Send CrashContext.runtime-xml file, PalGuard version, and log from Pal\Binaries\Win64\logs folder.

📌 Admin Tips:
Avoid joining or inviting guilds while using admin cheats.
Admin whitelist is based on IP for security against cheaters.

📋 Admin Commands: ⁠📑・commands-info

⚙️ Config Explanation: ⁠📑・config-info
!Admin Whitelist Example



📑 Configuration Explanation:
🔒 Security Settings:
adminIPs: Allowed IP addresses for admin commands.
useAdminWhitelist: Enable/disable admin IP whitelist.
shouldWarnCheaters: Warn cheaters in chat.
shouldWarnCheatersReason: Provide reason for cheater warnings.
shouldKickCheaters: Kick cheaters.
shouldBanCheaters: Ban cheaters.
shouldIPBanCheaters: IP ban cheaters.
bannedIPs: List of banned IP addresses.
useWhitelist: Enable/disable SteamID64/IP whitelist.

⚔️ Combat and Cheating Prevention:
pvpMaxToPlayerDamage: Max player-to-player damage.
pvpMaxToPalDamage: Max damage to player-owned pals.
pvpMaxBuildingDamage: Max damage to buildings.
isStealingAllowed: Allow stealing (anti-cheat ownership checks).
pveMaxToPalBanThreshold: Damage threshold for flagging player as cheater.
allowSpawningNPCItems: Allow spawning of certain items by cheaters.
allowAdminCheats: Allow admin cheats without punishment.
disableIllegalItemProtection: Disable protection against Debug/Robbery spheres.

📝 Logging and Communication:
logChat: Log all chat messages.
logNetworking: Log player-server network communication.
announceConnections: Broadcast message on player join/leave.
announcePunishments: Broadcast message on player kick/ban.
logRCON: Log RCON commands.

🚫 Chat Filtering and Cooldowns:
bannedChatWords: Words to block in chat.
chatBypassWait: Cooldown between chat messages.

🛡️ Server Protection Settings:
whitelistMessage: Custom whitelist message.
bannedMessage: Custom message for banned players.
disableButchering: Disable butchering to prevent dupe exploits.

🔧 Technical Settings:
RCONbase64: Use base64 encoding in RCON.

📋 Note:
Ensure to edit palguard.json file to adjust these settings.



📑 Admin Commands:
🔄 Server Management:
/reloadcfg: Reloads PalGuard config.
/imcheater: Flags you as a cheater for testing.
/getnearestbase: Get nearest guild base name.
/gotonearestbase: Teleport to nearest base.
/killnearestbase: Destroy nearest base.
/removedroppedpals: Remove dropped Pals.

👢 Player Management:
/kick PlayerName: Kick player by name.
/kickid UID: Kick player by ID.
/ban PlayerName: Ban player by name.
/banid UID: Ban player by ID.
/ipban PlayerName: IP ban player by name.
/ipbanid UID: IP ban player by ID.
/ipban_ip IP: Ban IP address from joining.
/unban_ip IP: Remove IP from ban list.
/getip UID/STEAMID64: Get IP of online player.

🔑 Admin Whitelist Management:
/addadminip IP: Add IP to admin whitelist.
/setadmin UID: Temporarily grant/revoke admin.

💼 Item & Pal Management:
/give UID/STEAMID64 ITEMID AMOUNT: Give player an item.
/give_exp UID/STEAMID64 AMOUNT: Give player experience.
/givepal UID/STEAMID64 CharacterID Level: Give player a Pal.
/giveegg UID/STEAMID64 Egg_ItemID: Give player an egg with random Pal.
/jetragon: Give admin jetragon pal.
/catwaifu: Give admin Cat Waifu.

📢 Communication:
/pgbroadcast: PalWorld Broadcast.

🔒 Admin Security:
/adminlogout: Log out of admin mode.

📝 Note:
In-game chat has a 40 character limit.
Some commands may require RCON due to character limit.
