# Projekt- und Umsetzungsplan: BOSS läuft

Projekt: Intelligente Trainingsplanung & Athleten-Steuerung für «BOSS läuft»
Repository: `adrianaleuenberger-byte/running-app`
Datum: 21. November 2026

Dieser Plan dokumentiert alle bisherigen und kommenden Entwicklungsschritte. Bei Unterbrüchen kann jederzeit an dieser Stelle nahtlos fortgesetzt werden.

---

## 1. Bereits abgeschlossene Basisanpassungen (V1 & V2)

- [x] **1.1 Vorbereitung & Algorithmus-Bugfix**
  - [x] Fehleranalyse der Planungslücken (24.–27. Nov bei 6/7 Läufen bzw. 25.–27. Nov bei 5 Läufen behoben)
  - [x] Lückenlose Kalenderverteilung sichergestellt
- [x] **1.2 Rebranding & Design**
  - [x] Umbenennung der Applikation zu «BOSS läuft»
  - [x] Sattes Tannengrün als Leitfarbe (`#1b4332`, `#2d6a4f`) mit Schweizer Gold-/Naturakzenten
  - [x] Vollständiger Verzicht auf Erwähnung von Holzbau im gesamten Projekt
- [x] **1.3 Schweizer Rechtschreibung & Zukunftssperre**
  - [x] Konsequente Schweizer Rechtschreibung («ss» statt «ß»)
  - [x] Sperre für reale Ist-Dateneingaben bei zukünftigen Läufen

---

## 2. Upgrade V3: Intelligente Trainingssteuerung & Personalisierung

- [x] **2.1 Athleten-Profil (Option A: Schlank & Unkompliziert)**
  - [x] Eingabe der aktuellen durchschnittlichen Wochenkilometer (Baseline-Volumen in km)
  - [x] Eingabe einer Referenzleistung (Auswahl: 5 km oder 10 km mit Zeit in Minuten/Sekunden)
  - [x] Mathematische VDOT- und Schwellen-Pace-Berechnung nach Jack Daniels
  - [x] Automatische Ableitung der individuellen Trainingsbereiche:
    - *Locker (Easy / GA1)* mit konkretem Pace-Korridor (min/km)
    - *Tempo / Schwellenlauf (Threshold / TDL)*
    - *Intervalle (VO2max)* mit Split-Vorgaben
    - *Langer Lauf (Long Run)*
- [x] **2.2 Automatische Zielzeit-Berechnung (Keine manuelle Eingabe)**
  - [x] Deaktivierung der manuellen Zielzeit-Vorgabe durch den Nutzer
  - [x] Berechnung der physiologisch realistischen Zielzeit durch den Algorithmus anhand von VDOT, verbleibenden Wochen und aktuellem Trainingsvolumen
  - [x] Transparente Anzeige der berechneten Zielzeit und der erforderlichen Renn-Pace
- [x] **2.3 Flexible Wochentags-Auswahl & Langer Lauf**
  - [x] Direkte Auswahl der verfügbaren Trainingstage (Checkboxen Mo, Di, Mi, Do, Fr, Sa, So)
  - [x] Ausdrückliche Definition des Wochentags für den langen Lauf (Long Run)
- [x] **2.4 Physiologische Periodisierung & Distanz/Pace-Kombination**
  - [x] Workouts mit konkreter Kilometer-Vorgabe und errechnetem Tempobereich (z.B. «14 km @ 5:45–6:10 min/km»)
  - [x] Automatische Schätzung der Laufdauer aus Distanz und Pace
  - [x] Strukturierung in Mesozyklen:
    - *Grundlagenphase (Base):* Fokus auf Ausdauerfundament und sanfte Steigerung des Long Runs
    - *Aufbauphase (Build):* Schwellentraining und Tempodauerläufe
    - *Zuspitzung (Peak):* Spezifische Belastungswochen
    - *Tapering:* Gezielte Reduktion vor dem Wettkampf
  - [x] Berücksichtigung der maximalen 10%-Steigerungsgrenze des Wochenvolumens
- [x] **2.5 Farbschema-Harmonisierung für geplante Einheiten**
  - [x] Geplante Einheiten übernehmen das exakte Farbschema der Ist-Einheiten:
    - *Locker:* Zartes Grün (`#d8f3dc`, Text `#1b4332`)
    - *Tempo:* Warmes Bernstein (`#fef3c7`, Text `#78350f`)
    - *Intervalle:* Helles Korallrot (`#fee2e2`, Text `#991b1b`)
    - *Langer Lauf:* Weiches Blau (`#e8f0fe`, Text `#1e40af`)
    - *Alternativsport:* Sanftes Violett (`#f3e8ff`, Text `#5b21b6`)
  - [x] Gestrichelte Umrandung (`border: 1.5px dashed currentColor`) bleibt als klares Planungskriterium erhalten
- [x] **2.6 Adaptiver Feedback-Banner (User entscheidet)**
  - [x] Erkennung von verpassten Einheiten oder protokollierter Erschöpfung
  - [x] Interaktiver Coaching-Banner: «Achtung: Ausfall oder Übermüdung festgestellt. Plan optimieren?»
  - [x] Zwei Aktionsschaltflächen: `[Plan optimieren]` und `[So lassen]`
- [x] **2.7 Bereitstellung & Deployment**
  - [x] Deployment auf GitHub (`main`)
  - [x] Synchronisation der Live-Vorschau
