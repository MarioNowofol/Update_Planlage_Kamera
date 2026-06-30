# Planlage Kamera - Update-Kanal

Dieses Repository ist der öffentliche Update-Kanal für die Nowofol Anwendung **Planlage Kamera**.

Die Anwendung wurde gemeinsam mit **Codex AI** erstellt und weiterentwickelt.

## Warum gibt es dieses Repository?

Das ursprüngliche Repository `MarioNowofol/Planlage_Kamera` ist das private Entwicklungs- und Quellcode-Repository. Dort liegen der Quellcode, die Projektstruktur, interne Entwicklungsdateien und die vollständige technische Pflege der Anwendung.

Dieses Repository `MarioNowofol/Update_Planlage_Kamera` ist bewusst öffentlich. Es enthält nur die Dateien, die für automatische Updates und Anwenderinformation benötigt werden. Dadurch kann die App auf einem normalen Ziel-PC ohne GitHub-Login und ohne zusätzlichen Token prüfen, ob eine neue Version verfügbar ist.

## Inhalt dieses Repositories

Dieses Repository enthält typischerweise:

- `Planlage_Kamera.exe` als Release-Asset
- `Ausfuehrliche_Dokumentation.pdf` als technische Dokumentation
- `PATCHNOTES.md` mit Versionsänderungen
- Hinweise zum Update-System
- Support- und Sicherheitsinformationen

Der vollständige Quellcode wird hier nicht veröffentlicht.

## Update-Ablauf

Beim Start prüft die App das neueste GitHub Release dieses Repositories. Wenn eine höhere Version verfügbar ist und das Release die Datei `Planlage_Kamera.exe` enthält, fragt die App den Anwender, ob das Update installiert werden soll.

Nach Zustimmung lädt die App die neue EXE herunter, ersetzt die laufende Anwendung und startet anschließend neu.

## Aktuelle Release-Dateien

Die aktuelle Version befindet sich unter:

```text
https://github.com/MarioNowofol/Update_Planlage_Kamera/releases/latest
```

Für automatische Updates muss jedes Release mindestens diese Datei enthalten:

```text
Planlage_Kamera.exe
```

Empfohlen ist zusätzlich:

```text
Ausfuehrliche_Dokumentation.pdf
```

## Betreiber

Nowofol Kunststoffprodukte GmbH & Co. KG

