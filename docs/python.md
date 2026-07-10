# Python Guidelines

## Geltungsbereich

Diese Regeln ergänzen `coding-standards.md` für Python-Projekte.

## Sprache und Struktur

- Eine im Projekt festgelegte Python-Version verwenden.
- Type Hints für öffentliche Funktionen, komplexe Datenstrukturen und Schnittstellen einsetzen.
- `pathlib` gegenüber manueller Pfadverkettung bevorzugen.
- Kleine, klar abgegrenzte Module und Funktionen erstellen.
- Datenklassen oder klar definierte Modelle verwenden, wenn strukturierte Daten transportiert werden.
- Keine neuen Frameworks oder Hilfsbibliotheken ohne konkreten Mehrwert einführen.

## Fehlerbehandlung

- Nur erwartbare und sinnvoll behandelbare Exceptions abfangen.
- Keine pauschalen `except Exception`-Blöcke ohne erneutes Auslösen, Logging oder definierte Ersatzreaktion.
- Fehlermeldungen mit fachlichem Kontext versehen.
- Ressourcen über Context Manager verwalten.

## Logging

- Das Standardmodul `logging` oder die im Projekt etablierte Lösung verwenden.
- Keine Secrets oder vollständigen personenbezogenen Daten protokollieren.
- Bibliothekscode soll nicht ungefragt die globale Logging-Konfiguration verändern.

## Abhängigkeiten und Umgebung

- Virtuelle Umgebungen verwenden.
- Abhängigkeiten reproduzierbar dokumentieren beziehungsweise sperren.
- Entwicklungs-, Test- und Produktionsabhängigkeiten trennen, sofern das Projekt dies vorsieht.
- Importierbaren Projektcode nicht durch Laufzeit-Manipulation von `sys.path` strukturieren.

## Formatierung und Analyse

Empfohlene Werkzeuge, sofern im Projekt eingesetzt:

```text
ruff check .
ruff format --check .
pytest
mypy .
```

Die tatsächlich verbindlichen Werkzeuge, Versionen und Befehle werden in `testing.md` festgelegt.

## Sicherheit

- Keine dynamische Codeausführung mit ungeprüften Eingaben.
- SQL-Abfragen parametrisieren.
- Unsichere Deserialisierung vermeiden.
- TLS-Verifikation nicht deaktivieren.
- Temporäre Dateien sicher erzeugen und sensible Inhalte zuverlässig behandeln.

## Tests

- Fehlerbehebungen durch einen reproduzierenden Regressionstest absichern.
- Externe Systeme an klaren Grenzen mocken; interne Implementierungsdetails nicht unnötig mocken.
- Tests müssen deterministisch und voneinander unabhängig sein.
