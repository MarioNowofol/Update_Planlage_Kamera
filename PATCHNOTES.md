# Patchnotes

## v2.0.9

- Update-Dialog zeigt nur noch die Patchnotes der Versionsdifferenz zwischen lokal installierter Version und neuester verfügbarer Version.
- Kopfzeile optisch nachjustiert: gleichmäßigere Logo-Abstände, bessere Titelposition und höher ausgerichteter Dark-Mode-Toggle.
- Rechte Bedienleiste gegen Darstellungsfehler beim Maximieren stabilisiert.
- App-Version auf 2.0.9 erhöht.

## v2.0.8

- Neuer öffentlicher Update-Kanal: `MarioNowofol/Update_Planlage_Kamera`.
- Bestehende lokale Konfigurationen, die noch auf `MarioNowofol/Planlage_Kamera` zeigen, werden automatisch auf das öffentliche Update-Repository migriert.
- Privates Code-Repository und öffentlicher Update-Kanal sind dokumentiert.
- App-Version auf 2.0.8 erhöht.

## v2.0.7

- README und ausführliche technische Dokumentation weisen nun aus, dass die Anwendung gemeinsam mit Codex AI erstellt wurde.
- App-Version auf 2.0.7 erhöht.

## v2.0.6

- GitHub-Updatequelle vorkonfiguriert: `MarioNowofol/Planlage_Kamera`.
- Release-Asset für automatische Updates bleibt `Planlage_Kamera.exe`.

## v2.0.5

- App-Name bereinigt: sichtbarer Name und EXE heißen wieder `Planlage Kamera` bzw. `Planlage_Kamera.exe`.
- Update-System vorbereitet: Die App kann beim Start GitHub Releases prüfen, den User fragen, die neue EXE herunterladen, sich selbst austauschen und neu starten.
- Alte Python/OpenCV-Auslieferung entfernt.
- Kopfzeile erneut angepasst: Logo stabiler positioniert, Dark-Mode-Toggle ohne Zusatz-Host direkt in der Layout-Zelle.

## v2.0.4

- Rechte Bedienleiste mit festen Zeilenhöhen versehen, damit Eingabefelder beim Maximieren nicht verzerren.
- Logo und Dark-Mode-Toggle nachjustiert.
- Ablageanzeige auf volle Breite der rechten Bedienleiste gestreckt.
- Dark-Mode-Toggle mit sichtbarerem Rand versehen.

## v2.0.3

- Livebild-Fix: `SoftwareBitmap.CopyToBuffer` ersetzt direkten COM-Speicherzugriff.
- Direct3D-Kameraframes werden in SoftwareBitmaps umgewandelt.
- Kamera-Fallback: Wenn eine gestartete Kamera keinen verwertbaren Frame liefert, wird die nächste Kameraquelle getestet.
- Einstellungen erweitert: Ablagepfad per `Auswählen`-Button und sichtbare Dateinamen-Variablen.

## v2.0.2

- MediaFrameReader-Startstatus wird geprüft und protokolliert.
- Kamera-Diagnose über `camera_diagnostics.log` ergänzt.
- Preview-freundliche Kameraformate werden bevorzugt.
- UI weiter Richtung Windows-/Fluent-Look poliert.

## v2.0.1

- Schwarzes Livebild durch Alpha-/RGB-Konvertierung adressiert.
- Dark-Mode-Toggle eingeführt.
- Admin-Abfrage und Einstellungen optisch an den App-Look angepasst.

## v2.0.0

- Architekturwechsel von Python/OpenCV auf native Windows-App mit .NET 8 WinForms und Windows.Media.Capture.
- Kameraauswahl mit Windows-Gerätenamen.
- Höchste erkannte Kameraauflösung wird gewählt und angezeigt.
- Nowofol-Branding und technische PDF-Dokumentation neu strukturiert.

## v1.x

- Ursprüngliche Python/Tkinter/OpenCV-Version.
- Pflichtfelder für Auftragsnummer, Rollennummer und Gewicht.
- Dateiname mit Datum/Uhrzeit, Admin-Einstellungen, SHA-512-Passwort-Hash, Zoom, Referenzlinie und Explorer-Button.
