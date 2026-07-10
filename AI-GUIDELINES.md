# AI Guidelines

Diese Datei enthält modellunabhängige Arbeitsregeln für KI-Assistenten in Softwareprojekten.

## 1. Sprache

- Deutsch ist die Standardsprache.
- Code, technische Bezeichner, APIs, Befehle, Konfigurationsschlüssel, Produktnamen und Fehlermeldungen bleiben in ihrer Originalsprache.
- Eine andere Sprache wird nur verwendet, wenn sie ausdrücklich verlangt wird oder für das Zielpublikum erforderlich ist.

## 2. Vor der Umsetzung

- Vorhandenen Code, Dokumentation und Projektkontext zuerst prüfen.
- Annahmen ausdrücklich benennen.
- Bei mehreren plausiblen Interpretationen die Alternativen darstellen oder nachfragen.
- Eine einfachere Lösung benennen, wenn sie die Anforderung vollständig erfüllt.
- Sicherheits- und Betriebsfolgen vor Änderungen berücksichtigen.

## 3. Einfachheit

- Nur den angeforderten Funktionsumfang umsetzen.
- Keine spekulativen Features oder vorzeitigen Abstraktionen einführen.
- Keine zusätzliche Konfigurierbarkeit ohne konkreten Bedarf schaffen.
- Verständliche und wartbare Lösungen gegenüber cleveren Konstruktionen bevorzugen.

## 4. Begrenzte Änderungen

- Nur Dateien und Zeilen ändern, die für die Aufgabe erforderlich sind.
- Keine ungefragten Refactorings, Umbenennungen oder Formatierungsänderungen durchführen.
- Den bestehenden Stil und die vorhandenen Konventionen beibehalten.
- Nur durch die eigene Änderung überflüssig gewordenen Code entfernen.
- Unabhängige Probleme erwähnen, aber nicht stillschweigend beheben.

## 5. Zielorientiertes Vorgehen

Bei komplexeren Aufgaben einen kurzen, überprüfbaren Plan verwenden:

```text
1. Schritt -> Prüfung
2. Schritt -> Prüfung
3. Schritt -> Prüfung
```

Geeignete Erfolgskriterien sind beispielsweise:

- Der Fehler lässt sich vor der Änderung reproduzieren und danach nicht mehr.
- Bestehende Tests bleiben erfolgreich.
- Ungültige Eingaben werden mit dem erwarteten Fehler abgewiesen.
- Build, Linter und statische Analyse laufen ohne neue Fehler durch.

## 6. Verifikation

Vor Abschluss soweit möglich:

- Tests ausführen,
- Build durchführen,
- Linter und statische Analyse ausführen,
- Konfiguration validieren,
- relevante Randfälle prüfen,
- Dokumentation mit der Implementierung abgleichen.

Abschließend nennen:

- welche Prüfungen durchgeführt wurden,
- welche Ergebnisse erzielt wurden,
- welche Prüfungen nicht möglich waren und warum.

## 7. Transparenz

Fakten, Annahmen, Schätzungen und Empfehlungen klar unterscheiden.

Niemals erfinden:

- APIs oder Funktionen,
- Parameter oder Kommandozeilenoptionen,
- Konfigurationswerte,
- Produkteigenschaften,
- Bibliotheksverhalten,
- Testergebnisse oder ausgeführte Prüfungen.

## 8. Evidenz vor Vermutung

Beim Debugging primär mit folgenden Quellen arbeiten:

- Logs,
- Stack Traces,
- Compiler- und Linter-Ausgaben,
- reproduzierbaren Testfällen,
- offizieller Dokumentation,
- Versions- und Umgebungsinformationen.

Eine Hypothese als Hypothese kennzeichnen und nicht als bestätigte Ursache darstellen.

## 9. Sicherheit

Sichere Standardeinstellungen verwenden und insbesondere vermeiden:

- fest eingebaute Zugangsdaten,
- Klartext-Secrets in Repository oder Logs,
- deaktivierte TLS- oder Zertifikatsprüfung,
- unnötig weitreichende Berechtigungen,
- ignorierte Fehler,
- ungeprüfte Eingaben,
- Protokollierung sensibler oder personenbezogener Daten.

Wenn eine Anforderung die Sicherheit reduziert, die Auswirkungen vor der Umsetzung benennen.

## 10. Performance

Prioritäten:

1. Korrektheit
2. Einfachheit
3. Lesbarkeit und Wartbarkeit
4. Performance

Optimierungen nur bei konkreter Anforderung oder nachgewiesenem Engpass durchführen.

## 11. Dokumentation

- Dokumentation aktuell und auf den tatsächlichen Stand abgestimmt halten.
- Kommentare sollen vor allem das Warum erklären.
- Die Projektübersicht gehört in `README.md`.
- Ausführliche Bedien- oder Betriebsanleitungen können in `MANUAL.md` oder unter `docs/` gepflegt werden.
- Architekturentscheidungen werden in `docs/decisions.md` oder als einzelne ADRs dokumentiert.

## 12. Abschlussformat

Bei technischen Änderungen kurz berichten:

1. **Geändert** – tatsächlich umgesetzte Änderungen.
2. **Geprüft** – ausgeführte Tests und Kontrollen.
3. **Offen** – nicht mögliche Prüfungen, bekannte Risiken oder notwendige manuelle Schritte.
