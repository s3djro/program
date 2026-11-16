# Suivi OSCP

Application web installable (PWA) : suivi quotidien, synchronisée entre tes appareils via un gist privé GitHub.

## 1. Mettre l'app en ligne (GitHub Pages)
1. Crée un compte sur github.com, puis un dépôt **public** nommé `oscp-suivi`.
2. Ajoute les 5 fichiers à la racine du dépôt : `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png` (bouton « Add file » > « Upload files »).
3. Dépôt > Settings > Pages > Source : « Deploy from a branch », branche `main`, dossier `/ (root)`.
4. Après 1 à 2 minutes, l'app est sur `https://TON-PSEUDO.github.io/oscp-suivi/`.

Le dépôt est public, mais il ne contient aucune donnée personnelle : ta progression est stockée dans un gist privé.

## 2. L'installer sur chaque appareil
Ouvre l'adresse dans Safari > bouton Partager > « Sur l'écran d'accueil ». Fais-le sur le téléphone et sur l'iPod touch.

## 3. Activer la synchronisation
1. GitHub > Settings > Developer settings > Personal access tokens > **Tokens (classic)** > Generate new token.
2. Coche **uniquement** la case `gist`. Choisis une durée (note la date d'expiration).
3. Copie le jeton, ouvre l'app > « Configurer » > colle-le > « Enregistrer ». Refais la même chose sur l'autre appareil avec le même jeton.

L'app crée un gist privé `suivi-oscp-2026` au premier appareil, et le retrouve toute seule sur le second. Garde ton jeton secret ; s'il fuit, révoque-le dans GitHub.
