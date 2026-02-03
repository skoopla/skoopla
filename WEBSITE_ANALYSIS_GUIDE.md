# Website Analysis Guide: umzug-helden.at

## Anleitung für die Chrome DevTools Analyse

### Schritt 1: Chrome DevTools öffnen
1. Öffne https://www.umzug-helden.at in Google Chrome
2. Drücke `F12` oder `Ctrl+Shift+I` (Windows/Linux) bzw. `Cmd+Option+I` (Mac)
3. Die DevTools öffnen sich am rechten oder unteren Rand

### Schritt 2: Console Errors prüfen
1. Gehe zum **Console** Tab in den DevTools
2. Aktualisiere die Seite (`F5` oder `Ctrl+R`)
3. Notiere alle Fehler (rot) und Warnungen (gelb)
4. Für jeden Fehler dokumentiere:
   - Fehlermeldung
   - Datei und Zeilennummer
   - Stack Trace (falls verfügbar)

### Schritt 3: CSS/Design Probleme identifizieren
Prüfe folgende Bereiche:

#### Layout & Responsiveness
- [ ] Teste verschiedene Bildschirmgrößen (Responsive Mode: `Ctrl+Shift+M`)
  - Mobile (375px)
  - Tablet (768px)
  - Desktop (1920px)
- [ ] Prüfe auf Overflow-Probleme (Elemente die über den Rand hinausgehen)
- [ ] Prüfe Scrolling-Verhalten

#### Visuelles Design
- [ ] Schriftarten laden korrekt
- [ ] Farben sind konsistent
- [ ] Abstände/Margins sind korrekt
- [ ] Bilder laden und werden richtig angezeigt
- [ ] Buttons und interaktive Elemente funktionieren

#### Performance Tab
1. Gehe zum **Performance** Tab
2. Klicke auf "Record" und interagiere mit der Seite
3. Stoppe die Aufnahme
4. Prüfe auf:
   - Layout Shifts (CLS)
   - Lange Tasks
   - Rendering-Probleme

### Schritt 4: Network Tab
1. Gehe zum **Network** Tab
2. Aktualisiere die Seite
3. Prüfe auf:
   - [ ] Fehlgeschlagene Requests (rot)
   - [ ] Langsame Requests (>1s)
   - [ ] Große Dateien (>1MB)
   - [ ] 404 Errors
   - [ ] CORS Errors

### Schritt 5: Elements Tab - CSS Debugging
1. Gehe zum **Elements** Tab
2. Inspiziere problematische Elemente
3. Im **Styles** Panel rechts:
   - Prüfe durchgestrichene CSS-Regeln (überschrieben)
   - Prüfe auf `!important` Overrides
   - Prüfe berechnete Styles im **Computed** Tab
4. Notiere CSS-Konflikte und Probleme

## Report Template

Fülle das folgende Template aus und speichere es in `ANALYSIS_REPORT.md`
