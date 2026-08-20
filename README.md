# 🧟 Vokabel gegen die Zombie-Lehrer (3D)

Ein Vokabeltrainer als 3D-Arcade-Spiel: Untote Lehrer schlurfen durchs nächtliche Klassenzimmer auf dein Pult zu – **Mr. Brainsworth** (Englisch), **Madame Ohlalaaargh** (Französisch), **Señor Muertos** (Spanisch), und alle 4 Wellen wankt **DER DIREKTOR** als Boss heran. Tippe die gesuchte Vokabel, bevor sie dich erwischen!

Alles steckt in einer einzigen Datei (`index.html`) – Three.js ist direkt eingebettet. Läuft auf Handy und PC, braucht keinen Server.

## Spielen

- **Sofort:** `index.html` herunterladen und doppelklicken (öffnet im Browser).
- **Online / auf dem Handy:** In den Repo-Einstellungen GitHub Pages aktivieren
  (*Settings → Pages → Deploy from a branch → `main` / root*).
  Danach läuft das Spiel unter
  `https://rolandsburmberger-spec.github.io/Vocabulary-Game/`.

## Features

- **Echtes 3D** (Three.js): nächtliches Klassenzimmer mit Mondlicht, flackernder Lampe, Nebel und umgekippten Bänken; die Zombie-Position hängt direkt am Antwort-Timer – Balken leer = Zombie am Pult
- **3 eingebaute Sprachen** (Englisch, Französisch, Spanisch) mit **Sprachniveaus A1, A2, B1, B2 und C1** – jedes Niveau mit eigenem Vokabelpaket und eigenen Rekorden
- **4 Modi:** 📝 Abschreiben (Vokabel + Bedeutung stehen da – schnell abtippen, zum ersten Lernen), Deutsch → Fremdsprache, Fremdsprache → Deutsch oder gemischt
- **Schwierigkeitsgrade:** Leicht (mehr Zeit), Normal, Schwer (+30 % Punkte) – eigene Rekorde je Stufe
- **🎓 Trainingsmodus:** keine Leben verlierbar, viel Zeit – zum entspannten Üben (halbe XP, kein Rekord)
- **Schlaue Wiederholung:** verfehlte Vokabeln kommen automatisch öfter dran („Angstgegner“)
- **XP & Klassenstufen:** von Klasse 1 bis „Klasse 13 – ABI-BOSS“, plus 🔥 Tage-Serie
- **📊 Statistik:** Spiele, Trefferquote, besiegte Zombies, beste Welle, Spielzeit, Gelernt-Zähler (3× richtig), meistverfehlte Vokabeln
- **Faire Antwortprüfung:** Groß-/Kleinschreibung egal, Artikel optional (*dog* = *the dog*),
  mehrere Lösungen per `/` (*laufen/rennen*), Akzente standardmäßig tolerant (*é* = *e*, umschaltbar)
- **Eigene Vokabellisten:**
  - von Hand eintippen
  - als Text einfügen (`englisch – deutsch`, eine Vokabel pro Zeile)
  - 📸 **per Foto vom Vokabelbuch**: Texterkennung (Tesseract.js) läuft komplett im Browser,
    nichts wird hochgeladen; erkannte Paare werden vor der Übernahme zur Kontrolle angezeigt
  - 📤 **Export als Text** zum Teilen mit Freunden
- **Lernhilfe:** Nach jedem Spiel eine Liste der Vokabeln, die du verfehlt hast
- Speicherung (Listen, Rekorde, XP, Statistik, Einstellungen) per `localStorage` direkt im Browser

## Technik

Vanilla HTML/CSS/JS + Three.js r147 (eingebettet, prozedurale Texturen und Zombie-Modelle aus Primitiven, keine Assets), Sound per WebAudio. Nur für den Foto-Scan wird einmalig Tesseract.js von einem CDN nachgeladen – der Rest funktioniert auch offline.
