# HTML, CSS und JavaScript Guidelines

## HTML

- Semantische Elemente verwenden.
- Formularelemente mit eindeutigen Labels versehen.
- Interaktive Elemente mit nativen HTML-Elementen statt nachgebauten `div`-Konstruktionen umsetzen.
- Überschriftenhierarchie nachvollziehbar halten.
- Inhalte und Funktionen auch ohne rein visuelle Hinweise verständlich machen.

## CSS

- Bestehendes Designsystem und vorhandene Namenskonventionen beibehalten.
- Layout mit Flexbox oder Grid statt positionsbasierten Workarounds umsetzen.
- Spezifität niedrig halten und `!important` nur mit dokumentiertem Grund verwenden.
- Wiederkehrende Werte über bestehende Variablen oder Tokens steuern.
- Responsive Verhalten und sichtbare Fokuszustände berücksichtigen.
- Keine globalen Stiländerungen für ein lokales Problem einführen.

## JavaScript

- Bestehenden Projektstil und unterstützte Runtime-Versionen beachten.
- `const` standardmäßig, `let` bei notwendiger Neuzuweisung verwenden.
- DOM-Eingaben und externe Daten nicht als vertrauenswürdig behandeln.
- Nutzerinhalte nicht ungeprüft über `innerHTML` einsetzen.
- Asynchrone Fehler gezielt behandeln.
- Globale Zustände und direkte Kopplung zwischen Komponenten minimieren.
- Keine neue Bibliothek einführen, wenn die Plattformfunktion die Anforderung einfach erfüllt.

## Sicherheit

- Kontextgerechtes Output Encoding verwenden.
- Content Security Policy und bestehende Sicherheitsheader nicht umgehen.
- Tokens oder vertrauliche Konfiguration nicht im Browser ausliefern.
- Clientseitige Validierung nur als Ergänzung; verbindliche Validierung an der vertrauenswürdigen Systemgrenze durchführen.
- Externe Skripte und Ressourcen nur aus freigegebenen Quellen einbinden.

## Qualität

- Kritische UI-Abläufe mit geeigneten Tests absichern.
- Browserkonsole auf neue Fehler prüfen.
- Tastaturbedienung und relevante Viewports manuell oder automatisiert prüfen.
- Vorgaben aus `ui-guidelines.md` einhalten.
