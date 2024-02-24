# Palguard v548
 Palworld Anticheat
<br>
Features:<br>
Various  additional admin commands.<br>
IP banning system.<br>
IP whitelisting for admin commands (so cheaters can't use them)<br>
Chat logging (currently only in console)<br>
Unreal Engine networking logging (currently only in console)<br>
Configurable cheating punishments<br>
PvP damage limiting (although I'd suggest not enabling PvP at all)<br>
Automatic cheating/exploiting prevention & punishment<br>
<br><br>
How to Install:<br>
Windows:<br>
1) Download & extract version.dll and palguard.dll file into your server Pal\Binaries\Win64 folder.<br>
2) Start your server once, you will be able to edit configuration stuff in palguard.json file afterwards.<br>
3) To apply changes, either restart your server or use /reloadcfg admin command.<br>
<br><br>
Linux (Wine/Proton):<br>
1) Install a PalGuard Proton/Wine server (don't ask me how to do this, I have no idea).<br>
2) Install UE4SS on your server.<br>
3) Download & extract latest Wine/Proton PalGuard file into your server Pal\Binaries\Win64 folder.<br>
4) Start your server once, you will be able to edit configuration stuff in palguard.json file afterwards.<br>
5) To apply changes, either restart your server or use /reloadcfg admin command. <br>
Important note: In-game chat has a limit of 40 characters. Keep that in mind, as some commands like giving a pal or item may only be usable via RCON<br>
(unless someone will make a mod to remove this limitation)<br>
<br><br>

Admin commands:

/reloadcfg - reloads palguard config.

/imcheater - flags you as a cheater and takes appropriate action. (for testing purposes)

/kick PlayerName - Kick player by name.

/kickid UID - Kick player by ID. (the one you can obtain by pressing on a player name in ESC menu while being an admin)

/ban PlayerName - Ban player by name.

/banid UID - Ban player by ID. (the one you can obtain by pressing on a player name in ESC menu while being an admin)

/ipban PlayerName - IP Ban player by name.

/ipbanid UID - IP Ban player by ID. (the one you can obtain by pressing on a player name in ESC menu while being an admin)

/ipban_ip IP - Ban IP address from joining the server.

/addadminip IP - Adds ip to admin whitelist

/setadmin UID - Temporarily grants/revokes admin from a player

/give UID/STEAMID64 ITEMID AMOUNT - Gives player an item (https://pwmodding.wiki/docs/game-data/item-table)

/give_exp UID/STEAMID64 AMOUNT - Gives player experience

/whitelist_add STEAMID64 - adds SteamID64 to whitelist.

/whitelist_remove STEAMID64 - removes SteamID64 from whitelist.

/whitelist_get - gets full list of whitelisted players

/givepal UID/STEAMID64 CharacterID Level - Gives player a Pal (if your party is full, it will go into your Pal storage)

/giveegg UID/STEAMID64 Egg_ItemID - Gives player an egg with a completely random Pal inside. Egg item type only affects hatch time, but not the Pal inside.

/jetragon - Gives you admin jetragon pal (it's fast)

/catwaifu - Gives you admin Cat Waifu that buffs your character stats. 
<br><br>

Config explanation:

adminIPs - IP addresses that are allowed to use admin commands.

useAdminWhitelist - enables/disables usage of admin IP whitelist system.

shouldWarnCheaters - warns cheaters in chat that they got caught.

shouldWarnCheatersReason - provides them a reason why they got caught.

shouldKickCheaters - kicks cheaters.

shouldBanCheaters - ban cheaters.

shouldIPBanCheaters - IP ban cheaters.

pvpMaxToPlayerDamage - max damage that can be done to players IF pvp is enabled (bEnablePlayerToPlayerDamage). If damage exceeds this number, it will be floored down to it.

pvpMaxToPalDamage - same as above, but against player owned pals.

pvpMaxBuildingDamage - same as above, but against buildings. Note: specifically this option is for damage before any damage mitigation.

isStealingAllowed - if set to true, disables anticheat ownership checks.

logChat - Log all chat messages.

logNetworking - Log almost everything that players are sending to server.

bannedIPs - List of banned IP addresses.

allowSpawningNPCItems - Allows certain items to be spawned by cheaters (and by normal players, when they talk to NPC).

allowAdminCheats - Allows those who have logged in with admin password to use cheats without being punished.

announceConnections - broadcast message when player joins/leaves server

announcePunishments - broadcast message when player gets kicked/banned by anticheat

isChineseCmd - sets console window code page to GBK936 (if you want Chinese characters support and using default windows console - set this to true)

bannedChatWords - allows you to get rid of pesky RMT adverts. Messages containing words from this array will be blocked.

chatBypassWait - allows you to get rid of 1 minute cooldown between sending chat messages.

logRCON - Logs RCON commands stuff

pveMaxToPalBanThreshold - Attempting to deal damage to Pal higher than this number will flag player as cheater.

useWhitelist - enables/disables SteamID64 whitelist. 


FAQ:
Q: I've accidentally banned myself/someone. How can I unban them?
A: If you've banned their IP, for the time being you would need to edit palguard.json file and either reload the config or restart the server. If you've banned their account, you would need to remove their steamID from Pal\Saved\SaveGames\banlist.txt and restart the server afterwards.

Q: I cannot login as an admin, it says that admin commands are whitelist protected.
A: Make sure you have added your IP to palguard.json like shown on the picture (https://i.imgur.com/izmTRJg.png). Alternatively, you can set useAdminWhitelist to false, but that is not recommended, since cheaters are known to have some kind of exploit to obtain admin password.

Q: How can I report crashes?
A: Send your \Pal\Saved\Crashes\*random numbers*\CrashContext.runtime-xml file + palguard version used + log from Pal\Binaries\Win64\logs folder 
