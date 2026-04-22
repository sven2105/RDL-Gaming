# Quiz App

**Copyright © 2026 Sven Riedel. Alle Rechte vorbehalten.**
Proprietäre Software – Nutzung, Vervielfältigung und Weitergabe nur mit ausdrücklicher schriftlicher Genehmigung des Urhebers.

---

## Beschreibung

Eine vollständig in sich geschlossene, browserbasierte Quiz-App für Gruppen und Events. Die gesamte Anwendung besteht aus **einer einzigen HTML-Datei** – kein Server, keine Installation, keine Abhängigkeiten nötig. Einfach die Datei im Browser öffnen und losspielen.

---

## Features

### Themes
Die App unterstützt fünf wählbare Themes, die Farben, Partikeleffekte und Titel anpassen:

| Theme | Icon | Partikeleffekte |
|---|---|---|
| Weihnachten | 🎄 | ❄ ❅ ❆ ✦ |
| Ostern | 🐣 | 🌸 🌷 🥚 🐣 🌼 |
| Geburtstag | 🎂 | 🎈 🎉 ⭐ ✨ 🎊 |
| Hochzeit | 💍 | 💍 💐 🌹 💕 ✨ |
| Party | 🎊 | 🎊 🎉 ⚡ 💫 🌟 |

### Fragentypen
Jede Frage kann einen der folgenden Inhaltstypen haben:

- **Text** – klassische Frage als reiner Text
- **Bild** – lokale Bilddatei hochladen (optional pixeliert darstellbar)
- **Audio** – lokale Audiodatei mit eigenem Play/Pause-Button
- **Video** – lokale Videodatei mit Lautstärkeregelung
- **YouTube** – YouTube-URL direkt einbetten (lädt YouTube IFrame API bei Bedarf nach)

### Spielablauf
- Bis zu beliebig viele **Teams** spielen gleichzeitig
- Teamnamen werden vor dem Spielstart individuell vergeben
- Das **Spielbrett** zeigt Kategorien als Spalten und Punktwerte als Zeilen
- Geklickte Felder öffnen die Frage in einem Modal-Fenster
- Nach Anzeige der Antwort kann der Spielleiter Punkte manuell an beliebige Teams vergeben
- Bereits beantwortete Felder werden ausgeblendet
- Die **Punkteanzeige** am unteren Rand hebt das führende Team hervor

### Punkte-Multiplikatoren
Multiplikatoren können so konfiguriert werden, dass sie nach einem bestimmten Prozentsatz der gespielten Fragen automatisch aktiviert werden (z. B. ×2 nach 50 % der Fragen). Mehrere Multiplikatoren sind möglich und werden kumuliert.

### Timer
Jede Frage kann einen eigenen Countdown-Timer erhalten. Die Lautstärke des Timer-Tons ist einstellbar.

---

## Einrichtung & Bedienung

### Start
1. `fix_snow_UI_after_FOSS.html` im Browser öffnen
2. Theme auswählen
3. Fragenkatalog als `.json`-Datei laden (oder vorhandenen Speicher verwenden)
4. Anzahl der Teams und Teamnamen eingeben
5. Quiz starten

### Settings-Panel
Über den Button **⚙ Einstellungen** (oben rechts im Quiz) öffnet sich das Settings-Panel mit drei Reitern:

**📝 Fragen**
Alle Fragen und Antworten bearbeiten, Fragetyp wählen, Medien hochladen, Timer pro Frage setzen.

**📁 Kategorien**
Kategorien anlegen, umbenennen, mit Emoji versehen, farblich anpassen oder löschen.

**🎨 Optionen**
- Theme wechseln
- Quiz-Titel anpassen
- Punktwerte und Timer-Stufen konfigurieren
- Punkte-Multiplikatoren verwalten
- Lautstärke für Timer, Video und Musik einstellen

### Import / Export
- **Export:** Speichert den gesamten Fragenkatalog (inkl. eingebetteter Medien) als `.json`-Datei
- **Import:** Lädt eine zuvor exportierte `.json`-Datei und stellt alle Fragen wieder her

---

## Datenspeicherung

Der aktuelle Spielstand, Fragen und Einstellungen werden automatisch im **localStorage** des Browsers gesichert. Änderungen im Settings-Panel werden nach 1 Sekunde Inaktivität automatisch gespeichert. Beim Schließen des Panels wird zusätzlich sofort gespeichert.

> **Hinweis:** Der localStorage ist browserspezifisch. Für dauerhafte Sicherung bitte regelmäßig exportieren.

---

## Drittanbieter-Hinweise

| Komponente | Lizenz |
|---|---|
| Mountains of Christmas, Playfair Display, Nunito (Google Fonts) | SIL Open Font License 1.1 (OFL) |
| YouTube IFrame API | Proprietärer Dienst von Google LLC – [Nutzungsbedingungen](https://www.youtube.com/t/terms) |

Weitere Details siehe [NOTICE](NOTICE).
---

## Technische Voraussetzungen

- Moderner Browser (Chrome, Firefox, Edge, Safari)
- Internetverbindung nur für Google Fonts und YouTube-Einbettung erforderlich
- Keine Installation, kein Server, keine Build-Tools

## Lizenz

Copyright (c) 2026 Sven Riedel. Alle Rechte vorbehalten.  
Proprietäre Software – siehe [LICENSE](LICENSE) für vollständige Bedingungen.

---

## Rechtliche Hinweise

- **Impressum:** [impressum.html](impressum.html)
- **Datenschutz:** [datenschutz.html](datenschutz.html)
