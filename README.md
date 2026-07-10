# My AI Code Guidelines

Wiederverwendbare Leitlinien und Dokumentationsvorlagen für die Arbeit mit **Claude Code**, **OpenAI Codex**, **ChatGPT Projects** und **GitHub Copilot**.

Das Repository trennt bewusst zwischen:

1. **modellunabhängigen Arbeitsregeln**,
2. **werkzeugspezifischen Einstiegspunkten** und
3. **projektspezifischer Dokumentation**.

## Ziel

Die Vorlagen sollen typische Fehler bei KI-gestützter Softwareentwicklung reduzieren:

- unnötige Änderungen und Refactorings,
- stillschweigende Annahmen,
- erfundene APIs, Parameter oder Produkteigenschaften,
- überkomplizierte Lösungen,
- fehlende Verifikation,
- unsichere Standardeinstellungen,
- unklare oder nicht reproduzierbare Ergebnisse.

## Repository-Inhalt

| Datei | Zweck |
|---|---|
| [`AI-GUIDELINES.md`](AI-GUIDELINES.md) | Allgemeine, modellunabhängige Arbeitsregeln |
| [`CLAUDE.md`](CLAUDE.md) | Einstiegspunkt für Claude Code |
| [`AGENTS.md`](AGENTS.md) | Einstiegspunkt für OpenAI Codex und kompatible Coding Agents |
| [`.github/copilot-instructions.md`](.github/copilot-instructions.md) | Repository-Anweisungen für GitHub Copilot |
| [`docs/project-goals.md`](docs/project-goals.md) | Projektziele, Nicht-Ziele und Prioritäten |
| [`docs/architecture.md`](docs/architecture.md) | Architektur, Komponenten und Datenflüsse |
| [`docs/coding-standards.md`](docs/coding-standards.md) | Allgemeine Coding-Konventionen |
| [`docs/testing.md`](docs/testing.md) | Teststrategie und Definition of Done |
| [`docs/security.md`](docs/security.md) | Sicherheitsanforderungen und sichere Standards |
| [`docs/deployment.md`](docs/deployment.md) | Build-, Release- und Deployment-Prozess |
| [`docs/decisions.md`](docs/decisions.md) | Architekturentscheidungen im ADR-Format |
| [`docs/ui-guidelines.md`](docs/ui-guidelines.md) | UI-, UX- und Accessibility-Vorgaben |
| [`docs/powershell.md`](docs/powershell.md) | PowerShell-Konventionen |
| [`docs/python.md`](docs/python.md) | Python-Konventionen |
| [`docs/html-css-js.md`](docs/html-css-js.md) | HTML-, CSS- und JavaScript-Konventionen |

## Empfohlene Struktur in einem Projekt

```text
.
├── README.md
├── AI-GUIDELINES.md
├── CLAUDE.md
├── AGENTS.md
├── .github/
│   └── copilot-instructions.md
├── docs/
│   ├── project-goals.md
│   ├── architecture.md
│   ├── coding-standards.md
│   ├── testing.md
│   ├── security.md
│   ├── deployment.md
│   ├── decisions.md
│   ├── ui-guidelines.md
│   ├── powershell.md
│   ├── python.md
│   └── html-css-js.md
├── src/
└── tests/
```

## Nutzung als Vorlage

### Neues Repository

1. Dieses Repository in GitHub unter **Settings → General → Template repository** als Vorlage markieren.
2. Über **Use this template** ein neues Projekt erstellen.
3. Nicht benötigte Sprach- oder UI-Dokumente entfernen.
4. Platzhalter in den Dateien unter `docs/` ausfüllen.
5. Konkrete Build-, Test- und Security-Befehle in `docs/testing.md` ergänzen.
6. Architektur, Ziele und Deployment an das neue Projekt anpassen.

### Bestehendes Repository

Als Mindestumfang übernehmen:

