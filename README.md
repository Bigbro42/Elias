# Claude Code Masterarbeit-System

Dieses Paket enthält: `CLAUDE.md` (PROF-Mentor), 8 Skills, 3 spezialisierte Subagents, Projektvorlagen und Ordner für Manuskript, Literatur, Analysen und Reviews. Die Übersicht, welcher Skill und welcher Agent wofür da ist, steht in `CLAUDE.md` unter „Zusammenarbeit“.

## Installation
1. Repository klonen.
2. Terminal im Repository-Ordner öffnen.
3. `projekt/steckbrief.md` und `projekt/hochschulregeln.md` ausfüllen; offizielle Hochschuldokumente ergänzen.
4. Im Projektordner `claude` starten. Claude Code erkennt `CLAUDE.md`, Skills und Agents automatisch.
5. Skill gezielt aufrufen, z. B. `/ma-konzept`, `/ma-recherche`, `/ma-schreiben`, `/ma-review`, `/ma-planung`.
6. Subagent im Chat beauftragen, z. B. „Lass den independent-examiner Kapitel 2 unabhängig prüfen.“ Verfügbare Agenten auch über `/agents` ansehen.

## Erster Prompt
„Lies CLAUDE.md und die Dateien in projekt/. Agiere als PROF. Analysiere die Angaben und schlage die nächsten drei Schritte für meine Masterarbeit vor. Erfinde keine fehlenden Details.“

## Ordner und Vorlagen
- `projekt/` – Steckbrief, Hochschulregeln, Fortschritt, KI-Nutzungsprotokoll (`ki-protokoll.md`)
- `arbeit/` – eigene Manuskripte
- `literatur/` – Evidenzmatrix (`evidenzmatrix.md`); Volltext-PDFs in `literatur/volltexte/` (nicht versioniert)
- `analyse/` – Skripte und Ergebnisse; personenbezogene Rohdaten in `analyse/rohdaten/` (nicht versioniert)
- `reviews/` – Gutachten der Subagents

## Werkzeugrechte der Subagents
Die Rechte sind per `tools:` begrenzt, damit die Regeln technisch greifen und nicht nur im Prompt stehen:
- `independent-examiner`: nur lesend; der Hauptagent speichert den Bericht in `reviews/`
- `literature-intelligence`: lesen, Websuche, neue Dateien in `literatur/` anlegen
- `data-analysis-specialist`: lesen und Befehle ausführen, um Analyseskripte nachzurechnen

MCP-Tools (z. B. Literaturdatenbanken wie Consensus oder Zotero) stehen Agents mit `tools:`-Liste nur zur Verfügung, wenn sie dort ergänzt werden, bei `literature-intelligence` als `mcp__<servername>__<toolname>` (den genauen Namen zeigt `/mcp`).

## Warum `ma-` vor den Skill-Namen?
Das Präfix verhindert Namensgleichheit mit allgemeinen persönlichen Skills (z. B. `prof-write`, `prof-review`). Die `ma-`-Skills sind auf dieses Projekt zugeschnitten: Sie lesen Steckbrief und Hochschulregeln und schreiben in die Projektordner.

## Hinweise
- Für wissenschaftliche Recherche können externe Such- und Literaturdienste sinnvoll sein; dieses Paket installiert keine Datenbank- oder MCP-Verbindungen.
- Subagents sind delegierbare Spezialisten, keine automatisch dauerhaft laufenden Hintergrundaufgaben.
- Die Hochschulregeln und deine wissenschaftliche Eigenleistung haben Vorrang. Jeder Beleg muss am Original überprüft werden.
- Vor Bearbeitung sensibler Interview- oder Personendaten Datenschutz und Hochschulvorgaben klären. Auch bei lokaler Ablage werden Inhalte, die Claude liest, an Anthropic übertragen; das kann eine Einwilligung oder Pseudonymisierung erfordern.
