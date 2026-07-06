# Update-System

Die Planlage Kamera kann beim Start automatisch prüfen, ob im GitHub Repository ein neueres Release vorhanden ist.

## Quelle

Standardmäßig prüft die App:

```text
MarioNowofol/Update_Planlage_Kamera
```

Das eigentliche Quellcode-Repository kann privat bleiben. Das öffentliche Update-Repository enthält nur die Dateien, die für Installation, Updateprüfung und Anwenderinformation benötigt werden.

Die Werte können in den Einstellungen angepasst werden:

- `GitHub Owner`
- `GitHub Repository`
- `Updates beim Start prüfen`

## Repository-Aufteilung

Die Veröffentlichung ist bewusst in zwei Repositories getrennt:

| Repository | Sichtbarkeit | Inhalt |
| --- | --- | --- |
| `MarioNowofol/Planlage_Kamera` | privat | Quellcode, interne Dokumentation, Scripte, private Releases |
| `MarioNowofol/Update_Planlage_Kamera` | öffentlich | Update-Releases, Patchnotes, Support-/Security-Hinweise, technische PDF |

Dieser Aufbau schützt den Quellcode und erlaubt trotzdem einfache Updates auf Ziel-PCs ohne GitHub-Login.

## Release-Anforderung

Damit die App ein Update findet, muss das GitHub Release diese Bedingungen erfüllen:

- Tag im Format `vX.Y.Z`, zum Beispiel `v3.0.0`.
- Die Versionsnummer muss höher sein als die lokale App-Version.
- Das Release muss ein Asset mit exakt diesem Namen enthalten:

```text
Planlage_Kamera.exe
```

Optional, aber empfohlen:

```text
Ausfuehrliche_Dokumentation.pdf
```

Die Release-Assets müssen exakt so heißen. Abweichende Dateinamen werden von der App nicht als Update erkannt.

## Ablauf in der App

1. Beim Start ruft die App die GitHub Releases API ab.
2. Die neueste Release-Version wird mit der lokalen Version verglichen.
3. Wenn eine neuere Version gefunden wird, fragt die App den Anwender und zeigt nur die Patchnotes der Versionsdifferenz an.
4. Bei Zustimmung lädt die App die neue `Planlage_Kamera.exe` in den Temp-Ordner.
5. Ein kleines Update-Skript wartet, bis die laufende App beendet ist.
6. Die alte EXE wird ersetzt.
7. Die neue Version wird automatisch gestartet.

## Verhalten bei Fehlern

Wenn die Update-Prüfung fehlschlägt, soll der Aufnahmebetrieb nicht blockiert werden. Typische Ursachen sind:

- Keine Internetverbindung.
- GitHub ist vom Ziel-PC aus nicht erreichbar.
- Das Release enthält kein Asset `Planlage_Kamera.exe`.
- Die Release-Version ist nicht höher als die lokale App-Version.
- Sicherheitssoftware blockiert den Download.

In diesen Fällen kann die neue Version manuell aus dem Release heruntergeladen und ersetzt werden. Die lokale `config.json` sollte erhalten bleiben.

## Private Repositories

Wenn ein Repository privat ist, kann ein normaler Ziel-PC ohne GitHub-Token Releases nicht anonym lesen oder herunterladen. Deshalb verwendet die App ab Version 2.0.8 standardmäßig das öffentliche Repository `MarioNowofol/Update_Planlage_Kamera` als Update-Kanal.

Vorteile dieses Aufbaus:

- Der Quellcode bleibt im privaten Haupt-Repository.
- Ziel-PCs benötigen keinen GitHub-Login und keinen Token.
- Die App kann Updates direkt über GitHub Releases finden und herunterladen.
- Das öffentliche Repository bleibt schlank und enthält nur Release-Dateien, Patchnotes und Update-Hinweise.

## Pflegeprozess

Bei jeder App-Änderung:

1. Versionsnummer im Code und Projekt erhöhen.
2. `PATCHNOTES.md` aktualisieren.
3. Technische Dokumentation aktualisieren.
4. Release-Build erstellen.
5. Privates GitHub Code-Repository aktualisieren.
6. Öffentliches Update-Repository aktualisieren.
7. Neues GitHub Release im Update-Repository mit `Planlage_Kamera.exe` anlegen.
8. Optional `Ausfuehrliche_Dokumentation.pdf` als zusätzliches Release-Asset hochladen.
9. Prüfen, ob `releases/latest` auf das neue Release zeigt.
10. Optional mit einer älteren Testversion prüfen, ob der Update-Dialog erscheint.

Für Version 3.0.0 müssen insbesondere diese Release-Assets bereitgestellt werden:

```text
Planlage_Kamera.exe
Ausfuehrliche_Dokumentation.pdf
```

## Standard-Veröffentlichung

Der bevorzugte Veröffentlichungsweg ist das vorbereitete Script:

```powershell
powershell -ExecutionPolicy Bypass -File .\scripts\publish_v3_0_0_no_git.ps1
```

Das Script benötigt eine angemeldete GitHub CLI mit Schreibrechten auf beide Repositories. Es aktualisiert Quellcode, Dokumente, Update-Repository und Release-Assets.
