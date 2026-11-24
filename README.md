# Chemie Oberstufe – Lern-Apps

Interaktive Lern-Apps für den Chemieunterricht der Oberstufe (Klasse 11–12, Lehrplan des deutschen Schulsystems).
Die Apps sind Übungs- und Wiederholungsmaterial, keine Leistungsüberprüfung.

**Live:** https://jsumme.github.io/oberstufe-chemie/

Autor: Jan Summe

---

## Apps

| Ordner | Thema | Inhalt | Link |
|---|---|---|---|
| `01-kinetik-ggw/` | Kinetik und chemisches Gleichgewicht | Lern-App inkl. Simulationen (Kinetik, Le Chatelier) | [öffnen](https://jsumme.github.io/oberstufe-chemie/01-kinetik-ggw/) |
| `01-kinetik-ggw/lechatelier-konzentration.html` | | Simulation Estersynthese (Konzentration) | [öffnen](https://jsumme.github.io/oberstufe-chemie/01-kinetik-ggw/lechatelier-konzentration.html) |
| `01-kinetik-ggw/lechatelier-druck.html` | | Simulation NO₂/N₂O₄ (Druck) | [öffnen](https://jsumme.github.io/oberstufe-chemie/01-kinetik-ggw/lechatelier-druck.html) |
| `01-kinetik-ggw/lechatelier-temperatur.html` | | Simulation NO₂/N₂O₄ (Temperatur) | [öffnen](https://jsumme.github.io/oberstufe-chemie/01-kinetik-ggw/lechatelier-temperatur.html) |
| `02-protonenuebergaenge/` | Protonenübergänge | Säure-Base-Reaktionen (React-Build) | [öffnen](https://jsumme.github.io/oberstufe-chemie/02-protonenuebergaenge/) |
| `03-redoxreaktionen/` | Redoxreaktionen | Lern-App Redoxreaktionen | [öffnen](https://jsumme.github.io/oberstufe-chemie/03-redoxreaktionen/) |
| `03-redoxreaktionen/elektrochemie/` | | Lern-App Elektrochemie | [öffnen](https://jsumme.github.io/oberstufe-chemie/03-redoxreaktionen/elektrochemie/) |
| `04-elektrolyse/` | Elektrolyse | Lern-App Elektrolyse inkl. Faraday-Gesetze | [öffnen](https://jsumme.github.io/oberstufe-chemie/04-elektrolyse/) |

Die Startseite (`index.html`) verlinkt alle Apps.

---

## Konventionen

- **Ein Ordner pro Thema**, nummeriert in Unterrichtsreihenfolge (`01-…`, `02-…`). Einstieg ist immer `index.html`.
- **Nur relative Pfade** (`bilder/a.png`, nicht `/bilder/a.png`). Die Seite liegt unter `/oberstufe-chemie/`, absolute Pfade führen dort ins Leere.
- **Statische Dateien.** Kein Server, keine Netlify Functions. Fortschritt wird nur im Browser der Lernenden gespeichert (`localStorage`).
- Tailwind und Lucide werden über CDN geladen → die Apps brauchen eine Internetverbindung.
- `02-protonenuebergaenge/` ist ein **Build** (Vite/React). Der Quellcode liegt lokal, nicht in diesem Repo. Nach einem neuen Build die Verweise in `index.html` auf `./assets/…` (relativ) prüfen, oder in `vite.config.js` `base: './'` setzen.
- `.nojekyll` verhindert, dass GitHub Pages die Dateien mit Jekyll verarbeitet.

## Neue App hinzufügen

1. Ordner anlegen, z. B. `05-thema/`, App als `index.html` hineinlegen.
2. Lokal im Browser öffnen und testen; Pfade prüfen.
3. Auf der Startseite (`index.html`) eine Karte ergänzen und die Tabelle oben aktualisieren.
4. Committen und pushen. Nach ca. 1–2 Minuten ist die App online.

## Nicht in dieses Repo

Das Repo ist **öffentlich**. Deshalb gehören hier nicht hinein:

- Klausuren, Erwartungshorizonte, Lösungen zu bewerteten Aufgaben
- Schulbuchseiten, Scans und andere urheberrechtlich geschützte Fremdmaterialien
- Daten von Schülerinnen und Schülern
- Zugangsdaten, Schlüssel, `.env`-Dateien

Hinweis: Die Apps prüfen Antworten im Browser. Die Lösungen stehen daher im Quelltext jeder Seite. Für Übungsmaterial ist das unproblematisch.

## Fortschritt erfassen (optional, geplant)

Soll eine App Ergebnisse sammeln, sendet sie diese an ein Google-Apps-Script im Schulkonto, das sie in eine private Google-Tabelle schreibt. In der App und im Repo stehen keine Schülerdaten. Die Lernenden geben nur ein Kürzel ein; die Zuordnung Kürzel → Name liegt getrennt im Schulkonto.

## Lizenz

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.de) – Jan Summe.
Eingebundenes Fremdmaterial (z. B. Abbildungen unter CC BY-SA) ist in den jeweiligen Apps mit Quelle ausgewiesen und behält seine eigene Lizenz.
