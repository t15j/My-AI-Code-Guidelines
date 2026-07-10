# PowerShell Guidelines

## Geltungsbereich

Diese Regeln ergänzen `coding-standards.md` für PowerShell-Projekte.

## Konventionen

- Genehmigte Verb-Noun-Namen für Funktionen verwenden.
- Aussagekräftige Parameternamen und konsistente Schreibweise nutzen.
- `Set-StrictMode` nur einsetzen, wenn das Projekt und die Zielumgebung damit getestet sind.
- Für wiederverwendbare Skripte einen `param()`-Block und nach Möglichkeit `[CmdletBinding()]` verwenden.
- Seiteneffekte transparent machen und bei destruktiven Aktionen `SupportsShouldProcess` beziehungsweise `-WhatIf` unterstützen.

## Fehlerbehandlung

- Bei externen Aufrufen gezielt `-ErrorAction Stop` verwenden, wenn Fehler per `try/catch` behandelt werden sollen.
- Keine leeren Catch-Blöcke.
- Fehlermeldungen mit relevantem Kontext ausgeben, ohne Secrets offenzulegen.
- `$ErrorActionPreference` nicht global ohne nachvollziehbaren Grund verändern.

## Ausgabe und Logging

- Pipelinefähige Objekte statt vorformatierter Textausgabe zurückgeben, sofern das Skript weiterverarbeitet werden soll.
- `Write-Host` nur für bewusst nicht weiterzuverarbeitende Statusausgaben verwenden.
- Für Fortschrittsanzeigen `Write-Progress` einsetzen, wenn die Gesamtdauer relevant und eine messbare Basis vorhanden ist.
- Logs mit Zeitstempel, Aktion, Ergebnis und Fehlerkontext versehen.

## Dateien und CSV

- Textdateien explizit mit geeigneter UTF-8-Kodierung schreiben.
- Für deutschsprachige Excel-Umgebungen CSV standardmäßig mit Semikolon als Trennzeichen erzeugen, sofern das Projekt nichts anderes vorgibt.
- Pfade mit `Join-Path` zusammensetzen und Eingabepfade validieren.
- UNC-Pfade und lange Laufzeiten bei Dateioperationen berücksichtigen.

## Sicherheit

- Keine Credentials im Skript speichern.
- Für Anmeldeinformationen sichere Plattformmechanismen verwenden.
- Zertifikatsprüfung nicht deaktivieren.
- Destruktive Datei-, AD-, Exchange- oder Cloud-Aktionen mit Dry-Run beziehungsweise `-WhatIf` absichern, sofern technisch möglich.

## Tests und Analyse

Empfohlene Werkzeuge, sofern im Projekt eingesetzt:

```powershell
Invoke-ScriptAnalyzer -Path . -Recurse
Invoke-Pester
```

Konkrete Befehle und Versionen in `testing.md` festlegen.
