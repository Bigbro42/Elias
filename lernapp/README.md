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

Mit KI: Lernstoff einfügen, „KI-Auftrag kopieren“, in Claude einfügen, Antwort als neuen Kurs speichern.

Fortschritt liegt im Browser (localStorage). Zum Übertragen zwischen Geräten: „Sicherung kopieren“ und auf dem anderen Gerät „Sicherung laden“.
