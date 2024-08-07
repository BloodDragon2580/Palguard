# PalGuard v895
 Palworld Anticheat
<br>
ALLGEMEIN<br>
ℹ️ Informationen zur Serververwaltung<br>
🖥️ Plattformkompatibilität:<br>
Windows: Funktioniert nur auf dedizierten Servern.<br>
Linux (Wine/Proton): Erfordert zusätzliches Setup.<br>
<br>
🔧 Installation:<br>
Windows:<br>
Lade die version.dll und palguard.dll herunter und extrahiere sie in den Pal\Binaries\Win64-Ordner deines Servers.<br>
Starte den Server einmal, um die Konfiguration in palguard.json zu bearbeiten. Übernehmen die Änderungen mit dem Admin-Befehl /reloadcfg.<br>
<br>
Linux (Wine/Proton):<br>
Installiere einen PalGuard Proton/Wine-Server.<br>
Installiere UE4SS auf dem Server.<br>
Laden die neueste Wine/Proton PalGuard-Datei herunter und extrahiere sie in den Pal\Binaries\Win64-Ordner deines Servers.<br>
Starten den Server einmal und bearbeite dann die Konfiguration in palguard.json. Übernehmen die Änderungen mit dem Admin-Befehl /reloadcfg.<br>
<br>
🛠️ Funktionen:<br>
Verschiedene zusätzliche Admin-Befehle.<br>
IP-Verbotssystem.<br>
IP-Whitelisting für Admin-Befehle.<br>
Chat-Protokollierung.<br>
Netzwerkprotokollierung der Unreal Engine.<br>
Konfigurierbare Strafen für Betrug.<br>
PvP-Schadensbegrenzung.<br>
Automatische Betrugs-/Ausbeutungsprävention und Bestrafung.<br>
<br>
🔒FAQ:<br>
F: Wie kann ich die Sperrung einer Person aufheben?<br>
A: Bearbeiten die palguard.json für IP-Sperren oder entfernen die SteamID aus Pal\Saved\SaveGames\banlist.txt für Kontosperren.<br>
<br>
F: Kann ich mich nicht als Administrator anmelden?<br>
A: Stelle sicher, dass deine IP in palguard.json auf der Whitelist steht. Alternativ kannst du useAdminWhitelist auf „false“ setzen, <br>
dies wird jedoch nicht empfohlen.<br>
<br>
F: Wie melde ich Abstürze?<br>
A: Senden die Datei CrashContext.runtime-xml, die PalGuard-Version und das Protokoll aus dem Ordner Pal\Binaries\Win64\logs.<br>
<br>
📌 Admin-Tipps:<br>
Vermeide es, Gilden beizutreten oder Gilden einzuladen, während du Admin-Cheats verwendest.<br>
Die Admin-Whitelist basiert auf IP zum Schutz vor Betrügern.<br>
<br>
📋 Admin-Befehle: ⁠📑・Befehlsinfo<br>
<br>
⚙️ Konfigurationserklärung: ⁠📑・config-info<br>
Beispiel für eine !Admin-Whitelist<br>
<br>
<br>
<br>
KONFIG<br>
📑 Konfigurationserklärung:<br>
🔒 Sicherheitseinstellungen:<br>
adminIPs: Zulässige IP-Adressen für Admin-Befehle.<br>
useAdminWhitelist: Administrator-IP-Whitelist aktivieren/deaktivieren.<br>
ShouldWarnCheaters: Betrüger im Chat warnen.<br>
ShouldWarnCheatersReason: Geben Sie den Grund für Cheater-Warnungen an.<br>
ShouldKickCheaters: Cheater treten.<br>
ShouldBanCheaters: Betrüger verbieten.<br>
ShouldIPBanCheaters: IP-Ban-Cheater.<br>
bannedIPs: Liste der gesperrten IP-Adressen.<br>
useWhitelist: SteamID64/IP-Whitelist aktivieren/deaktivieren.<br>
<br>
⚔️ Kampf- und Betrugsprävention:<br>
pvpMaxToPlayerDamage: Maximaler Spieler-zu-Spieler-Schaden.<br>
pvpMaxToPalDamage: Maximaler Schaden für spielereigene Freunde.<br>
pvpMaxBuildingDamage: Maximaler Schaden an Gebäuden.<br>
isStealingAllowed: Stehlen zulassen (Anti-Cheat-Besitzprüfungen).<br>
pveMaxToPalBanThreshold: Schadensschwelle für die Kennzeichnung eines Spielers als Betrüger.<br>
AllowSpawningNPCItems: Erlaubt das Spawnen bestimmter Gegenstände durch Betrüger.<br>
AllowAdminCheats: Admin-Cheats ohne Bestrafung zulassen.<br>
disableIllegalItemProtection: Deaktiviert den Schutz vor Debug-/Robbery-Sphären.<br>
<br>
📝 Protokollierung und Kommunikation:<br>
logChat: Alle Chat-Nachrichten protokollieren.<br>
logNetworking: Spieler-Server-Netzwerkkommunikation protokollieren.<br>
AnnounceConnections: Broadcast-Nachricht beim Beitritt/Verlassen des Spielers.<br>
ankündigenStrafen: Broadcast-Nachricht zum Kicken/Bannen eines Spielers.<br>
logRCON: RCON-Befehle protokollieren.<br>
<br>
🚫 Chat-Filterung und Abklingzeiten:<br>
bannedChatWords: Wörter, die im Chat blockiert werden sollen.<br>
chatBypassWait: Abklingzeit zwischen Chat-Nachrichten.<br>
<br>
🛡️ Serverschutzeinstellungen:<br>
whitelistMessage: Benutzerdefinierte Whitelist-Nachricht.<br>
bannedMessage: Benutzerdefinierte Nachricht für gesperrte Spieler.<br>
disableButchering: Deaktivieren Sie das Butchering, um betrügerische Exploits zu verhindern.<br>
<br>
🔧 Technische Einstellungen:<br>
RCONbase64: Base64-Kodierung in RCON verwenden.<br>
<br>
📋 Hinweis:<br>
Stellen Sie sicher, dass Sie die Datei palguard.json bearbeiten, um diese Einstellungen anzupassen.<br>
<br>
<br>
<br>
BEFEHL<br>
📑 Admin-Befehle:<br>
🔄 Serververwaltung:<br>
/reloadcfg: Lädt die PalGuard-Konfiguration neu.<br>
/imcheater: Markiert Sie zum Testen als Betrüger.<br>
/getnearestbase: Den Namen der nächstgelegenen Gildenbasis abrufen.<br>
/gotonearestbase: Zur nächsten Basis teleportieren.<br>
/killnearestbase: Zerstöre die nächstgelegene Basis.<br>
/removedroppedpals: Gelöschte Pals entfernen.<br>
<br>
👢 Spielerverwaltung:<br>
/kick PlayerName: Spieler nach Namen kicken.<br>
/kickid UID: Spieler nach ID kicken.<br>
/ban PlayerName: Spieler namentlich sperren.<br>
/banid UID: Spieler anhand seiner ID sperren.<br>
/ipban PlayerName: IP-Spieler namentlich sperren.<br>
/ipbanid UID: IP-Spieler nach ID sperren.<br>
/ipban_ip IP: IP-Adresse vom Beitritt verbieten.<br>
/unban_ip IP: IP aus der Sperrliste entfernen.<br>
/getip UID/STEAMID64: IP des Online-Players abrufen.<br>
<br>
🔑 Admin-Whitelist-Verwaltung:<br>
/addadminip IP: IP zur Admin-Whitelist hinzufügen.<br>
/setadmin UID: Administrator vorübergehend gewähren/entziehen.<br>
<br>
💼 Artikel- und Freundesverwaltung:<br>
/give UID/STEAMID64 ITEMID AMOUNT: Gib dem Spieler einen Gegenstand.<br>
/give_exp UID/STEAMID64 AMOUNT: Spielererfahrung geben.<br>
/givepal UID/STEAMID64 Charakter-ID-Level: Gib dem Spieler einen Kumpel.<br>
/giveegg UID/STEAMID64 Egg_ItemID: Gib dem Spieler ein Ei mit einem zufälligen Kumpel.<br>
/jetragon: Gib Admin Jetragon Kumpel.<br>
/catwaifu: Gib Admin Cat Waifu.<br>
<br>
📢 Kommunikation:<br>
/pgbroadcast: PalWorld Broadcast.<br>
<br>
🔒 Admin-Sicherheit:<br>
/adminlogout: Aus dem Admin-Modus abmelden.<br>
<br>
📝 Hinweis:<br><br>
Der Chat im Spiel ist auf 40 Zeichen begrenzt.
Für einige Befehle ist aufgrund der Zeichenbeschränkung möglicherweise RCON erforderlich.<br>
