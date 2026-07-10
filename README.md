My AI Code Guidelines

Meine konkrete Empfehlung

Für deine Nutzung würde ich folgende Struktur wählen:

Benutzerweit
├── AI Custom Instructions
└── ~/.claude/CLAUDE.md

Pro Repository
├── CLAUDE.md
├── AGENTS.md
├── README.md
└── docs/
    ├── architecture.md
    ├── security.md
    └── testing.md

Dabei gilt:

Inhalt	Speicherort
Deutsch als Standardsprache	globale Anweisungen
Kommunikationsstil	globale Anweisungen
Vorsicht, Transparenz, einfache Lösungen	global und verkürzt im Projekt
Architektur und Technologie	Repository
Test- und Buildbefehle	Repository
Sicherheitsanforderungen	Repository
Lokale URLs oder persönliche Testdaten	CLAUDE.local.md, nicht in Git
Teamweite Regeln	versionierte CLAUDE.md und AGENTS.md
Umfangreiche Dokumentation	separate Dateien unter docs/
