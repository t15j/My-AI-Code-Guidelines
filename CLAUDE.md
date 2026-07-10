# CLAUDE.md

Diese Datei ist der Einstiegspunkt für Claude Code.

## Verbindliche Reihenfolge

Vor Änderungen sind folgende Dateien zu lesen:

1. `AI-GUIDELINES.md`
2. `docs/project-goals.md`
3. `docs/architecture.md`
4. `docs/coding-standards.md`
5. `docs/testing.md`
6. `docs/security.md`
7. bei Bedarf die sprach- oder technologiespezifischen Dokumente unter `docs/`

## Sprache

- Deutsch ist die Standardsprache.
- Code, APIs, technische Bezeichner, Befehle, Produktnamen, Konfigurationsschlüssel und Fehlermeldungen bleiben in ihrer Originalsprache.
- Eine andere Sprache wird nur verwendet, wenn sie ausdrücklich verlangt wird oder für das Zielpublikum erforderlich ist.

## Arbeitsweise

- Vorhandenen Code und Dokumentation vor Änderungen vollständig genug verstehen.
- Annahmen und wesentliche Unsicherheiten ausdrücklich benennen.
- Nur den angeforderten Umfang umsetzen.
- Keine ungefragten Refactorings, Umbenennungen, Formatierungsänderungen oder zusätzlichen Features durchführen.
- Bestehenden Stil und bestehende Architekturgrenzen beibehalten.
- Einfache, sichere und wartbare Lösungen bevorzugen.
- Neue Abhängigkeiten nur bei belegtem Nutzen und ausdrücklicher Freigabe einführen.

## Planung und Verifikation

Bei komplexeren Aufgaben einen kurzen Plan mit überprüfbaren Kriterien formulieren:

```text
1. Schritt -> Prüfung
2. Schritt -> Prüfung
3. Schritt -> Prüfung
```

Vor Abschluss die in `docs/testing.md` vorgesehenen Tests, Builds, Linter und Kontrollen soweit möglich ausführen.

Der Abschlussbericht enthält:

1. **Geändert** – tatsächlich umgesetzte Änderungen.
2. **Geprüft** – tatsächlich ausgeführte Prüfungen und Ergebnisse.
3. **Offen** – nicht mögliche Prüfungen, bekannte Risiken oder manuelle Schritte.

## Sicherheit

Die Vorgaben aus `docs/security.md` sind verbindlich. Insbesondere:

- keine Secrets im Code, Repository oder Log,
- keine deaktivierte TLS- oder Zertifikatsprüfung,
- keine unnötigen Berechtigungen,
- keine ungeprüften externen Eingaben,
- keine erfundenen APIs, Parameter, Funktionen oder Testergebnisse.

## Dokumentation

Wenn sich Verhalten, Architektur, Betrieb, Konfiguration oder öffentliche Schnittstellen ändern, die zugehörige Dokumentation im selben Änderungssatz aktualisieren.

Projektbezogene Regeln haben Vorrang vor allgemeinen Empfehlungen, sofern sie nicht zu unsicheren oder offensichtlich fehlerhaften Ergebnissen führen.
