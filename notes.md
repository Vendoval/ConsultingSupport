# ConsultingSupport – Notizen

> Laufender Stand. Claude hängt neue Einträge unten an. Neueste Einträge zuletzt.

## 2026-11-05 – Start

- Repo nach Vorlage aus `Vendoval/Claudework` angelegt: `CLAUDE.md`, `context.md`, `usecases.md`, `notes.md`, `README.md`, `bausteine/`
- Datenklassen Grün/Gelb/Rot festgelegt; ins Repo nur Grün
- Abgrenzung: SAPwork = Fachwissen, CustandTest = Toolbau, hier = Beraterarbeit
- Offene Punkte:
  - [ ] Micha: `context.md` prüfen und freigeben
  - [ ] Micha: KI-Einsatz mit matrix/Kunde klären (erlaubt? Gerät/Account?)
  - [ ] Quick Wins testen: E2 Workshop-Nachbereitung, Q1 Mails, R1 Testfälle
  - [ ] Skill `sap-handbuch` hierher ziehen (Quelle bisher in Claudework geplant)
  - [ ] Erste Bausteine: Fragenkatalog Störmeldung/Auftrag, Go-Live-Checkliste

## 2026-11-05 – Microsoft 365 Copilot beim Kunden

- Beim Kunden erlaubt: M365 Copilot (Premium), Modellwahl Auto / GPT-6 Sol / GPT-6.1 Sol, keine Anthropic-Modelle freigeschaltet
- Excel: Copilot-Button nicht im Menüband, sondern schwebend unten in der Ansicht; Bearbeitungsmodus („Mit Copilot bearbeiten“, grüner Stift) trägt direkt in die Mappe ein – getestet, klappt
- Modell: Auto für einfache Einträge; bei Fehlgriffen GPT-6.1 Sol fest einstellen
- Skills lassen sich nicht anhängen, aber eine Skill-Datei (.md) als Anhang wirkt als Anweisung sehr gut → Entscheidung: eigene Copilot-Skill-Dateien bauen
- Erster Baustein: `bausteine/copilot-excel-eintrag.md` (getestet); Use Case Q5 in `usecases.md`
- Claude-Skill `copilot-skill` vorgeschlagen: erzeugt neue Copilot-Skill-Dateien nach gleichem Schema
- Erkenntnis: Freie Prompts in Copilot sind fehleranfällig; feste Datei mit Ablauf, Verboten, Rückmeldung reduziert Fehler
- Offene Punkte:
  - [ ] Micha: `context.md` ergänzen – KI beim Kunden = M365 Copilot erlaubt (Datenregeln dort nach Kundenvorgabe)
  - [ ] Weitere Copilot-Skills: `copilot-protokoll`, `copilot-mail`, `copilot-testfaelle`
  - [ ] Datei suchen in verschachteltem SharePoint: Favoriten/„Meine Dateien“ oder Copilot-Chat-Suche testen
  - [ ] Bei wiederkehrend gleichen Listen: Power-Automate-Flow „Zeile hinzufügen“ prüfen

## 2026-11-09 – Kick-off-Timeline als draw.io
- Timeline fürs mittlere Management aus Aufgabenliste (Reihenfolge, Kategorie, PT) als draw.io-XML erzeugt, per Python-Skript generiert
- Aufbau bewährt: Seite 1 Management (3 Phasen + Puffer, Meilensteine, externe Abhängigkeit SAP-Release, Annahmen), Seite 2 Detail je Team (Backend, Fachbereich, Frontend/MDK, Middleware/BTP)
- Erkenntnis: Ohne Startdatum und Besetzung relative Wochen (W1 …) plus sichtbarer Annahmen-Kasten; Release-Abhängigkeit als eigener Meilenstein
- Offene Punkte:
  - [ ] Micha: Startdatum/KW und Besetzung klären, dann auf KW umstellen (Feiertage Jahresende beachten)
  - [ ] Doppelte Zeilen in der Aufgabenliste klären (2. Runde oder Kopierfehler)
- Bei Wiederholung: Generator als neutralen Baustein `bausteine/` anlegen (Use Case P2)

## 2026-11-09 – Timeline: Kachel-Stil statt Gantt fürs Management
- Micha bevorzugt für Kick-off-Folien Phasen als Kacheln mit Pfeilen (Vorbereitung, Vortest, Vorentwicklungsvorbereitung, Entwicklung, Test, Go Live) statt Gantt
- Umsetzung: Seite 1 Kacheln + Meilenstein-Leiste darunter, Klammer „Vorphase (geplant)“ vs. „Folgephasen (Planung nach Fit/Gap)“; Seite 2 Detailplan je Team als Gantt bleibt
- Erkenntnis: Ungeplante Folgephasen heller und gestrichelt darstellen, Platzhalter `[Text]` stehen lassen

## 2026-11-09 – Timeline: grobe Monats-Roadmap fürs Management
- Für Management reicht Monatsebene: Phasen-Pfeile über Monate, 2–3 Stichpunkte je Phase, Meilenstein-Leiste, Fußzeile mit Annahmen
- Grobablauf SSAM-Upgrade: Fit/Gap in Sandbox (Nov–Mitte Dez) → Vorbereitung Entwicklungsumgebung (Dez) → Entwicklung (Jan–Ende Mär) → Test (Apr) → Go Live (Jun 2027)
- Mai als Vorschlag für Schulung, Cutover, Go/No-Go (von Micha zu bestätigen)
- Detail-Gantt der Vorphase bleibt als Backup-Seite
