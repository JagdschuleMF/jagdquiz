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
