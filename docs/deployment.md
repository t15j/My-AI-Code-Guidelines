# Deployment

Diese Datei beschreibt den reproduzierbaren Weg vom Quellcode bis zur Zielumgebung sowie Wiederanlauf und Rollback.

## Umgebungen

| Umgebung | Zweck | Freigabe | Datenklasse |
|---|---|---|---|
| Development | Lokale Entwicklung | Entwickler | Testdaten |
| Test/Staging | Integrations- und Abnahmetests | <!-- ergänzen --> | <!-- ergänzen --> |
| Production | Produktiver Betrieb | <!-- ergänzen --> | <!-- ergänzen --> |

## Voraussetzungen

- <!-- Laufzeit und Version -->
- <!-- Externe Dienste -->
- <!-- Berechtigungen -->
- <!-- Secret Store / Konfiguration -->

## Build

```text
<!-- Reproduzierbare Build-Befehle ergänzen -->
```

Build-Artefakte müssen aus einem definierten Commit erzeugt und eindeutig versioniert werden.

## Deployment-Ablauf

1. Änderungen prüfen und freigeben.
2. Tests und Security Checks ausführen.
3. Versioniertes Artefakt erzeugen.
4. Konfiguration und Secrets für die Zielumgebung bereitstellen.
5. Deployment durchführen.
6. Health Checks und Smoke Tests ausführen.
7. Ergebnis und Version dokumentieren.

## Datenbank- und Datenänderungen

<!-- Migrationen, Reihenfolge, Rückwärtskompatibilität, Backup und Wiederherstellung beschreiben. -->

## Rollback

```text
<!-- Konkrete Rollback-Schritte ergänzen -->
```

Ein Rollback muss berücksichtigen:

- Anwendungsversion,
- Konfigurationsänderungen,
- Datenbankmigrationen,
- Caches und Queues,
- externe Schnittstellen.

## Verifikation nach Deployment

- Anwendung beziehungsweise Dienst ist erreichbar.
- Kritische Geschäfts- und Nutzerabläufe funktionieren.
- Logs zeigen keine neuen kritischen Fehler.
- Monitoring und Alarmierung funktionieren.
- Die tatsächlich ausgerollte Version ist nachvollziehbar.

## Betriebsübergabe

- Bekannte Einschränkungen dokumentieren.
- Monitoring und Verantwortlichkeiten benennen.
- Wiederanlauf- und Eskalationswege bereitstellen.
- Notwendige manuelle Schritte dokumentieren.

## Pflege

Bei Änderungen an Build, Laufzeit, Zielumgebung, Freigaben, Migration oder Rollback aktualisieren.
