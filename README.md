# Jagdquiz Edition – Jagdschule Mittelfranken

Vereinfachte Social-Media-Version des Prüfungstrainers.

## Enthalten
- Nur ein Startbutton: „Jagdquiz starten“
- 6 Fragen insgesamt: je 1 zufällige Frage aus SG1–SG6
- Fragenpool aus den ausgewählten 60 Fragen
- Keine Themenauswahl, keine Lösungsanzeige während des Quiz
- Gewinnspiel-Formular mit Vorname, Nachname, E-Mail und optional Telefon
- Pflicht-Checkbox Datenschutz/Gewinnspiel
- freiwillige Checkbox Kontaktaufnahme/Infos zu Jagdscheinkursen
- Knappe Ergebnisübersicht nach Formularabsendung

## Wichtig zur Datenspeicherung
Diese statische Version speichert Teilnahmen zunächst lokal im Browser. Für den öffentlichen Einsatz muss in `index.html` ein Formular-Endpunkt eingetragen werden:

```js
const SUBMISSION_ENDPOINT = "https://...";
```

Geeignet sind z. B. Google Forms, Formspree, Make/Zapier Webhook oder eine Vercel Function mit Datenbank/E-Mail-Anbindung.

## Deployment
Dateien in ein eigenes GitHub-Repo oder einen eigenen Branch laden und über Vercel veröffentlichen, z. B. als `/jagdquiz` oder eigene Subdomain.


## Hinweise für Tally

Formular-Link: https://tally.so/r/obgrjN

### Datenschutz-Link im Formular
In der Checkbox „Datenschutz“ sollte der Text idealerweise so lauten:

`Ich habe die Datenschutzerklärung gelesen und akzeptiere die Teilnahmebedingungen.`

Das Wort „Datenschutzerklärung“ bitte in Tally als Link hinterlegen:
https://jagdschule-mittelfranken.de/datenschutzerklaerung/

Falls die Datenschutzerklärung auf eurer Website unter einer anderen URL liegt, bitte `PRIVACY_URL` in `index.html` entsprechend anpassen.

### Eigene Danke-Seite
Diese Version enthält eine eigene Danke-Seite:

`/danke.html`

Text:
„Vielen Dank fürs Mitmachen! Die Gewinner werden Anfang der kommenden Woche ausgelost und persönlich benachrichtigt.“

Wenn Tally im Free-Plan keine eigene Weiterleitung erlaubt, kann diese Seite trotzdem direkt verlinkt werden. Falls eine Weiterleitung verfügbar ist, als Redirect-URL diese Seite hinterlegen:

`https://DEINE-VERCEL-URL/danke.html`


## Aktualisierung auf GitHub/Vercel

1. Diese ZIP-Datei lokal entpacken.
2. GitHub Repository `jagdquiz` öffnen.
3. Reiter **Code** öffnen.
4. Bestehende Dateien ersetzen bzw. neue Datei `danke.html` mit hochladen.
5. Unten bei **Commit changes** z. B. schreiben: `Update Jagdquiz Ergebnistext und Danke-Seite`.
6. Nach dem Commit startet Vercel automatisch ein neues Deployment.
7. Die Vercel-URL öffnen und testen.

## Tally-Einstellungen

Formular: https://tally.so/r/obgrjN

### Datenschutz verlinken
In Tally die Checkbox **Datenschutz** bearbeiten.

Empfohlener Text:
`Ich habe die Datenschutzerklärung gelesen und akzeptiere die Teilnahmebedingungen.`

Das Wort **Datenschutzerklärung** markieren und als Link hinterlegen:
https://jagdschule-mittelfranken.de/datenschutzerklaerung/

Falls eure Datenschutzerklärung anders heißt, bitte die tatsächliche URL verwenden und zusätzlich in `index.html` die Konstante `PRIVACY_URL` anpassen.

### Hidden Fields prüfen
Die Hidden Fields sollten in Tally vorhanden sein:
- `ergebnis`
- `punkte`
- `prozent`

Optional zusätzlich:
- `fragen`
- `richtige_fragen`
- `falsche_fragen`
- `quelle`

### Danke-Seite
Diese Version enthält eine eigene Danke-Seite:
`/danke.html`

Wenn Tally eine Weiterleitung nach Absenden erlaubt, als Redirect-URL eintragen:
`https://DEINE-VERCEL-URL/danke.html`

Falls Tally im Free-Plan keine Weiterleitung erlaubt, kann die Standard-Dankeseite von Tally bleiben.


## Version v5

Umgesetzt:
- Antworttext korrigiert: `Kipplaufgewehr mit Handspannung`
- Instagram-Screenshot-Hinweis direkt vor der Ergebnisanzeige ergänzt
- zusätzlicher Hinweis auf kleine Überraschung für geteilte Stories


Finale Version: Button zur Danke-Seite entfernt.
