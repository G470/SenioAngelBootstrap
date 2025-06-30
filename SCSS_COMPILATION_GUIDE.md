# SCSS-Kompilierung mit Cursor AI - Anleitung

## 🎯 Empfohlene Erweiterungen für Cursor AI

### Haupt-Erweiterungen für SCSS-Kompilierung:

1. **Live Sass Compiler** (`glenn2223.live-sass`)
   - Kompiliert SCSS automatisch beim Speichern
   - Generiert CSS und Source Maps
   - Unterstützt verschiedene Ausgabeformate

2. **Live Server** (`ritwickdey.LiveServer`)
   - Startet einen lokalen Entwicklungsserver
   - Automatisches Neuladen bei Änderungen
   - Perfekt für die Vorschau

3. **Sass** (`syler.sass-indented`)
   - Syntax-Highlighting für SCSS/Sass
   - IntelliSense und Autocomplete
   - Fehlerdiagnose

### Zusätzliche nützliche Erweiterungen:

4. **Prettier** (`esbenp.prettier-vscode`)
   - Automatische Code-Formatierung
   - Unterstützt SCSS/CSS

5. **CSS Peek** (`pranaygp.vscode-css-peek`)
   - Schnelle Navigation zu CSS-Definitionen
   - Hilft bei der SCSS-Struktur

6. **Path Intellisense** (`christian-kohler.path-intellisense`)
   - Autocomplete für Dateipfade
   - Nützlich für @import-Statements

## ⚙️ Konfiguration

### Automatische Installation:
1. Öffnen Sie das Projekt in Cursor AI
2. Cursor wird automatisch die empfohlenen Erweiterungen vorschlagen
3. Klicken Sie auf "Install All" in der Benachrichtigung

### Manuelle Installation:
```bash
# Öffnen Sie die Command Palette (Cmd+Shift+P)
# Tippen Sie: "Extensions: Install Extensions"
# Suchen Sie nach den oben genannten Erweiterungen
```

## 🚀 Verwendung

### Automatische Kompilierung:
1. Die **Live Sass Compiler**-Erweiterung startet automatisch
2. Änderungen in `scss/bootstrap.scss` werden automatisch kompiliert
3. CSS-Dateien werden in `/build/css/` gespeichert

### Manuelle Build-Befehle:
```bash
# Einmalige Kompilierung
npm run build

# Minifizierte Version
npm run build:min

# Watch-Modus (kontinuierliche Kompilierung)
npm run watch

# Entwicklungsserver starten
npm run serve
```

### VS Code/Cursor Tasks:
1. Öffnen Sie die Command Palette (Cmd+Shift+P)
2. Tippen Sie: "Tasks: Run Task"
3. Wählen Sie:
   - "Build SCSS" für normale Kompilierung
   - "Build SCSS Minified" für minifizierte Version
   - "Watch SCSS" für kontinuierliche Überwachung

## 📁 Ausgabestruktur

Nach der Kompilierung finden Sie folgende Dateien in `/build/css/`:

```
build/css/
├── bootstrap.css          # Normale CSS-Datei
├── bootstrap.css.map      # Source Map für Debugging
├── bootstrap.min.css      # Minifizierte CSS-Datei
└── bootstrap.min.css.map  # Source Map für minifizierte Version
```

## 🔧 Einstellungen anpassen

### Live Sass Compiler Einstellungen:
```json
{
  "liveSassCompile.settings.formats": [
    {
      "format": "expanded",
      "extensionName": ".css",
      "savePath": "/build/css"
    },
    {
      "format": "compressed",
      "extensionName": ".min.css",
      "savePath": "/build/css"
    }
  ],
  "liveSassCompile.settings.autoprefix": [
    "> 1%",
    "last 2 versions"
  ],
  "liveSassCompile.settings.generateMap": true
}
```

## 🐛 Troubleshooting

### Häufige Probleme:

1. **Erweiterung startet nicht automatisch:**
   - Öffnen Sie eine SCSS-Datei
   - Drücken Sie Cmd+Shift+P und tippen Sie "Live Sass: Watch Sass"

2. **CSS wird nicht generiert:**
   - Überprüfen Sie die Konsolenausgabe
   - Stellen Sie sicher, dass der `/build/css/`-Ordner existiert

3. **Source Maps funktionieren nicht:**
   - Aktivieren Sie "Generate Map" in den Einstellungen
   - Überprüfen Sie die Browser-Entwicklertools

### Debugging:
```bash
# Überprüfen Sie die Sass-Version
sass --version

# Testen Sie die Kompilierung manuell
sass scss/bootstrap.scss:build/css/test.css

# Überprüfen Sie die Ausgabe
ls -la build/css/
```

## 📚 Nützliche Befehle

### Cursor AI Shortcuts:
- `Cmd+Shift+P`: Command Palette
- `Cmd+Shift+X`: Extensions Panel
- `Cmd+,`: Settings
- `Cmd+Shift+B`: Build Task ausführen

### Terminal-Befehle:
```bash
# Abhängigkeiten installieren
npm install

# Entwicklungsumgebung starten
npm run dev

# Produktions-Build
npm run build:min

# Ordner bereinigen
npm run clean
```

## 🎉 Erfolgreiche Einrichtung

Nach der Einrichtung sollten Sie:
- ✅ Automatische SCSS-Kompilierung beim Speichern
- ✅ CSS-Dateien in `/build/css/`
- ✅ Source Maps für Debugging
- ✅ Live Server für die Vorschau
- ✅ Syntax-Highlighting und IntelliSense

Ihr SCSS-Workflow ist jetzt vollständig eingerichtet! 🚀 