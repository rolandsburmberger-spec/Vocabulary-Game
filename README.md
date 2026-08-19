# 👹 Vokabel gegen die Monster-Lehrer

Ein Vokabeltrainer als Arcade-Spiel: Lustige Lehrermonster greifen an – **Mr. Grammargh** (Englisch), **Madame Ohlala** (Französisch), **Señor Subjuntivo** (Spanisch) – und alle 4 Wellen wartet **DER DIREKTOR** als Boss. Tippe die gesuchte Vokabel, bevor der Lehrer dein Pult erreicht!

Alles steckt in einer einzigen Datei (`index.html`), läuft auf Handy und PC und braucht keinen Server.

## Spielen

- **Sofort:** `index.html` herunterladen und doppelklicken (öffnet im Browser).
- **Online / auf dem Handy:** In den Repo-Einstellungen GitHub Pages aktivieren
  (*Settings → Pages → Deploy from a branch → `main` / root*).
  Danach läuft das Spiel unter
  `https://rolandsburmberger-spec.github.io/Vocabulary-Game/`.

## Features

- **3 eingebaute Sprachen** (Englisch, Französisch, Spanisch) mit Starter-Vokabeln
- **Abfragerichtung wählbar:** Deutsch → Fremdsprache, Fremdsprache → Deutsch oder gemischt
- **Arcade-Mechanik:** Zeitdruck, 3 Leben, Combos, Punkte, Wellen, Boss-Kämpfe, Rekorde
- **Faire Antwortprüfung:** Groß-/Kleinschreibung egal, Artikel optional (*dog* = *the dog*),
  mehrere Lösungen per `/` (*laufen/rennen*), Akzente standardmäßig tolerant (*é* = *e*, umschaltbar)
- **Eigene Vokabellisten:**
  - von Hand eintippen
  - als Text einfügen (`englisch – deutsch`, eine Vokabel pro Zeile)
  - 📸 **per Foto vom Vokabelbuch**: Texterkennung (Tesseract.js) läuft komplett im Browser,
    nichts wird hochgeladen; erkannte Paare werden vor der Übernahme zur Kontrolle angezeigt
- **Lernhilfe:** Nach jedem Spiel eine Liste der Vokabeln, die du verfehlt hast
- Speicherung (Listen, Rekorde, Einstellungen) per `localStorage` direkt im Browser

## Technik

Vanilla HTML/CSS/JS, Monster als Inline-SVG, Sound per WebAudio (keine Audiodateien).
Nur für den Foto-Scan wird einmalig Tesseract.js von einem CDN nachgeladen – der Rest
funktioniert auch offline.
