# Website Analysis Report: umzug-helden.at

**Datum:** [DATUM EINFÜGEN]
**Analysiert von:** [DEIN NAME]
**Browser:** Chrome [VERSION]
**Ziel:** CSS-Probleme für Claude Opus 4.5 dokumentieren

---

## 1. Console Errors & Warnings

### JavaScript Errors
```
[Hier Console Errors einfügen - Format: Fehlertyp, Datei:Zeile, Nachricht]

Beispiel:
❌ TypeError: Cannot read property 'x' of undefined
   at main.js:145
   Stack: ...
```

### Warnungen
```
[Hier Warnungen einfügen]

Beispiel:
⚠️ Deprecated API usage in analytics.js:23
```

### Network Errors
```
[Fehlgeschlagene Requests]

Beispiel:
❌ 404 - /assets/missing-image.png
❌ Failed to load resource: net::ERR_CONNECTION_REFUSED
```

---

## 2. CSS & Design Probleme

### 2.1 Layout Probleme

#### Desktop (1920px)
- [ ] Problem 1: [Beschreibung]
  - **Betroffenes Element:** [CSS Selector, z.B. `.header .navigation`]
  - **Aktuelles Verhalten:** [Was ist falsch?]
  - **Erwartetes Verhalten:** [Was sollte passieren?]
  - **Screenshot:** [Optional: Screenshot-Link]

#### Tablet (768px)
- [ ] Problem 1: [Beschreibung]
  - **Betroffenes Element:**
  - **Aktuelles Verhalten:**
  - **Erwartetes Verhalten:**

#### Mobile (375px)
- [ ] Problem 1: [Beschreibung]
  - **Betroffenes Element:**
  - **Aktuelles Verhalten:**
  - **Erwartetes Verhalten:**

### 2.2 CSS Konflikte & Specificity Probleme

```css
/* Dokumentiere hier CSS-Regeln die sich gegenseitig überschreiben */

Beispiel:
/* Problem: Button hat falsche Farbe */
.button {
  background: blue; /* Diese Regel wird überschrieben */
}

.header .button {
  background: red !important; /* Überschreibt obige Regel */
}

/* Lösung benötigt: ... */
```

### 2.3 Overflow & Scrolling Probleme

- [ ] **Horizontaler Overflow:** [Ja/Nein]
  - Betroffene Bereiche: [Elemente auflisten]
  - Ursache: [z.B. feste Breiten, fehlende max-width]

- [ ] **Vertikaler Overflow:** [Ja/Nein]
  - Betroffene Bereiche:
  - Ursache:

### 2.4 Typographie Probleme

- [ ] **Schriftarten laden nicht:** [Liste]
- [ ] **Lesbarkeit:** [Probleme mit Kontrast, Größe, Zeilenhöhe]
- [ ] **Font-Rendering:** [Probleme mit Antialiasing, etc.]

### 2.5 Spacing & Alignment

```
[Dokumentiere Abstands- und Ausrichtungsprobleme]

Beispiel:
- Header padding ist auf Mobile zu groß (aktuell: 40px, sollte: 20px)
- Footer Elemente sind nicht vertikal zentriert
- Inkonsistente margins zwischen Sektionen
```

### 2.6 Farben & Kontraste

- [ ] **WCAG Kontrast-Probleme:** [Liste]
  - Element: [Selector]
  - Aktueller Kontrast: [Ratio]
  - Mindest-Anforderung: [z.B. 4.5:1 für AA]

### 2.7 Bilder & Medien

- [ ] **Fehlende Bilder:** [Liste der 404s]
- [ ] **Bildgrößen-Probleme:** [Zu groß, verzerrt, etc.]
- [ ] **Lazy Loading Probleme:** [Falls vorhanden]

### 2.8 Interaktive Elemente

#### Buttons
- [ ] **Hover States:** [Funktionieren/Fehlen]
- [ ] **Active States:** [Funktionieren/Fehlen]
- [ ] **Focus States:** [Funktionieren/Fehlen - wichtig für Accessibility]

#### Forms
- [ ] **Input Styling:** [Probleme]
- [ ] **Validation States:** [Probleme]
- [ ] **Placeholder Text:** [Lesbarkeit]

#### Navigation
- [ ] **Menu Verhalten:** [Probleme]
- [ ] **Dropdown Styling:** [Probleme]
- [ ] **Mobile Menu:** [Probleme]

---

## 3. Performance Metriken

