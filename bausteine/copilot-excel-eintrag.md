# Skill: Eintrag in Excel-Liste ergänzen

> Copilot-Skill-Datei für Microsoft 365 Copilot in Excel (Bearbeitungsmodus). Als Datei an den Chat anhängen.
> Aufruf: `Nach copilot-excel-eintrag.md. Blatt "<…>": <Feld>: <Wert>, <Feld>: <Wert>, …`
> Status: getestet (2026-11-05)

## Zweck
Neue Zeile(n) in eine bestehende Liste eintragen, ohne sonst etwas zu ändern.

## Ablauf
1. Ziel: Arbeitsblatt und Liste laut meiner Angabe. Fehlt die Angabe und gibt es mehrere Listen: nachfragen, nicht raten.
2. Kopfzeile lesen, meine Feldnamen den Spalten zuordnen. Ist die Zuordnung unklar: nachfragen.
3. Neue Zeile direkt unter dem letzten Eintrag einfügen. Keine Leerzeile, nicht mitten in die Liste.
4. Format der Zeile darüber übernehmen (Datum, Zahl, Dropdown). Formeln in berechneten Spalten fortführen, nicht überschreiben.
5. Werte nur aus meiner Angabe. Fehlende Felder leer lassen. Nichts erfinden.

## Verboten
- Andere Zellen, Spalten, Formate, Filter oder Sortierung ändern
- Daten zusammenfassen, umformatieren oder "aufräumen"
- Neue Blätter oder Dateien anlegen

## Datum
TT.MM.JJJJ, sofern die Spalte nichts anderes vorgibt.

## Rückmeldung
Kurz: Blatt, Zeilennummer, eingetragene Werte als Tabelle. Hinweis nur bei Abweichungen, z. B. Wert passt nicht zur Dropdown-Liste.
