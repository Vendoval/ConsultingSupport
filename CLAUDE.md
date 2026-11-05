# CLAUDE.md – Regeln für dieses Repo

Unterstützung für Michas Beraterarbeit (SAP EAM/PM, SSAM) beim Kunden: Workshops, Anforderungen, Tests, Doku, Schulung, Kommunikation, Projektsteuerung.
Genutzt von Claude im Browser (claude.ai-Project „ConsultingSupport“) und Claude Code.

## Dateien

| Datei | Inhalt | Wer pflegt |
|---|---|---|
| `context.md` | Rolle, Datenregeln, Abgrenzung, Arbeitsweise | **Micha** – Claude nur nach Rückfrage |
| `usecases.md` | Use-Case-Katalog mit Ort, Phase, Datenklasse, Status | beide – Status/Erfahrung pflegt Claude |
| `notes.md` | Laufender Stand: Entscheidungen, offene Punkte, Erkenntnisse | **Claude** – nur anhängen |
| `bausteine/` | Neutrale, wiederverwendbare Bausteine (Fragenkataloge, Checklisten, Gliederungen) | beide |

@context.md

## Arbeitsregeln für Claude

1. Zu Beginn `context.md`, `usecases.md` und die letzten Einträge in `notes.md` lesen.
2. **Datenklasse prüfen, bevor gearbeitet wird** (siehe `context.md`). Rot → nicht verarbeiten, auf Anonymisierung hinweisen. Gelb → im Chat ok, nichts davon ins Repo.
3. Ins Repo nur Neutrales: keine Kundennamen, Werke, Personen, SIDs/Mandanten, Belegnummern, Preise. Im Zweifel abstrahieren oder weglassen.
4. SAP-Aussagen (Customizing, T-Codes, Tabellen, BAdIs, Releasestände) mit Prüfstatus: `[geprüft]` nur mit Quelle, sonst `[ungeprüft]`. Nichts erfinden.
5. Ergebnisse zuerst als Gliederung/Entwurf, dann ausarbeiten. Fachliche Freigabe bleibt bei Micha.
6. `notes.md`: neue Einträge **unten** anhängen, Format `## JJJJ-MM-TT – Thema`, kurz. Alte Einträge nicht umschreiben. Erledigtes abhaken (`- [x]`), nicht löschen.
7. Wiederholt sich ein Ablauf (≥ 3 ×), vorschlagen, daraus einen Skill oder Baustein zu machen; in `usecases.md` vermerken.
8. Commit-Messages Deutsch, kurz: `notes: …`, `usecases: …`, `bausteine: …`, `context: …`. Am Ende committen **und pushen**.
