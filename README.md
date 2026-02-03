# Website Analysis Toolkit für umzug-helden.at

Dieses Repository enthält Tools und Templates zur systematischen Analyse von Website-Problemen, speziell CSS- und Design-Issues, mit Chrome DevTools.

## 📋 Übersicht

Das Projekt enthält:
- **Detaillierte Analyse-Anleitung** für Chrome DevTools
- **Strukturierte Report-Templates** für konsistente Dokumentation
- **Priorisierungs-Framework** für gefundene Probleme
- **Claude Opus 4.5 Integration** für automatisierte CSS-Fixes
- **Übungs-Seite** zum Trainieren der DevTools-Analyse

## 🚀 Quick Start

1. **Start hier:** [`QUICK_START.md`](QUICK_START.md)
   - 5-Minuten Schnellanleitung
   - Alle wichtigen Schritte auf einen Blick

2. **Detaillierte Anleitung:** [`WEBSITE_ANALYSIS_GUIDE.md`](WEBSITE_ANALYSIS_GUIDE.md)
   - Schritt-für-Schritt Anweisungen
   - Chrome DevTools Tutorial
   - Best Practices

3. **Report Template:** [`ANALYSIS_REPORT.md`](ANALYSIS_REPORT.md)
   - Strukturiertes Template zum Ausfüllen
   - Vordefinierte Kategorien
   - Priorisierungs-Schema
   - Claude Opus 4.5 Prompt Template

4. **Übungs-Seite:** [`test-page.html`](test-page.html)
   - HTML-Datei mit absichtlichen CSS/JS-Fehlern
   - Perfekt zum Üben der DevTools-Analyse
   - Öffne einfach im Browser

## 📁 Dateien

```
skoopla/
├── README.md                      # Diese Datei
├── QUICK_START.md                 # 5-Min Schnellstart
├── WEBSITE_ANALYSIS_GUIDE.md      # Detaillierte Anleitung
├── ANALYSIS_REPORT.md             # Report Template (ausfüllen!)
└── test-page.html                 # Übungs-Seite
```

## 🎯 Workflow

```
1. Chrome DevTools öffnen (F12)
   ↓
2. Website analysieren (siehe WEBSITE_ANALYSIS_GUIDE.md)
   ↓
3. Findings dokumentieren (in ANALYSIS_REPORT.md)
   ↓
4. Probleme priorisieren (Critical → High → Medium → Low)
   ↓
5. Report an Claude Opus 4.5 senden
   ↓
6. CSS-Fixes erhalten und testen
```

## 🔍 Was wird analysiert?

### Console Errors
- JavaScript Fehler
- Warnungen
- Network Errors (404, CORS, etc.)

### CSS/Design Probleme
- Layout Issues (Desktop/Tablet/Mobile)
- Responsiveness
- CSS Konflikte & Specificity
- Overflow & Scrolling
- Typographie
- Spacing & Alignment
- Farben & Kontraste
- Bilder & Medien
- Interaktive Elemente (Buttons, Forms, Navigation)

### Performance
- Largest Contentful Paint (LCP)
- First Input Delay (FID)
- Cumulative Layout Shift (CLS)
- Layout Shifts
- Long Tasks

### Accessibility
- Alt-Texte
- Kontrast-Verhältnisse
- Keyboard Navigation
- ARIA Labels
- Focus Indicators

## 🛠️ Chrome DevTools Setup

### Option 1: Manuell (Empfohlen für diese Umgebung)
Da Chrome in dieser Docker-Umgebung nicht verfügbar ist:

1. Öffne die Website auf deinem **lokalen Computer**
2. Drücke `F12` für Chrome DevTools
3. Folge der Anleitung in `WEBSITE_ANALYSIS_GUIDE.md`

### Option 2: Mit Chrome DevTools MCP (Lokal)
Falls du Claude Code lokal mit Chrome ausführst:

```bash
# MCP Server installieren
claude mcp add chrome-devtools -- npx -y chrome-devtools-mcp@latest

# Claude mit Chrome starten
claude --chrome

# In der Session:
# "Analysiere https://www.umzug-helden.at"
```

