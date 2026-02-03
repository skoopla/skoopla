# Quick Start: Website Analyse für umzug-helden.at

## Schnellanleitung (5 Minuten)

### Option 1: Auf deinem lokalen Computer

Da Chrome in dieser Umgebung nicht verfügbar ist, führe die Analyse auf deinem lokalen Computer durch:

1. **Öffne Chrome und die Website:**
   ```
   https://www.umzug-helden.at
   ```

2. **Chrome DevTools öffnen:**
   - Drücke `F12` (Windows/Linux) oder `Cmd+Option+I` (Mac)

3. **Schnell-Check (5 Minuten):**

   **Console Tab:**
   - Seite neu laden (`F5`)
   - Alle roten Fehler kopieren → In `ANALYSIS_REPORT.md` unter "Console Errors" einfügen

   **Elements Tab:**
   - Rechtsklick auf problematische Bereiche → "Inspect"
   - Im Styles Panel: Suche nach durchgestrichenen CSS-Regeln
   - Notiere CSS-Konflikte

   **Network Tab:**
   - Seite neu laden
   - Filter auf "Errors" (rotes Symbol)
   - Liste alle 404/500 Fehler

   **Responsive Test:**
   - `Ctrl+Shift+M` für Device Mode
   - Teste: Mobile (375px), Tablet (768px), Desktop (1920px)
   - Notiere Breakpoint-Probleme

4. **Report ausfüllen:**
   - Öffne `ANALYSIS_REPORT.md`
   - Fülle die relevanten Abschnitte aus
   - Priorisiere Probleme (Critical/High/Medium/Low)

5. **An Claude Opus 4.5 senden:**
   - Kopiere den ausgefüllten Report
   - Verwende den Prompt Template aus Abschnitt 10
   - Sende an Claude Opus 4.5

---

## Option 2: Mit Chrome DevTools MCP (lokal mit installierten Chrome)

Wenn du Claude Code lokal ausführst und Chrome installiert hast:

1. **MCP Server installieren:**
   ```bash
   claude mcp add chrome-devtools -- npx -y chrome-devtools-mcp@latest
   ```

2. **Claude mit Chrome starten:**
   ```bash
   claude --chrome
   ```

3. **In der Claude Session:**
   ```
   Öffne https://www.umzug-helden.at und analysiere:
   - Alle Console Errors
   - CSS/Design Probleme
   - Network Errors
   - Performance Issues

   Erstelle einen detaillierten Report.
   ```

---

## Dateien in diesem Projekt

- **`WEBSITE_ANALYSIS_GUIDE.md`** - Detaillierte Schritt-für-Schritt Anleitung
- **`ANALYSIS_REPORT.md`** - Template zum Ausfüllen mit deinen Findings
- **`QUICK_START.md`** - Diese Datei (Schnellstart)
- **`README.md`** - Projekt README

---

## Typische CSS-Probleme worauf du achten solltest

### 🔴 Critical
- Layout komplett kaputt auf Mobile
- Wichtige Buttons nicht klickbar/sichtbar
- Text unleserlich (zu klein, falscher Kontrast)
- Navigation funktioniert nicht
- Formular-Inputs nicht nutzbar

### 🟡 High
- Horizontal Scroll auf Mobile
- Bilder überlappen Text
- Inkonsistente Abstände
- Hover States fehlen
- Responsiveness Probleme

### 🟢 Medium
- Kleine Alignment-Probleme
- Suboptimale Margins/Paddings
- Font-Loading Performance
- Animations ruckeln

### ⚪ Low
- Kleine visuelle Inconsistenzen
- Micro-interactions fehlen
- Hover-Effekte könnten smoother sein

---

## Nützliche Chrome DevTools Shortcuts

- `F12` - DevTools öffnen/schließen
- `Ctrl+Shift+M` - Device Mode (Responsive)
- `Ctrl+Shift+C` - Element Picker
- `Ctrl+Shift+P` - Command Menu
  - Type: "Screenshot" für Screenshots
  - Type: "Coverage" für CSS Coverage
- `Esc` - Console drawer toggle

---

## Pro Tips

1. **Screenshots machen:**
   - `Ctrl+Shift+P` → "Capture full size screenshot"
   - Sehr hilfreich um Probleme zu dokumentieren

2. **CSS Coverage prüfen:**
   - `Ctrl+Shift+P` → "Show Coverage"
   - Zeigt ungenutztes CSS (Optimierung möglich)

3. **Lighthouse Audit:**
   - DevTools → "Lighthouse" Tab
   - Automatische Analyse von Performance, Accessibility, SEO

4. **Console Errors persistent machen:**
   - Console → Settings (⚙️) → "Preserve log"
   - Verhindert dass Errors bei Navigation verschwinden

5. **Network Throttling:**
   - Network Tab → "No throttling" → "Fast 3G" oder "Slow 3G"
   - Teste Performance auf langsameren Verbindungen

---

## Nächste Schritte

1. ✅ Analyse durchführen (mit obiger Anleitung)
2. ✅ `ANALYSIS_REPORT.md` ausfüllen
3. ✅ Report an Claude Opus 4.5 senden
4. ⏳ CSS Fixes von Claude Opus 4.5 erhalten
5. ⏳ Fixes testen und verifizieren

---

**Bei Fragen oder Problemen:**
- Siehe `WEBSITE_ANALYSIS_GUIDE.md` für detaillierte Erklärungen
- Chrome DevTools Docs: https://developer.chrome.com/docs/devtools/
