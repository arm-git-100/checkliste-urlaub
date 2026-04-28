# Checkliste Urlaub

PWA-Packliste mit Multi-Tag-Filtern, Google-Login und Echtzeit-Sync via Firebase.

**Live:** https://arm-git-100.github.io/checkliste-urlaub/

## Features

- Login per Google-Account (Email-Whitelist in Firestore Rules)
- 5 Filtergruppen: Saison, Reisetyp, Person, Ausstattung, Extras
- Items mit Mehrfach-Tags (z.B. „Sonnencreme" = Sommer + Basis)
- Dynamisch hinzufügbare Mitreisende
- ~80 vorbefüllte Standard-Items (Reisepass, Skihose, Hundefutter, …)
- „Erledigte zurücksetzen" — Liste fürs nächste Jahr wiederverwendbar
- PWA-installierbar, offline-fähig

## Firebase

| | |
|--|--|
| Projekt-ID | `checkliste-urlaub` |
| Region | `europe-west3` |
| Auth | Google Sign-In, Email-Whitelist in Rules |
| Collections | `items`, `travelers`, `meta` |

## Hosting

GitHub Pages über `https://arm-git-100.github.io/checkliste-urlaub/`. HTTPS automatisch, Service Worker cached die App offline.

## Deploy-Update

```bash
cd C:/ai/projekte/checkliste-urlaub
git add .
git commit -m "Beschreibung"
git push
```

GitHub Pages aktualisiert sich nach 1–2 Min automatisch.
