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
🛠️ Features:<br>
Various additional admin commands.<br>
IP banning system.<br>
IP whitelisting for admin commands.<br>
Chat logging.<br>
Unreal Engine networking logging.<br>
Configurable cheating punishments.<br>
PvP damage limiting.<br>
Automatic cheating/exploiting prevention & punishment.<br>
<br>
🔒 FAQ:<br>
Q: How to unban someone?<br>
A: Edit palguard.json for IP bans, or remove their SteamID from Pal\Saved\SaveGames\banlist.txt for account bans.<br>
<br>
Q: Unable to login as admin?<br>
A: Ensure your IP is whitelisted in palguard.json. Alternatively, set useAdminWhitelist to false, though not recommended.<br>
<br>
Q: How to report crashes?<br>
A: Send CrashContext.runtime-xml file, PalGuard version, and log from Pal\Binaries\Win64\logs folder.<br>
<br>
📌 Admin Tips:<br>
Avoid joining or inviting guilds while using admin cheats.<br>
Admin whitelist is based on IP for security against cheaters.<br>
<br>
📋 Admin Commands: ⁠📑・commands-info<br>
<br>
⚙️ Config Explanation: ⁠📑・config-info<br>
!Admin Whitelist Example<br>
<br>
<br>
<br>
📑 Configuration Explanation:<br>
🔒 Security Settings:<br>
adminIPs: Allowed IP addresses for admin commands.<br>
useAdminWhitelist: Enable/disable admin IP whitelist.<br>
shouldWarnCheaters: Warn cheaters in chat.<br>
shouldWarnCheatersReason: Provide reason for cheater warnings.<br>
shouldKickCheaters: Kick cheaters.<br>
shouldBanCheaters: Ban cheaters.<br>
shouldIPBanCheaters: IP ban cheaters.<br>
bannedIPs: List of banned IP addresses.<br>
useWhitelist: Enable/disable SteamID64/IP whitelist.<br>
<br>
⚔️ Combat and Cheating Prevention:<br>
pvpMaxToPlayerDamage: Max player-to-player damage.<br>
pvpMaxToPalDamage: Max damage to player-owned pals.<br>
pvpMaxBuildingDamage: Max damage to buildings.<br>
isStealingAllowed: Allow stealing (anti-cheat ownership checks).<br>
pveMaxToPalBanThreshold: Damage threshold for flagging player as cheater.<br>
allowSpawningNPCItems: Allow spawning of certain items by cheaters.<br>
allowAdminCheats: Allow admin cheats without punishment.<br>
disableIllegalItemProtection: Disable protection against Debug/Robbery spheres.<br>
<br>
📝 Logging and Communication:<br>
logChat: Log all chat messages.<br>
logNetworking: Log player-server network communication.<br>
announceConnections: Broadcast message on player join/leave.<br>
announcePunishments: Broadcast message on player kick/ban.<br>
logRCON: Log RCON commands.<br>
<br>
🚫 Chat Filtering and Cooldowns:<br>
bannedChatWords: Words to block in chat.<br>
chatBypassWait: Cooldown between chat messages.<br>
<br>
🛡️ Server Protection Settings:<br>
whitelistMessage: Custom whitelist message.<br>
bannedMessage: Custom message for banned players.<br>
disableButchering: Disable butchering to prevent dupe exploits.<br>
<br>
🔧 Technical Settings:<br>
RCONbase64: Use base64 encoding in RCON.<br>
<br>
📋 Note:<br>
Ensure to edit palguard.json file to adjust these settings.<br>
<br>
<br>
<br>
📑 Admin Commands:<br>
🔄 Server Management:<br>
/reloadcfg: Reloads PalGuard config.<br>
/imcheater: Flags you as a cheater for testing.<br>
/getnearestbase: Get nearest guild base name.<br>
/gotonearestbase: Teleport to nearest base.<br>
/killnearestbase: Destroy nearest base.<br>
/removedroppedpals: Remove dropped Pals.<br>
<br>
👢 Player Management:<br>
/kick PlayerName: Kick player by name.<br>
/kickid UID: Kick player by ID.<br>
/ban PlayerName: Ban player by name.<br>
/banid UID: Ban player by ID.<br>
/ipban PlayerName: IP ban player by name.<br>
/ipbanid UID: IP ban player by ID.<br>
/ipban_ip IP: Ban IP address from joining.<br>
/unban_ip IP: Remove IP from ban list.<br>
/getip UID/STEAMID64: Get IP of online player.<br>
<br>
🔑 Admin Whitelist Management:<br>
/addadminip IP: Add IP to admin whitelist.<br>
/setadmin UID: Temporarily grant/revoke admin.<br>
<br>
💼 Item & Pal Management:<br>
/give UID/STEAMID64 ITEMID AMOUNT: Give player an item.<br>
/give_exp UID/STEAMID64 AMOUNT: Give player experience.<br>
/givepal UID/STEAMID64 CharacterID Level: Give player a Pal.<br>
/giveegg UID/STEAMID64 Egg_ItemID: Give player an egg with random Pal.<br>
/jetragon: Give admin jetragon pal.<br>
/catwaifu: Give admin Cat Waifu.<br>
<br>
📢 Communication:<br>
/pgbroadcast: PalWorld Broadcast.<br>
<br>
🔒 Admin Security:<br>
/adminlogout: Log out of admin mode.<br>
<br>
📝 Note:<br>
In-game chat has a 40 character limit.<br>
Some commands may require RCON due to character limit.<br>
