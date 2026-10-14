# Funke Lernapp

Eigene Lern-App im Stil von Sprachlern-Apps: Lernpfad, XP, Streak, Herzen, Wiederholung nach Lernkartei-Prinzip und Erklär-Shorts mit Vorlesefunktion. Alles läuft im Browser, ohne Server und ohne Konto.

## Starten

- **Am PC:** `index.html` im Browser öffnen.
- **Auf dem Handy als App:** Ordner über HTTPS hosten (z. B. GitHub Pages), Seite öffnen und „Zum Startbildschirm hinzufügen“ wählen. Danach läuft sie auch offline.

## Eigene Inhalte

Unter **Inhalte** einen Kurs als Text anlegen:

```
# Kursname
## Einheit
### Lektion
MC: Frage | richtig | falsch | falsch
TF: Aussage | wahr
GAP: Satz mit ___ Lücke | Lösung / Alternative
PAIRS: Begriff = Erklärung ; Begriff = Erklärung
CARD: Vorderseite | Rückseite
SHORT: Titel | Erklärtext in kurzen Sätzen | Formel
QUIZ: Frage zum Short | richtig | falsch
```

Zusätzlich: `KURZ: MOC` (Kürzel fürs Fach-Emblem), `LANG: en` (Vorlesesprache) und `@12` am Zeilenende (Verweis auf Folie 12).

**Aus Unterlagen erstellen:** Unter „Inhalte“ eine PDF (Folien, Skript) oder Text hochladen. In claude.ai baut Claude daraus direkt in der App den Kurs und speichert die Folien, die dann in Lektionen und Shorts angezeigt werden. Außerhalb von claude.ai gibt es stattdessen „KI-Auftrag kopieren“.

**Fächer:** Oben links das Fach wechseln, wie eine Sprache bei Sprachlern-Apps. Jedes Fach hat seinen eigenen Lernpfad.

In claude.ai wird der Stand mit dem Claude-Konto synchronisiert (Handy und PC). Sonst liegt er im Browser (localStorage); zum Übertragen zwischen Geräten: „Sicherung kopieren“ und auf dem anderen Gerät „Sicherung laden“.
