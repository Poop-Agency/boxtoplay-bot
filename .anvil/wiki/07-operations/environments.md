# Environnements & Exécution — boxtoplay-bot

## Variables d’environnement

Obligatoires:

- `DISCORD_TOKEN`
- `CLIENT_ID`
- `GIST_ID`
- `GH_TOKEN`
- `GITHUB_REPO`

Optionnelle:

- `IP_DNS` (défaut `orny`)
- `BTP_API_KEY_0`, `BTP_API_KEY_1` (ou `BTP_API_KEY` en fallback) — requis pour `/say` et `/start` (API REST BoxToPlay v1, une clé par compte, même ordre que le Gist)

Source: [`index.js`](../../../../index.js).

## Runtime

- Lancement d’un serveur Express (`/` et `/keep-alive`)
- Cycle keepalive toutes les 5 min (`KEEPALIVE_INTERVAL`)
- Mise à jour présence Discord toutes les 60s (`PRESENCE_INTERVAL`)

Source: [`index.js`](../../../../index.js).
