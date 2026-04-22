# Quiz App

Eine browserbasierte, themenfähige Quiz-Anwendung im Jeopardy-Stil.  
Entwickelt als Einzeldatei-HTML-App – kein Build-Prozess, kein Backend, keine Abhängigkeiten außer einem Browser.

---

## Funktionsumfang

- **Kategorien & Fragen** – beliebig viele Kategorien und Frage-Stufen, frei konfigurierbar
- **Medientypen** – Text, Bild (URL), Video (lokal oder YouTube), Audio (lokal oder YouTube)
- **Themes** – Weihnachten, Ostern, Geburtstag, Hochzeit, Party (inkl. Partikel-Effekt)
- **Teams** – 1–10 Teams mit individuellen Namen und Punktestand
- **Punktemultiplikatoren** – konfigurierbare Multiplikatoren die nach einem bestimmten Prozentsatz gespielter Fragen ausgelöst werden
- **Timer** – pro Frage-Stufe konfigurierbarer Standard-Timer, individuell pro Frage überschreibbar
- **Admin-Panel** – vollständige Konfiguration im laufenden Betrieb über drei Tabs (Fragen / Kategorien / Einstellungen)
- **Autosave** – alle Änderungen im Admin-Panel werden automatisch 1 Sekunde nach der letzten Eingabe im `localStorage` gespeichert
- **Export / Import** – Fragenkatalog als JSON exportieren und wieder importieren

---

## Schnellstart

1. `quiz_app.html` in einem modernen Browser öffnen (Chrome, Firefox, Edge, Safari)
2. Theme auswählen
3. Optional: Fragenkatalog als `.json` Datei laden
4. Anzahl der Teams und Teamnamen eingeben
5. Quiz starten

Kein Webserver nötig – die Datei funktioniert direkt als lokale Datei (`file://`).

---

## Fragenkatalog (JSON)

Der Fragenkatalog kann über das Admin-Panel (⚙ Einstellungen → Export) als JSON-Datei gesichert und wieder importiert werden.

**Struktur:**
```json
{
  "cats": [
    { "name": "Geografie", "emoji": "🌍", "color": "#1565C0" }
  ],
  "pts": [200, 500, 1000],
  "timers": [30, 45, 60],
  "qs": [
    [
      { "type": "text", "question": "Hauptstadt von Frankreich?", "answer": "Paris", "timer": null, "pixelated": false, "startTime": null, "duration": null }
    ]
  ],
  "theme": "christmas",
  "title": "🎄 Weihnachts Trivia Quiz 🎄"
}
```

**Fragetypen:**

| Typ | `type` | `question`-Feld |
|---|---|---|
| Text | `text` | Fragetext |
| Bild | `image` | Bild-URL |
| Video | `video` | Video-URL oder Blob |
| Audio | `audio` | Audio-URL, Blob oder YouTube-URL |

---

## Admin-Panel

Erreichbar über den **⚙ Einstellungen** Button während des Spiels.

### Tab: Fragen
- Fragenstruktur (Anzahl Stufen, Punkte, Timer) bearbeiten
- Alle Fragen aller Kategorien bearbeiten
- Mediadateien lokal laden

### Tab: Kategorien
- Kategorien hinzufügen, umbenennen, Emoji und Farbe ändern
- Kategorien löschen (löscht alle zugehörigen Fragen)

### Tab: Einstellungen
- Theme wechseln
- Quiz-Titel bearbeiten
- Punktemultiplikatoren konfigurieren
- Lautstärken für Timer-Ton, Video und Musik einstellen

---

## Technische Details

| Merkmal | Beschreibung |
|---|---|
| Technologie | Vanilla HTML / CSS / JavaScript (ES6+) |
| Abhängigkeiten | Keine npm / build-Abhängigkeiten |
| Datenspeicherung | Ausschließlich `localStorage` des Browsers |
| Offline-fähig | Ja (ohne YouTube-Funktion vollständig offline nutzbar) |
| Minimalgröße | Eine einzelne `.html` Datei |

---

## Drittanbieter-Abhängigkeiten

| Komponente | Typ | Wann aktiv |
|---|---|---|
| Google Fonts CDN | Extern | Beim Laden der Seite |
| YouTube IFrame API | Extern (proprietär) | Nur bei Klick auf Play mit YouTube-URL |

> **Hinweis:** Es ist geplant, Google Fonts künftig lokal zu hosten, um externe Verbindungen beim Seitenaufruf zu vermeiden.

Weitere Details siehe [NOTICE](NOTICE).

---

## Dateistruktur (Deployment)

```
/
├── quiz_app.html        ← Hauptanwendung
├── impressum.html       ← Impressum (§ 5 TMG)
├── datenschutz.html     ← Datenschutzerklärung (DSGVO)
├── LICENSE              ← Lizenzbedingungen
├── NOTICE               ← Drittanbieter-Attributionen
└── README.md            ← Diese Datei
```

---

## Lizenz

Copyright (c) 2026 Sven Riedel. Alle Rechte vorbehalten.  
Proprietäre Software – siehe [LICENSE](LICENSE) für vollständige Bedingungen.

---

## Rechtliche Hinweise

- **Impressum:** [impressum.html](impressum.html)
- **Datenschutz:** [datenschutz.html](datenschutz.html)
