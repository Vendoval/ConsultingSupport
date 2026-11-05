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
