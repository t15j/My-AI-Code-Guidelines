# Architecture Decisions

Diese Datei dokumentiert wesentliche technische Entscheidungen. Für umfangreiche Projekte können einzelne ADR-Dateien unter `docs/adr/` verwendet werden.

## Statuswerte

- Proposed
- Accepted
- Deprecated
- Superseded

## Vorlage

```markdown
## ADR-XXX: Titel

- Status: Proposed
- Datum: YYYY-MM-DD
- Verantwortlich: Name/Rolle

### Kontext

Welches Problem oder welche Randbedingung erfordert eine Entscheidung?

### Entscheidung

Welche Option wurde gewählt?

### Alternativen

Welche realistischen Alternativen wurden betrachtet?

### Konsequenzen

Welche positiven und negativen Auswirkungen entstehen?

### Verifikation

Woran wird erkannt, dass die Entscheidung funktioniert?
```

---

## ADR-001: Modellunabhängige KI-Richtlinien

- Status: Accepted
- Datum: 2026-07-10

### Kontext

Mehrere Coding-Assistenten verwenden unterschiedliche Einstiegspunkte und Konfigurationsmechanismen.

### Entscheidung

Gemeinsame Arbeitsregeln werden zentral in `AI-GUIDELINES.md` gepflegt. `CLAUDE.md`, `AGENTS.md` und `.github/copilot-instructions.md` dienen als werkzeugspezifische Einstiegspunkte.

### Konsequenzen

- Gemeinsame Regeln müssen nur an einer Stelle fachlich gepflegt werden.
- Einstiegspunkt-Dateien müssen auf die zentrale Richtlinie verweisen.
- Werkzeugspezifische Besonderheiten bleiben separat dokumentierbar.
