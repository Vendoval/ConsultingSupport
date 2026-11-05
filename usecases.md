# Use-Case-Katalog

> Bewertung: Nutzen **H**/M/N · Daten **G**rün/**Ge**lb · Status: `idee` → `getestet` → `routine` → `skill`
> Wo: **Chat** (claude.ai-Project) · **Skill** · **Code** (Claude Code) · **Jira** (Connector, Projekt `MP`)

## Nach Projektphase

### Prepare / Angebot
| # | Use Case | Wo | Daten | Nutzen | Status |
|---|---|---|---|---|---|
| P1 | Scope-Fragen und Annahmen für Angebot/Aufwandsschätzung aus Anfrage ableiten | Chat | Ge | M | idee |
| P2 | Projektstrukturplan / Phasenplan EAM-Einführung als Rohgerüst | Chat | G | M | idee |
| P3 | Stakeholder-Analyse und Kommunikationsplan (Rollen statt Namen) | Chat | Ge | M | idee |

### Explore (Fit-to-Standard)
| # | Use Case | Wo | Daten | Nutzen | Status |
|---|---|---|---|---|---|
| E1 | Workshop vorbereiten: Agenda, Fragenkatalog je Prozess (Meldung, Auftrag, Wartungsplanung, Mobile, Material) | Chat → `bausteine/` | G | **H** | idee |
| E2 | Workshop nachbereiten: Stichpunkte → Protokoll, Entscheidungen, offene Punkte, Gap-Liste | Chat → Skill | Ge | **H** | idee |
| E3 | User Stories / Anforderungen mit Akzeptanzkriterien formulieren | Chat | Ge | **H** | idee |
| E4 | Gap bewerten: Standard, Customizing, Erweiterung (BAdI/Fiori-Anpassung/MDK) – Optionen mit Vor-/Nachteilen | Chat (Opus) | Ge | **H** | idee |
| E5 | Fachkonzept: Gliederung, dann kapitelweise | Chat → Skill | Ge | **H** | idee |

### Realize
| # | Use Case | Wo | Daten | Nutzen | Status |
|---|---|---|---|---|---|
| R1 | Testfälle/Testskripte aus Prozess oder Fachkonzept ableiten (Positiv, Negativ, Berechtigung, Mobile offline) | Chat → Skill | Ge | **H** | idee |
| R2 | Customizing-Recherche und -Erklärung (IMG-Pfad, Abhängigkeiten) mit Prüfstatus | Chat + SAPwork | G | **H** | idee |
| R3 | Code verstehen/schreiben: ABAP-Snippets, MDK-Regeln (JS), OData-Abfragen | Code | Ge | M | idee |
| R4 | Datenmigration: Mapping-Tabellen, Bereinigungslogik, Prüfmakros (Excel/VBA, Python) | Code | Ge (nur Struktur/Testdaten) | **H** | idee |
| R5 | Spezifikation für Entwickler (Funktional → Technik) | Chat | Ge | M | idee |

### Deploy
| # | Use Case | Wo | Daten | Nutzen | Status |
|---|---|---|---|---|---|
| D1 | Benutzerhandbuch / Betriebshandbuch in Word-Vorlage | Skill `sap-handbuch` (geplant) | Ge | **H** | idee |
| D2 | Kurzanleitungen, Spickzettel, FAQ für Techniker (SSAM) | Chat | Ge | **H** | idee |
| D3 | Schulungskonzept, Schulungsablauf, Übungsaufgaben | Chat | G | M | idee |
| D4 | Change-Kommunikation: Info-Mails, Go-Live-Ankündigung, Einwandbehandlung | Chat | Ge | M | idee |
| D5 | Cutover-/Go-Live-Checkliste | Chat → `bausteine/` | G | M | idee |

### Run / Support
| # | Use Case | Wo | Daten | Nutzen | Status |
|---|---|---|---|---|---|
| S1 | Fehleranalyse: Meldung/Dump/Log (anonymisiert) → Hypothesen, Prüfschritte | Chat | Ge | **H** | idee |
| S2 | Störungs-/Ticketantwort an Anwender formulieren | Chat | Ge | M | idee |
| S3 | Lessons Learned je Projekt → neutrale Bausteine | Chat → `bausteine/` | G | M | idee |

### Querschnitt (jede Phase)
| # | Use Case | Wo | Daten | Nutzen | Status |
|---|---|---|---|---|---|
| Q1 | Mails: heikel (Eskalation, Absage, Nachfordern), Statusbericht | Chat | Ge | **H** | idee |
| Q2 | Eigene Aufgaben/ToDos aus Notizen → Jira `MP` | Jira | Ge | M | idee |
| Q3 | Meeting-/Telefonnotizen strukturieren | Chat | Ge | M | idee |
| Q4 | Excel/Power-BI-Auswertungen (Formeln, DAX, VBA) | Code/Chat | Ge | M | idee |
| Q5 | Copilot-Skill-Dateien für M365 Copilot beim Kunden (als .md anhängen): Excel-Eintrag, Protokoll, Mail, Testfälle | Skill `copilot-skill` → `bausteine/copilot-*.md` | G | **H** | getestet (`copilot-excel-eintrag`) |

## Wo was Sinn macht

| Ort | Wann | Nicht für |
|---|---|---|
| **Chat im Project** | Einmaliges, Dialog, Entwürfe, Bewertung von Optionen | Wiederkehrendes mit festem Format (→ Skill) |
| **Skill** | Gleicher Ablauf ≥ 3 × mit fester Form (Protokoll, Testfall, Handbuch) | Einmalfragen |
| **Repo `bausteine/`** | Neutrale Vorlagen, die in jedem Projekt wieder gebraucht werden | Alles mit Kundenbezug |
| **Claude Code** | Dateien/Code: VBA, Python, MDK, Massen-Umformungen | Fließtext-Arbeit |
| **Jira-Connector** | Eigene Aufgaben in `MP` | Kunden-Jira (nur falls freigegeben) |
| **M365 Copilot beim Kunden** | Arbeit direkt in Kunden-Dateien (Excel, Word, Outlook), gesteuert über angehängte Copilot-Skill-Dateien | Freie Prompts ohne Vorlage – zu fehleranfällig |

## Nicht sinnvoll / Vorsicht

- Verbindliche Customizing- oder Release-Aussagen ohne Prüfung im System oder in Quelle
- SAP-Hinweise recherchieren: Claude hat keinen Zugang zum SAP for Me – Hinweisinhalt selbst zusammenfassen und einfügen
- Kundendaten im Original (Rot) – auch nicht „kurz mal“
- Entscheidungen im Namen des Kunden formulieren, die nicht abgestimmt sind
- Lange Chats über mehrere Kunden-Themen – je Teilproblem neuer Chat

## Reihenfolge (Vorschlag)

1. Quick Wins im Chat testen: **E2** Workshop-Nachbereitung, **Q1** Mails, **R1** Testfälle
2. Was trägt → Skill: zuerst `workshop-protokoll`, `testfall`; `sap-handbuch` (aus Claudework geplant) hierher ziehen
3. Parallel `bausteine/` aufbauen: Fragenkataloge Explore (E1), Go-Live-Checkliste (D5)
