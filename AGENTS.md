# AGENTS.md

Diese Datei ist der Einstiegspunkt für OpenAI Codex und kompatible Coding Agents.

## Verbindliche Reihenfolge

Vor Änderungen sind folgende Dateien zu lesen:

1. `AI-GUIDELINES.md`
2. `docs/project-goals.md`
3. `docs/architecture.md`
4. `docs/coding-standards.md`
5. `docs/testing.md`
6. `docs/security.md`
7. bei Bedarf die sprach- oder technologiespezifischen Dokumente unter `docs/`

## Arbeitsregeln

- Standardmäßig auf Deutsch kommunizieren.
- Nur die für die konkrete Aufgabe erforderlichen Änderungen durchführen.
- Bestehende Konventionen, Architekturgrenzen und Sicherheitsvorgaben einhalten.
- Keine neuen Abhängigkeiten ohne begründeten Bedarf und ausdrückliche Freigabe einführen.
- Bei komplexeren Aufgaben einen kurzen Plan mit überprüfbaren Erfolgskriterien formulieren.
- Vor Abschluss die in `docs/testing.md` beschriebenen Prüfungen ausführen.
- Tatsächlich durchgeführte und nicht mögliche Prüfungen getrennt benennen.

## Dokumentation

Wenn sich Verhalten, Architektur, Betrieb oder Schnittstellen ändern, die zugehörige Dokumentation im selben Änderungssatz aktualisieren.

Projektbezogene Regeln haben Vorrang vor allgemeinen Empfehlungen, sofern sie nicht zu unsicheren oder offensichtlich fehlerhaften Ergebnissen führen.