```
[Chrome DevTools > Performance Tab Ergebnisse]

Largest Contentful Paint (LCP): [X]s (Ziel: <2.5s)
First Input Delay (FID): [X]ms (Ziel: <100ms)
Cumulative Layout Shift (CLS): [X] (Ziel: <0.1)

Layout Shifts detected:
- [Wo und warum]

Long Tasks (>50ms):
- [Liste]
```

---

## 4. Accessibility (a11y) Probleme

- [ ] **Fehlende Alt-Texte:** [Anzahl]
- [ ] **Kontrast-Probleme:** [Liste]
- [ ] **Keyboard Navigation:** [Probleme]
- [ ] **ARIA Labels:** [Fehlend/Falsch]
- [ ] **Focus Indicators:** [Sichtbar/Unsichtbar]

---

## 5. Browser Compatibility

Getestet in:
- [ ] Chrome [Version]: [Status]
- [ ] Firefox: [Status]
- [ ] Safari: [Status]
- [ ] Edge: [Status]

Browser-spezifische Probleme:
```
[Liste der Probleme die nur in bestimmten Browsern auftreten]
```

---

## 6. Prioritisierte CSS-Probleme für Claude Opus 4.5

### 🔴 CRITICAL (Sofort beheben)

**Problem 1:** [Titel]
```css
/* Aktueller Code */
[Problematischer CSS Code]

/* Problem */
[Detaillierte Beschreibung was falsch ist]

/* Erwartetes Verhalten */
[Was sollte passieren]

/* Betroffene Dateien */
- /path/to/file.css (Zeile XX)
- /path/to/component.css (Zeile YY)

/* Reproduktion */
1. [Schritte zum Reproduzieren]
2. ...

/* Screenshots/Videos */
[Links einfügen]
```

### 🟡 HIGH (Wichtig)

**Problem 2:** [Titel]
[Gleiche Struktur wie oben]

### 🟢 MEDIUM (Kann warten)

**Problem 3:** [Titel]
[Gleiche Struktur wie oben]

### ⚪ LOW (Nice to have)

**Problem 4:** [Titel]
[Gleiche Struktur wie oben]

---

## 7. Technischer Context für Claude Opus 4.5

### CSS Framework/Libraries
- [ ] Framework: [z.B. Bootstrap, Tailwind, Custom]
- [ ] Version: [X.X.X]
- [ ] CSS Preprocessor: [SASS/LESS/PostCSS/None]

### CSS Architektur
```
[Beschreibe die CSS Struktur]

Beispiel:
/styles
  /components
  /layouts
  /utilities
  /variables
  main.css
```

### Browser Support Anforderungen
```
[Welche Browser/Versionen müssen unterstützt werden?]

Beispiel:
- Chrome: letzte 2 Versionen
- Firefox: letzte 2 Versionen
- Safari: 12+
- IE11: Nein
```

### Besondere Anforderungen
```
[Gibt es besondere Requirements?]

Beispiel:
- Muss responsive sein (Mobile First)
- Dark Mode Support benötigt
- RTL (Right-to-Left) Support
- Print Stylesheet benötigt
```

---

## 8. Empfohlener Aktionsplan

### Schritt 1: Critical Fixes
```
1. [Problem beheben]
2. [Problem beheben]
```

### Schritt 2: High Priority
```
1. [Problem beheben]
2. [Problem beheben]
```

### Schritt 3: Optimierungen
```
1. [Verbesserung]
2. [Verbesserung]
```

### Schritt 4: Testing
```
- Cross-browser testing
- Responsive testing
- Performance testing
- Accessibility audit
```

---

## 9. Zusätzliche Notizen

```
[Alle weiteren Beobachtungen, die nicht in die obigen Kategorien passen]
```

---

## 10. Claude Opus 4.5 Prompt Template

**Verwende diesen Prompt wenn du den Report an Claude Opus 4.5 gibst:**

```
Ich habe eine detaillierte Analyse der Website umzug-helden.at durchgeführt
und CSS-Probleme identifiziert. Bitte lies den folgenden Report und behebe
die CRITICAL und HIGH priority CSS-Probleme.

[ANALYSIS_REPORT.md Content hier einfügen]

Bitte:
1. Analysiere alle dokumentierten CSS-Probleme
2. Erstelle Lösungen für die Critical und High Priority Probleme
3. Zeige mir den korrigierten CSS-Code
4. Erkläre was du geändert hast und warum
5. Gib Empfehlungen für Best Practices

Beginne mit den Critical Problemen.
```

---

**Report erstellt:** [TIMESTAMP]
**Analysedauer:** [XX Minuten]
