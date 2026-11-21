# Projekt- und Umsetzungsplan: BOSS läuft

Projekt: Optimierung der Lauf-App «BOSS läuft»
Repository: `adrianaleuenberger-byte/running-app`
Datum: 21. November 2026

Dieser Plan dokumentiert sämtliche Anforderungen und den jeweiligen Umsetzungsstatus. Bei Unterbrüchen kann jederzeit an dieser Stelle nahtlos fortgesetzt werden.

---

## Aufgaben und Status

- [x] **1. Vorbereitung und Anforderungsanalyse**
  - [x] Analyse des bestehenden Codes in `index.html` und der Spezifikationen in `docs/superpowers/specs/`
  - [x] Identifikation des Planungs-Bugs (warum 24.–27. Nov bzw. 25.–27. Nov leer blieben)
  - [x] Bestimmung des satten grünen Farbschemas und des App-Namens «BOSS läuft» (keinerlei Erwähnung von Holzbau)
  - [x] Schweizer Rechtschreibregeln festlegen (konsequent «ss» statt «ß»)

- [x] **2. Bugfix: Planungsalgorithmus für 5, 6 und 7 Läufe pro Woche**
  - [x] *Problem:* In der Funktion `makePlan` wurde bei Erreichen eines langen Laufs (`w.run === 'long'`) die Hilfsfunktion `longDayDate(d)` aufgerufen. Diese sprang hart auf den nächsten Samstag vor. Dadurch wurden Dienstag 24. bis Freitag 27. November komplett übersprungen.
  - [x] *Lösung:* Implementierung einer sauberen Wochentagsmatrix:
    - **7 Läufe / Woche:** Läufe an jedem Wochentag (Mo–So). Keine Leerstellen, 24.–27. Nov sind belegt.
    - **6 Läufe / Woche:** Genau 1 Ruhetag pro Woche (Freitag vor dem langen Lauf). 24. Nov (Di), 25. Nov (Mi) und 26. Nov (Do) sind aktiv mit Einheiten belegt.
    - **5 Läufe / Woche:** Genau 2 Ruhetage pro Woche (z. B. Mo & Fr). 24. Nov (Di), 25. Nov (Mi) und 26. Nov (Do) sind aktiv mit Einheiten belegt.
    - Kein willkürliches Überspringen von Tagen mehr.

- [x] **3. Rebranding auf «BOSS läuft» & sattes grünes Farbschema**
  - [x] Umbenennung aller Bezeichnungen von «RunWise» zu «BOSS läuft»
  - [x] Neutrales, hochwertiges Farbschema:
    - Dominantes Tannengrün (`#1b4332`, `#2d6a4f`, `#40916c`)
    - Schweizer Akzente (`#c29b38`, `#fbf9f5`)
    - Harmonische Statustöne für Einheiten (Locker, Tempo, Intervalle, Langer Lauf, Alternativsport)
  - [x] Schweizer «BOSS»-Badge in der Kopfzeile
  - [x] Vollständiger Verzicht auf jegliche Erwähnung von Holzbau im gesamten Code und Text

- [x] **4. Vollständige Übersetzung ins Deutsche (Schweizer Rechtschreibung)**
  - [x] Komplette Benutzeroberfläche in deutscher Sprache
  - [x] Schweizer Schreibweise: striktes Vermeiden von «ß», durchgängige Verwendung von «ss» (z. B. «schliessen», «regelmässig», «grossartig», «Strasse»)
  - [x] Sportfachliche Bezeichnungen (Grundlagenausdauer, Tempodauerlauf, Intervalle, Langer Lauf, Ausgleichssport)

- [x] **5. Zukünftige Läufe: Sperre der Erfassungsfelder**
  - [x] Bei Auswahl eines geplanten Laufs in der Zukunft (`selectedDate > today`):
    - Ausblenden aller Ist-Eingabefelder (Gefühl, gelaufene Einheit, Laufdauer, Details, «Lauftag speichern»-Button)
    - Einblenden eines Hinweises: «Geplanter Lauf in der Zukunft. Ist-Daten können erst am Lauftag erfasst werden.»
    - Planungsoptionen (Lauf verschieben, Lauf entfernen, Alternativsport reservieren) bleiben erhalten.
  - [x] Bei vergangenen oder heutigen Tagen (`selectedDate <= today`):
    - Vollständige Ist-Erfassungsmaske bleibt aktiv.

- [x] **6. Bereitstellung und Deployment auf GitHub**
  - [x] `PLAN.md` im Hauptverzeichnis des Repositories aktualisiert
  - [x] `index.html` aktualisiert und auf den Branch `main` übertragen
  - [x] `README.md` aktualisiert
  - [x] GitHub Pages Kompatibilität verifiziert
