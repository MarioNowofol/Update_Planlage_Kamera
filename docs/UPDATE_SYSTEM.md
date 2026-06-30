# Update-System

Die Planlage Kamera verwendet dieses öffentliche Repository als Update-Kanal:

```text
MarioNowofol/Update_Planlage_Kamera
```

Das private Entwicklungsrepository bleibt geschützt. Ziel-PCs benötigen dadurch keinen GitHub-Token, weil nur die Release-Dateien dieses öffentlichen Repositories abgefragt werden.

## Release-Anforderungen

Ein Release muss diese Bedingungen erfüllen:

- Tag im Format `vX.Y.Z`, zum Beispiel `v2.0.8`
- Versionsnummer höher als die lokal installierte App-Version
- Asset mit exakt diesem Namen:

```text
Planlage_Kamera.exe
```

Optional empfohlen:

```text
Ausfuehrliche_Dokumentation.pdf
```

## Ablauf in der App

1. Die App fragt `releases/latest` dieses Repositories ab.
2. Die neueste Version wird mit der lokalen App-Version verglichen.
3. Bei einer neueren Version fragt die App den Anwender.
4. Nach Zustimmung wird `Planlage_Kamera.exe` heruntergeladen.
5. Die laufende App wird beendet.
6. Die EXE wird ersetzt.
7. Die neue Version wird gestartet.

## Hinweis

Die Anwendung wurde gemeinsam mit Codex AI erstellt und weiterentwickelt.

