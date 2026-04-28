# Checkliste Urlaub

PWA-Packliste für Heike & Armin mit Echtzeit-Sync über Firebase Firestore.

## Filter

- **Saison**: Sommerurlaub, Winterurlaub
- **Reisetyp**: Auto, Flug, Wohnmobil, Fahrrad
- **Person**: Heike, Armin + dynamisch hinzufügbare Mitreisende
- **Ausstattung**: Basis, Spezial
- **Extras**: Hund

Items können mehrere Tags haben. Sichtbarkeit pro Item: AND zwischen Filter-Gruppen, OR innerhalb. Items ohne Tag in einer Gruppe gelten als „immer relevant" für diese Gruppe.

## Hosting

Statische Files via **GitHub Pages**, Daten in **Firebase Firestore** (gleiches Projekt wie testprojekt, Collections `urlaub_items`, `urlaub_travelers`, `urlaub_meta`).

Deploy:
1. Repo auf GitHub anlegen
2. Files pushen
3. Settings → Pages → Branch `main` → Save
4. URL: `https://<user>.github.io/checkliste-urlaub/`

## Erststart

Beim ersten Aufruf wird die Liste mit ~80 Standard-Items befüllt (Reisepass, Skihose, Hundefutter etc.). Der Seed-Status wird in `urlaub_meta/seeded` markiert, sodass keine Doppel-Befüllung passiert.