```text
AI-GUIDELINES.md
CLAUDE.md
AGENTS.md
.github/copilot-instructions.md
docs/project-goals.md
docs/architecture.md
docs/testing.md
docs/security.md
```

Danach nur die für das Projekt relevanten Zusatzdokumente ergänzen.

## Einrichtung nach Werkzeug

### Claude Code

Claude Code verwendet `CLAUDE.md` als Einstiegspunkt. Die Datei verweist auf die gemeinsamen Regeln und die Projektdokumentation.

Globale persönliche Regeln können zusätzlich unter folgendem Pfad gepflegt werden:

```text
~/.claude/CLAUDE.md
```

Dort sollten nur dauerhaft gültige Präferenzen stehen, beispielsweise Deutsch als Standardsprache oder die gewünschte Kommunikationsform.

### OpenAI Codex

Codex verwendet `AGENTS.md` als projektspezifischen Einstiegspunkt. Diese Datei verweist ebenfalls auf die gemeinsamen Richtlinien.

Bei größeren Repositories können zusätzliche `AGENTS.md`-Dateien in Unterverzeichnissen spezifischere Regeln für den jeweiligen Bereich enthalten.

### GitHub Copilot

Repository-weite Anweisungen liegen unter:

```text
.github/copilot-instructions.md
```

Die Datei sollte kurz bleiben und auf die detaillierten Projektdokumente verweisen.

### ChatGPT Projects

Für ein ChatGPT Project:

1. Ein eigenes Projekt für das Softwarevorhaben anlegen.
2. Die relevanten Dateien dieses Repositories als Projektdateien bereitstellen oder das GitHub-Repository verbinden.
3. In den Projektanweisungen Deutsch als Standardsprache und die verbindliche Nutzung von `AI-GUIDELINES.md` festlegen.
4. Projektbezogene Chats ausschließlich innerhalb dieses Projekts führen.

## Was gehört wohin?

| Information | Global | Repository | Lokal / Secret Store |
|---|:---:|:---:|:---:|
| Standardsprache | X | optional | |
| Kommunikationsstil | X | optional | |
| Architektur | | X | |
| Frameworks und Versionen | | X | |
| Build- und Testbefehle | | X | |
| Sicherheitsanforderungen | allgemein | X | |
| Definition of Done | | X | |
| Lokale Pfade und Testserver | | | X |
| Passwörter, Tokens und Schlüssel | | | X |

## Anpassungsreihenfolge

Für ein neues Projekt zuerst diese Dateien bearbeiten:

1. [`docs/project-goals.md`](docs/project-goals.md)
2. [`docs/architecture.md`](docs/architecture.md)
3. [`docs/testing.md`](docs/testing.md)
4. [`docs/security.md`](docs/security.md)
5. [`docs/deployment.md`](docs/deployment.md)
6. relevante sprachspezifische Richtlinien

Nicht benötigte Vorlagen sollten entfernt werden. Eine kurze und aktuelle Dokumentation ist wirksamer als eine umfangreiche, veraltete Sammlung.

## Pflegeprinzipien

- Allgemeine Regeln zentral in `AI-GUIDELINES.md` pflegen.
- Werkzeugspezifische Dateien möglichst kurz halten.
- Projektwissen nicht in globale persönliche Einstellungen aufnehmen.
- Änderungen an Architektur oder Betrieb im selben Commit dokumentieren.
- Wiederkehrende Korrekturen als verbindliche Regel aufnehmen.
- Widersprüche zwischen Dokumenten zeitnah auflösen.

## Grenzen

Die Dateien ersetzen keine technische oder fachliche Prüfung. KI-generierter Code muss weiterhin durch geeignete Tests, Reviews, Sicherheitskontrollen und die im Projekt vorgesehenen Freigaben validiert werden.

Auch die automatische Berücksichtigung einzelner Dateien kann sich zwischen Produkten und Versionen unterscheiden. Die werkzeugspezifischen Einstiegspunkte sollten deshalb regelmäßig gegen die aktuelle Produktdokumentation geprüft werden.
