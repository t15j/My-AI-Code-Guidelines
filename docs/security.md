# Security Guidelines

Diese Datei definiert die sicherheitsrelevanten Mindestanforderungen des Projekts. Projektspezifische Anforderungen und Schutzbedarfe müssen ergänzt werden.

## Grundprinzipien

- Secure by Default
- Least Privilege
- Defense in Depth
- Fail Secure
- Minimierung von Daten, Berechtigungen und Angriffsfläche
- Nachvollziehbare und überprüfbare Sicherheitsentscheidungen

## Secrets und Zugangsdaten

- Keine Passwörter, Tokens, API Keys, Zertifikatsschlüssel oder Connection Strings im Repository speichern.
- Secrets über geeignete Secret Stores, geschützte Umgebungsvariablen oder Plattformmechanismen bereitstellen.
- Beispielkonfigurationen ausschließlich mit erkennbaren Platzhaltern veröffentlichen.
- Secrets nicht in Logs, Fehlermeldungen, Screenshots oder Testdaten ausgeben.
- Bei versehentlicher Veröffentlichung ist das Secret zu widerrufen beziehungsweise zu rotieren; das bloße Löschen aus Git reicht nicht aus.

## Authentifizierung und Autorisierung

- Autorisierung serverseitig beziehungsweise an der vertrauenswürdigen Systemgrenze durchsetzen.
- Berechtigungen standardmäßig verweigern und explizit freigeben.
- Technische Konten auf den erforderlichen Umfang begrenzen.
- Keine Sicherheitsentscheidungen allein anhand von UI-Zuständen oder Clientdaten treffen.

## Eingaben und Ausgaben

- Externe Eingaben an der Systemgrenze validieren.
- Kontextgerechtes Encoding und parametrisierte Abfragen verwenden.
- Dateipfade, Uploads, URLs und Deserialisierung besonders prüfen.
- Sensible Informationen in Fehlermeldungen und API-Antworten vermeiden.

## Transport und Kryptografie

- TLS- und Zertifikatsprüfung nicht deaktivieren.
- Etablierte Bibliotheken und Plattformfunktionen verwenden; keine eigene Kryptografie entwickeln.
- Unsichere Protokolle, Algorithmen oder veraltete Cipher vermeiden.
- Schlüsselrotation und Zertifikatsablauf im Betrieb berücksichtigen.

## Logging und Datenschutz

- Nur für Betrieb, Audit oder Fehleranalyse erforderliche Daten protokollieren.
- Personenbezogene und vertrauliche Daten minimieren oder pseudonymisieren.
- Aufbewahrung, Zugriffsschutz und Löschung von Logs definieren.
- Sicherheitsrelevante Ereignisse nachvollziehbar erfassen, ohne Secrets zu protokollieren.

## Abhängigkeiten und Lieferkette

- Abhängigkeiten auf bekannte Schwachstellen und Lizenzrisiken prüfen.
- Versionen reproduzierbar festlegen, sofern das Ökosystem dies vorsieht.
- Update- und Patchprozess dokumentieren.
- Installationsskripte und Build-Abhängigkeiten nicht ungeprüft ausführen.

## Sicherheitsprüfung bei Änderungen

Mindestens prüfen:

- Werden neue Daten verarbeitet oder gespeichert?
- Entstehen neue externe Schnittstellen oder Vertrauensgrenzen?
- Werden Berechtigungen erweitert?
- Werden neue Abhängigkeiten eingeführt?
- Können Eingaben zu Injection, Path Traversal, SSRF oder unsicherer Deserialisierung führen?
- Verändert sich Logging oder Fehlerausgabe?

## Projektspezifischer Schutzbedarf

| Bereich | Einstufung / Vorgabe |
|---|---|
| Vertraulichkeit | <!-- ergänzen --> |
| Integrität | <!-- ergänzen --> |
| Verfügbarkeit | <!-- ergänzen --> |
| Personenbezogene Daten | <!-- ja/nein und Kategorien --> |
| Regulatorische Anforderungen | <!-- ergänzen --> |
| Zulässige Betriebsumgebungen | <!-- ergänzen --> |

## Sicherheitsausnahmen

Abweichungen müssen dokumentiert, begründet, zeitlich begrenzt und mit kompensierenden Maßnahmen versehen werden.
