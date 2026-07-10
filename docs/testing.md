# Testing und Definition of Done

Diese Datei beschreibt, welche Prüfungen vor Abschluss einer Änderung erwartet werden. Projektspezifische Befehle müssen ergänzt werden.

## Teststrategie

| Testart | Zweck | Befehl/Werkzeug |
|---|---|---|
| Unit Tests | Fachlogik und isolierte Komponenten | <!-- ergänzen --> |
| Integrationstests | Zusammenspiel von Komponenten | <!-- ergänzen --> |
| End-to-End-Tests | Kritische Nutzer- und Betriebsabläufe | <!-- ergänzen --> |
| Statische Analyse | Typen, Regeln und typische Fehler | <!-- ergänzen --> |
| Security Checks | Abhängigkeiten, Secrets und Schwachstellen | <!-- ergänzen --> |

## Mindestprüfungen

Vor Abschluss soweit anwendbar:

1. Der ursprüngliche Fehler oder Anwendungsfall wurde reproduziert.
2. Die Änderung erfüllt die festgelegten Erfolgskriterien.
3. Bestehende Tests laufen erfolgreich.
4. Neue oder geänderte Logik ist durch geeignete Tests abgedeckt.
5. Build, Linter und statische Analyse erzeugen keine neuen Fehler.
6. Relevante Negativ- und Randfälle wurden geprüft.
7. Dokumentation und Beispiele entsprechen dem tatsächlichen Verhalten.
8. Es wurden keine Secrets oder sensiblen Daten eingecheckt.

## Wann neue Tests erforderlich sind

Neue oder angepasste Tests sind grundsätzlich erforderlich bei:

- Fehlerbehebungen,
- neuer Fachlogik,
- Änderungen an Validierung oder Fehlerbehandlung,
- Änderungen öffentlicher Schnittstellen,
- sicherheitsrelevanten Änderungen,
- Regressionen mit reproduzierbarem Testfall.

Bei rein redaktionellen Änderungen kann auf automatisierte Tests verzichtet werden, wenn keine ausführbare Logik betroffen ist.

## Projektspezifische Befehle

```text
# Build
<!-- Befehl ergänzen -->

# Tests
<!-- Befehl ergänzen -->

# Linter / statische Analyse
<!-- Befehl ergänzen -->

# Security Checks
<!-- Befehl ergänzen -->
```

## Definition of Done

Eine Änderung gilt erst als abgeschlossen, wenn:

- die Anforderung umgesetzt ist,
- der Scope nicht ungefragt erweitert wurde,
- die relevanten Prüfungen erfolgreich waren,
- sicherheitsrelevante Auswirkungen bewertet wurden,
- Dokumentation bei Bedarf aktualisiert wurde,
- durchgeführte und nicht mögliche Prüfungen transparent benannt wurden.

## Abschlussbericht

```text
Geändert:
- ...

Geprüft:
- ...

Nicht geprüft / offen:
- ...
```
