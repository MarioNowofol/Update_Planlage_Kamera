# Planlage Kamera - Update-Kanal

Dieses Repository ist der öffentliche Update-Kanal für die Nowofol Anwendung **Planlage Kamera**.

Die Anwendung wurde gemeinsam mit **Codex AI** erstellt und weiterentwickelt.

## Zweck dieses Repositories

Das eigentliche Entwicklungsrepository `MarioNowofol/Planlage_Kamera` bleibt privat. Dort liegen Quellcode, Projektstruktur, interne Entwicklungsdateien und technische Pflegeinformationen.

Dieses Repository `MarioNowofol/Update_Planlage_Kamera` ist bewusst öffentlich. Es enthält nur die Dateien, die Ziel-PCs für automatische Updates und Anwenderinformation benötigen. Dadurch kann die App ohne GitHub-Login und ohne zusätzlichen Token prüfen, ob eine neue Version verfügbar ist.

## Enthaltene Dateien

Typischer Inhalt:

- `Planlage_Kamera.exe` als Release-Asset
- `Ausfuehrliche_Dokumentation.pdf` als technische Dokumentation
- `PATCHNOTES.md` mit Versionsänderungen
- `docs/UPDATE_SYSTEM.md` mit Beschreibung des Update-Ablaufs
- `SUPPORT.md` und `SECURITY.md`

Der vollständige Quellcode wird hier nicht veröffentlicht.

## Update-Ablauf

Beim Start prüft die App das neueste GitHub Release dieses Repositories. Wenn eine höhere Version verfügbar ist und das Release die Datei `Planlage_Kamera.exe` enthält, fragt die App den Anwender, ob das Update installiert werden soll.

Im Updatefenster werden nur die Patchnotes angezeigt, die zwischen der lokal installierten Version und der neuesten verfügbaren Version liegen.

Nach Zustimmung lädt die App die neue EXE herunter, ersetzt die laufende Anwendung und startet anschließend neu.

## Release-Anforderung

Jedes produktive Release muss mindestens dieses Asset enthalten:

```text
Planlage_Kamera.exe
```

Empfohlen ist zusätzlich:

```text
Ausfuehrliche_Dokumentation.pdf
```

Die aktuelle Version ist immer über diese Adresse erreichbar:

```text
https://github.com/MarioNowofol/Update_Planlage_Kamera/releases/latest
```

## Sicherheitsprinzip

In diesem öffentlichen Repository dürfen keine Passwörter, Tokens, internen Konfigurationsdateien oder vertraulichen Entwicklungsinformationen abgelegt werden.

## Betreiber

Nowofol Kunststoffprodukte GmbH & Co. KG
