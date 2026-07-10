# Architektur

Diese Datei beschreibt die technische Struktur, Verantwortlichkeiten und zulässigen Abhängigkeiten des Projekts. Sie soll verhindern, dass Änderungen bestehende Architekturgrenzen unbeabsichtigt verletzen.

## Systemüberblick

<!-- Kurze Beschreibung des Systems und seiner Hauptkomponenten. -->

```text
[Client] -> [Anwendung/API] -> [Datenhaltung]
```

## Komponenten

| Komponente | Verantwortung | Technologie | Abhängigkeiten |
|---|---|---|---|
| <!-- Name --> | <!-- Zweck --> | <!-- Stack --> | <!-- Erlaubte Abhängigkeiten --> |

## Datenfluss

<!-- Beschreibe die wichtigsten Datenflüsse, Vertrauensgrenzen und externen Schnittstellen. -->

## Schnittstellen

| Schnittstelle | Richtung | Format/Protokoll | Authentifizierung | Dokumentation |
|---|---|---|---|---|
| <!-- API/Datei/Queue --> | <!-- ein/aus --> | <!-- HTTPS/JSON/CSV --> | <!-- Methode --> | <!-- Verweis --> |

## Architekturregeln

- Komponenten dürfen nur über dokumentierte Schnittstellen gekoppelt werden.
- Domänenlogik gehört nicht in UI-, Transport- oder Persistenzschichten.
- Neue externe Abhängigkeiten benötigen eine nachvollziehbare Begründung.
- Sicherheits- und Vertrauensgrenzen müssen explizit dokumentiert werden.
- Bestehende öffentliche Schnittstellen dürfen nicht unbeabsichtigt gebrochen werden.

## Betriebs- und Fehlerverhalten

<!-- Timeouts, Retries, Idempotenz, Transaktionen, Ausfallverhalten und Wiederanlauf beschreiben. -->

## Bekannte Einschränkungen

- <!-- Einschränkung oder technische Schuld -->

## Pflege

Bei Änderungen an Komponenten, Datenflüssen, Schnittstellen oder Architekturgrenzen aktualisieren. Wesentliche Entscheidungen zusätzlich in `decisions.md` dokumentieren.
