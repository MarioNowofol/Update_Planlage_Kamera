# Sicherheit

Dieses Dokument beschreibt die wichtigsten Sicherheits- und Datenschutzpunkte für Betrieb und Wartung der Anwendung.

## Passwortschutz

Die Einstellungen der Anwendung sind durch ein Admin-Passwort geschützt.

Das initiale Passwort lautet:

```text
admin
```

Dieses Passwort muss nach der ersten Inbetriebnahme geändert werden.

## Speicherung des Passworts

Das Admin-Passwort wird nicht im Klartext gespeichert. In `config.json` wird ausschließlich ein SHA-512-Hash abgelegt.

## Lokale Konfiguration

Die Datei `config.json` wird neben der EXE erzeugt und enthält lokale Einstellungen wie:

- Ablagepfad
- Kamera-ID
- Dateinamenmuster
- Zoom-Status
- Referenzlinien-Status
- Update-Konfiguration
- Admin-Passwort-Hash

Diese Datei wird nicht im GitHub Repository versioniert.

## Rollen und Zugriff

Die Anwendung trennt produktive Bedienung, QS-Einstellungen und Admin-Funktionen. Produktionsbenutzer sollen keine technischen Einstellungen ändern. QS und Admin erhalten nur die Einstellungen, die für ihre jeweilige Aufgabe erforderlich sind.

## Kamera und Datenschutz

Die Anwendung verarbeitet das Kamerabild lokal auf dem Windows-PC. Bilder werden nur gespeichert, wenn der Anwender aktiv eine Aufnahme auslöst.

## Update-Sicherheit

Die automatische Aktualisierung lädt ausschließlich das Release-Asset mit dem Namen:

```text
Planlage_Kamera.exe
```

aus dem konfigurierten GitHub Repository. Für produktive Nutzung sollte geprüft werden, dass Releases nur von berechtigten Personen erstellt werden.

Für das öffentliche Update-Repository gilt:

- Keine Tokens oder Passwörter veröffentlichen.
- Keine lokalen `config.json`-Dateien hochladen.
- Keine Diagnose-Logs mit internen Pfaden oder Fehlerdetails hochladen.
- Release-Dateien vor Veröffentlichung prüfen.
- Das private Quellcode-Repository bleibt geschützt.

## Private Repositories

Bei privaten GitHub Repositories ist ein normaler anonymer Update-Download nicht möglich. Für automatische Updates sollte entweder ein öffentlich erreichbares Release verwendet oder ein authentifiziertes internes Updateverfahren ergänzt werden.

Der aktuelle Aufbau nutzt deshalb ein öffentliches Update-Repository und ein privates Entwicklungsrepository. Das reduziert den Aufwand auf Ziel-PCs und vermeidet GitHub-Tokens in der Anwendung.
