# Claude Code Masterarbeit-System

Dieses Paket enthält: `CLAUDE.md` (PROF-Mentor), 15 Skills, 9 spezialisierte Subagents, Projektvorlagen und Ordner für Manuskript, Literatur, Analysen und Reviews.

## Installation
1. ZIP entpacken.
2. Terminal im Ordner `Claude_Masterarbeit_System` öffnen.
3. `projekt/steckbrief.md` und `projekt/hochschulregeln.md` ausfüllen; offizielle Hochschuldokumente ergänzen.
4. Im Projektordner `claude` starten. Claude Code erkennt `CLAUDE.md`, Skills und Agents automatisch.
5. Skill gezielt aufrufen, z. B. `/thesis-architect`, `/research-scout`, `/prof-write`, `/prof-review`, `/bring-es-mir-bei`.
6. Subagent im Chat beauftragen, z. B. „Lass den independent-examiner Kapitel 2 unabhängig prüfen.“ Verfügbare Agenten auch über `/agents` ansehen.

## Erster Prompt
„Lies CLAUDE.md und die Dateien in projekt/. Agiere als PROF. Analysiere die Angaben und schlage die nächsten drei Schritte für meine Masterarbeit vor. Erfinde keine fehlenden Details.“

## Hinweise
- Für wissenschaftliche Recherche können externe Such- und Literaturdienste sinnvoll sein; dieses Paket installiert keine Datenbank- oder MCP-Verbindungen.
- Subagents sind delegierbare Spezialisten, keine automatisch dauerhaft laufenden Hintergrundaufgaben.
- Die Hochschulregeln und deine wissenschaftliche Eigenleistung haben Vorrang. Jeder Beleg muss am Original überprüft werden.
- Vor Bearbeitung sensibler Interview- oder Personendaten Datenschutz und Hochschulvorgaben klären.