## 📊 Priorisierungs-Schema

### 🔴 CRITICAL
- Layout komplett kaputt
- Buttons nicht klickbar
- Text unleserlich
- Navigation funktioniert nicht

### 🟡 HIGH
- Horizontal Scroll auf Mobile
- Bilder überlappen Text
- Inkonsistente Abstände
- Responsiveness Probleme

### 🟢 MEDIUM
- Kleine Alignment-Probleme
- Suboptimale Margins/Paddings
- Font-Loading Performance

### ⚪ LOW
- Kleine visuelle Inkonsistenzen
- Micro-interactions fehlen

## 🤖 Claude Opus 4.5 Integration

Nach dem Ausfüllen des Reports:

1. Kopiere den kompletten Inhalt von `ANALYSIS_REPORT.md`
2. Verwende den Prompt Template aus Abschnitt 10
3. Sende an Claude Opus 4.5
4. Erhalte strukturierte CSS-Lösungen

**Beispiel Prompt:**
```
Ich habe eine detaillierte Analyse der Website umzug-helden.at
durchgeführt. Bitte behebe die CRITICAL und HIGH priority CSS-Probleme.

[Report einfügen]

Beginne mit den Critical Problemen.
```

## 🎓 Learning Resources

- [Chrome DevTools Docs](https://developer.chrome.com/docs/devtools/)
- [Web Vitals](https://web.dev/vitals/)
- [WCAG Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [CSS Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

## 💡 Pro Tips

1. **Preserve Log** in Console aktivieren (bleibt bei Navigation erhalten)
2. **Screenshots** für Dokumentation: `Ctrl+Shift+P` → "Capture screenshot"
3. **CSS Coverage** checken: `Ctrl+Shift+P` → "Show Coverage"
4. **Lighthouse Audit** für automatische Analyse nutzen
5. **Network Throttling** für Performance-Tests (Fast 3G/Slow 3G)

## 🧪 Übung mit test-page.html

Bevor du die echte Website analysierst, übe mit `test-page.html`:

```bash
# Öffne die Datei im Browser
open test-page.html  # macOS
xdg-open test-page.html  # Linux
start test-page.html  # Windows
```

**Die Seite enthält absichtlich:**
- Console Errors (6 verschiedene)
- CSS Konflikte (!important Probleme)
- Layout Issues (Fixed Width, kein Responsive)
- Overflow Probleme
- 404 Network Errors
- Performance Issues
- Poor Contrast
- Z-Index Probleme

**Challenge:** Finde alle 15+ Probleme und dokumentiere sie im Report!

## 📝 Checkliste

- [ ] `QUICK_START.md` gelesen
- [ ] `test-page.html` im Browser geöffnet
- [ ] DevTools geöffnet (`F12`)
- [ ] Console Errors gefunden
- [ ] CSS Probleme identifiziert
- [ ] Responsive Breakpoints getestet
- [ ] Network Tab geprüft
- [ ] Performance Audit durchgeführt
- [ ] `ANALYSIS_REPORT.md` ausgefüllt
- [ ] Probleme priorisiert
- [ ] Report an Claude Opus 4.5 gesendet

## 🚦 Next Steps

1. **Jetzt:** Übe mit `test-page.html`
2. **Dann:** Analysiere https://www.umzug-helden.at
3. **Dokumentiere:** Fülle `ANALYSIS_REPORT.md` aus
4. **Löse:** Sende Report an Claude Opus 4.5
5. **Teste:** Verifiziere die CSS-Fixes

## ⚙️ Git Branch

Working Branch: `claude/add-view-command-RyTEK`

```bash
# Status checken
git status

# Änderungen committen
git add .
git commit -m "Add website analysis toolkit"

# Pushen
git push -u origin claude/add-view-command-RyTEK
```

---

**Erstellt für:** Website Analysis von umzug-helden.at
**Zweck:** Systematische CSS/Design Problem-Dokumentation
**Tool:** Chrome DevTools + Claude Opus 4.5
