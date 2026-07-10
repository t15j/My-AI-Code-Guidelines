# Coding Standards

Diese Datei enthält allgemeine, projektbezogene Implementierungsregeln. Sprachspezifische Ergänzungen stehen in separaten Dokumenten.

## Grundsätze

- Bestehenden Stil und bestehende Konventionen beibehalten.
- Lesbarkeit und Wartbarkeit vor Kürze oder Cleverness priorisieren.
- Funktionen und Methoden klein und auf eine Verantwortung begrenzt halten.
- Seiteneffekte und globale Zustände minimieren.
- Öffentliche Schnittstellen stabil halten oder Änderungen ausdrücklich dokumentieren.
- Neue Abhängigkeiten nur bei belegtem Nutzen einführen.

## Benennung

- Fachlich aussagekräftige Namen verwenden.
- Abkürzungen nur nutzen, wenn sie im Projekt etabliert sind.
- Keine Umbenennungen ausschließlich aus persönlicher Präferenz durchführen.

## Fehlerbehandlung

- Fehler nicht stillschweigend ignorieren.
- Fehler dort behandeln, wo eine sinnvolle Reaktion möglich ist.
- Fehlermeldungen müssen Ursache und betroffenen Kontext erkennen lassen, ohne Secrets offenzulegen.
- Keine pauschalen Catch-Blöcke ohne Logging, erneutes Auslösen oder definierte Ersatzreaktion.

## Logging

- Strukturierte und verwertbare Meldungen bevorzugen.
- Keine Passwörter, Tokens oder vollständigen personenbezogenen Daten protokollieren.
- Log-Level konsistent verwenden.
- Erwartbare Benutzerfehler nicht als Systemfehler protokollieren.

## Konfiguration

- Umgebungsabhängige Werte nicht im Code fest einbauen.
- Sichere Defaults verwenden.
- Konfigurationsschlüssel und zulässige Werte dokumentieren.
- Secrets über geeignete Secret Stores oder Umgebungsmechanismen bereitstellen.

## Abhängigkeiten

Vor einer neuen Abhängigkeit prüfen:

1. Lässt sich die Anforderung mit vorhandenen Mitteln einfach lösen?
2. Ist das Projekt aktiv gepflegt und für die Zielplattform geeignet?
3. Sind Lizenz, Sicherheitslage und Updateprozess akzeptabel?
4. Ist der Nutzen größer als zusätzlicher Betriebs- und Wartungsaufwand?

## Dokumentation

- Öffentliche oder nicht offensichtliche Schnittstellen dokumentieren.
- Kommentare erklären primär Gründe und Randbedingungen.
- Veraltete Kommentare im selben Änderungssatz korrigieren.

## Sprachspezifische Regeln

- PowerShell: [`powershell.md`](powershell.md)
- Python: [`python.md`](python.md)
- Web: [`html-css-js.md`](html-css-js.md)
