# Claude Code Masterarbeit-System

Dieses Paket enthält: `CLAUDE.md` (PROF-Mentor), 15 Skills, 9 spezialisierte Subagents, Projektvorlagen und Ordner für Manuskript, Literatur, Analysen und Reviews.

## Installation
1. Repository klonen.
2. Terminal im Repository-Ordner öffnen.
3. `projekt/steckbrief.md` und `projekt/hochschulregeln.md` ausfüllen; offizielle Hochschuldokumente ergänzen.
4. Im Projektordner `claude` starten. Claude Code erkennt `CLAUDE.md`, Skills und Agents automatisch.
5. Skill gezielt aufrufen, z. B. `/thesis-architect`, `/research-scout`, `/prof-write`, `/prof-review`, `/bring-es-mir-bei`.
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
- nur lesend: `independent-examiner`, `academic-editor`, `defense-examiner`
- lesend und Websuche: `research-professor`, `methods-professor`
- dürfen Dateien anlegen: `quality-assurance` (in `reviews/`), `literature-intelligence` (in `literatur/`)
- darf Dateien bearbeiten: `project-manager` (nur `projekt/fortschritt.md`, nur auf Auftrag)
- darf Befehle ausführen: `data-analysis-specialist` (um Analyseskripte nachzurechnen)

MCP-Tools (z. B. Literaturdatenbanken) stehen Agents mit `tools:`-Liste nur zur Verfügung, wenn sie dort ergänzt werden.

## Hinweise
- Für wissenschaftliche Recherche können externe Such- und Literaturdienste sinnvoll sein; dieses Paket installiert keine Datenbank- oder MCP-Verbindungen.
- Subagents sind delegierbare Spezialisten, keine automatisch dauerhaft laufenden Hintergrundaufgaben.
- Die Hochschulregeln und deine wissenschaftliche Eigenleistung haben Vorrang. Jeder Beleg muss am Original überprüft werden.
- Vor Bearbeitung sensibler Interview- oder Personendaten Datenschutz und Hochschulvorgaben klären. Auch bei lokaler Ablage werden Inhalte, die Claude liest, an Anthropic übertragen; das kann eine Einwilligung oder Pseudonymisierung erfordern.
