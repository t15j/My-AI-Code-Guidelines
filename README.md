# AI Assistant Setup Guide

Dieses Dokument beschreibt eine empfohlene Struktur für die Nutzung von **ChatGPT**, **Claude** und **Codex** in Softwareprojekten. Ziel ist eine konsistente Arbeitsweise über alle KI-Assistenten hinweg.

## Ziele

- Einheitliches Verhalten aller KI-Assistenten
- Weniger unnötige Änderungen im Code
- Nachvollziehbare Entscheidungen
- Wartbare Lösungen
- Wiederverwendbare Projektkonfiguration

---

# Architektur

Die Konfiguration sollte aus drei Ebenen bestehen:

```text
┌────────────────────────────┐
│ Globale Regeln             │
│ (persönliche Arbeitsweise) │
└─────────────┬──────────────┘
              │
              ▼
┌────────────────────────────┐
│ Projektregeln              │
│ (Repository)               │
└─────────────┬──────────────┘
              │
              ▼
┌────────────────────────────┐
│ Projektdokumentation        │
│ README, docs, Architektur   │
└────────────────────────────┘
```

---

# 1. Globale Regeln

Diese Regeln gelten für alle Projekte.

Sie sollten ausschließlich Dinge enthalten, die **immer** gelten.

Beispiele:

- Deutsch als Standardsprache
- Kommunikationsstil
- Umgang mit Unsicherheiten
- Transparenz
- Bevorzugung einfacher Lösungen
- Sicherheitsbewusstsein

Nicht hier hinein gehören:

- Frameworks
- Testbefehle
- Architektur
- Build-Kommandos
- Projektstruktur

---

# 2. Projektregeln

Diese Regeln beschreiben ausschließlich das jeweilige Repository.

Beispiele:

- verwendete Programmiersprachen
- Frameworks
- Architektur
- Testbefehle
- Linter
- Buildprozess
- Coding Standards
- Security-Anforderungen
- Definition of Done

---

# 3. Projektdokumentation

Hier befinden sich alle Informationen, die nicht dauerhaft in einer Prompt-Datei gepflegt werden sollten.

Typische Dateien:

```text
docs/
    architecture.md
    security.md
    testing.md
    deployment.md
README.md
```

Die KI kann diese Dokumente bei Bedarf lesen, ohne dass sämtliche Informationen in einer einzigen Datei gepflegt werden müssen.

---

# Einrichtung für Claude

## Globale Regeln

```text
~/.claude/CLAUDE.md
```

Diese Datei gilt für sämtliche Projekte.

Empfohlener Inhalt:

- Standardsprache Deutsch
- Kommunikationsstil
- Transparenz
- einfache Lösungen
- kleine Änderungen
- Tests durchführen
- Annahmen kennzeichnen

---

## Projektregeln

Im Repository:

```text
project/
│
├── CLAUDE.md
├── README.md
├── docs/
└── src/
```

Diese Datei wird versioniert und gilt für alle Entwickler.

Sie sollte enthalten:

- Projektbeschreibung
- Architektur
- Testbefehle
- Buildbefehle
- Sicherheitsregeln
- Definition of Done

---

## Persönliche Projektregeln

Optional:

```text
CLAUDE.local.md
```

Beispiele:

- lokale URLs
- persönliche Testserver
- Debug-Einstellungen

Diese Datei sollte nicht eingecheckt werden.

---

# Einrichtung für ChatGPT

## Benutzerdefinierte Anweisungen

Unter

```text
Einstellungen
→ Personalisierung
→ Benutzerdefinierte Anweisungen
```

gehören ausschließlich allgemeine Regeln hinein.

Zum Beispiel:

- Antworte auf Deutsch.
- Technische Begriffe nicht übersetzen.
- Annahmen kennzeichnen.
- Einfache Lösungen bevorzugen.
- Nur notwendige Änderungen durchführen.

---

## ChatGPT Projects

Für jedes Softwareprojekt sollte ein eigenes Projekt angelegt werden.

Dort können hinterlegt werden:

- Projektanweisungen
- README
- Architektur
- Sicherheitsrichtlinien
- weitere Dokumentation

Empfohlene Struktur:

```text
Project

├── Instructions
├── README.md
├── architecture.md
├── security.md
└── testing.md
```

---

# Einrichtung für Codex

Codex verwendet anstelle von `CLAUDE.md` eine Datei namens

```text
AGENTS.md
```

Empfohlene Struktur:

```text
project/

├── AGENTS.md
├── CLAUDE.md
├── README.md
├── docs/
└── src/
```

Damit können sowohl Claude Code als auch Codex dasselbe Repository verwenden.

---

# Empfohlene Repository-Struktur

```text
project/

├── AGENTS.md
├── CLAUDE.md
├── README.md
├── docs/
│   ├── architecture.md
│   ├── security.md
│   ├── testing.md
│   └── deployment.md
├── src/
└── tests/
```

---

# Was gehört wohin?

| Information | Global | Projekt |
|------------|:------:|:--------:|
| Sprache | ✅ | |
| Kommunikationsstil | ✅ | |
| Transparenz | ✅ | |
| Einfache Lösungen | ✅ | |
| Sicherheitsprinzipien | ✅ | |
| Frameworks | | ✅ |
| Architektur | | ✅ |
| Build-Befehle | | ✅ |
| Testbefehle | | ✅ |
| Deployment | | ✅ |
| Coding Standards | | ✅ |
| Definition of Done | | ✅ |
| Lokale Testserver | | Persönlich |

---

# Empfehlung

Für den täglichen Einsatz empfiehlt sich folgende Struktur:

```text
Benutzer

├── ChatGPT Custom Instructions
└── ~/.claude/CLAUDE.md

Repositories

├── AGENTS.md
├── CLAUDE.md
├── README.md
└── docs/
```

Die globale Konfiguration bleibt bewusst kurz und beschreibt ausschließlich die persönliche Arbeitsweise.

Alle projektspezifischen Informationen gehören in das Repository und werden gemeinsam versioniert.

---

# Best Practices

- Eine KI sollte niemals Projektwissen erraten.
- Projektregeln gehören ins Repository.
- Globale Regeln möglichst kurz halten.
- Änderungen sollten möglichst klein bleiben.
- Annahmen immer kennzeichnen.
- Tests nach Änderungen durchführen.
- Nicht verifizierbare Aussagen ausdrücklich nennen.
- Zusätzliche Verbesserungen als Empfehlung kennzeichnen und nicht ungefragt umsetzen.

---

# Fazit

Eine klare Trennung zwischen **globalen Regeln**, **Projektregeln** und **Dokumentation** reduziert Fehlinterpretationen deutlich.

Diese Struktur funktioniert gleichermaßen mit:

- ChatGPT
- ChatGPT Codex
- Claude
- Claude Code

und lässt sich problemlos auf Teams und mehrere Projekte skalieren.
