# Suivi — installation sur téléphone (PWA)

App 100 % locale : aucune donnée ne quitte le téléphone (localStorage).
Le repo ne contient que du code générique, aucune donnée personnelle.

## Option A — GitHub Pages (5 min)
1. Crée un repo (nom neutre, ex. `daily-log`) sur github.com.
2. Pousse les 5 fichiers : index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png.
3. Settings → Pages → Source : "Deploy from a branch" → main / root → Save.
4. Ouvre https://TON_USER.github.io/daily-log/ sur ton téléphone.
5. Android/Chrome : menu ⋮ → "Ajouter à l'écran d'accueil" (ou "Installer l'application").
   iPhone/Safari : Partager → "Sur l'écran d'accueil".

## Option B — GitLab Pages
Le .gitlab-ci.yml est inclus : push sur un repo GitLab, le job `pages` publie
automatiquement sur https://TON_USER.gitlab.io/NOM_DU_REPO/.

## Données
- Stockées uniquement dans le navigateur du téléphone (localStorage).
- Bouton "Exporter (backup)" dans l'onglet Données → fichier JSON.
- "Importer" pour restaurer. À faire de temps en temps : vider les données
  du navigateur effacerait le suivi.
- Fonctionne hors-ligne une fois installée (service worker).
