# Support

Dieses Repository enthält die Nowofol Anwendung **Planlage Kamera**.

## Zuständigkeit

Support und Pflege erfolgen intern durch Nowofol beziehungsweise durch die zuständigen Administratoren der Anwendung.

## Empfohlener Support-Ablauf

1. Fehlerbild kurz beschreiben.
2. App-Version aus der Titelleiste notieren.
3. Prüfen, ob Kamera und Ablageordner erreichbar sind.
4. Falls vorhanden, `camera_diagnostics.log` sichern.
5. Prüfen, ob das aktuellste Release installiert ist.

## Informationen bei Fehlern

Für eine schnelle Analyse bitte folgende Informationen bereithalten:

- App-Version aus der Titelleiste.
- Windows-Version.
- Verwendete Kamera.
- Aktive Kameraauflösung aus der rechten Bedienleiste.
- Beschreibung des Fehlers.
- Zeitpunkt des Fehlers.
- Falls vorhanden: Inhalt von `camera_diagnostics.log`.
- Ob der Fehler nach einem Update, Kamerawechsel oder Pfadwechsel aufgetreten ist.

## Typische Prüfungen

- Kamera in Windows freigegeben?
- Kamera bereits durch ein anderes Programm belegt?
- Schreibrechte im Ablageordner vorhanden?
- Netzwerkablage erreichbar?
- Admin-Passwort bekannt?
- Aktuelles GitHub Release vorhanden?

## Update-Probleme

Wenn die automatische Aktualisierung nicht funktioniert:

- Prüfen, ob das GitHub Release ein Asset `Planlage_Kamera.exe` enthält.
- Prüfen, ob die Release-Version höher ist als die lokale Version.
- Bei privatem Repository prüfen, ob der Ziel-PC Zugriff auf das Release hat.
- Prüfen, ob der Ziel-PC `https://github.com/MarioNowofol/Update_Planlage_Kamera/releases/latest` erreichen kann.
- Prüfen, ob Sicherheitssoftware den Download einer EXE blockiert.

## Wiederherstellung

Wenn ein Update fehlschlägt, kann die aktuelle EXE aus dem neuesten GitHub Release erneut heruntergeladen und manuell in den Installationsordner kopiert werden. Die lokale `config.json` sollte dabei erhalten bleiben, weil sie Ablagepfad, Kameraauswahl und Passwörter enthält.
