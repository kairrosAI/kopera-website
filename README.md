# Site vitrine KOPERA

Site statique (HTML/CSS/JS) pour la solution KOPERA — une page marketing, hébergée via OpenAI Hosting.

## Structure

| Chemin | Rôle |
|--------|------|
| `dist/` | Fichiers servis en production (`index.html`, `styles.css`, `script.js`, `assets/`) |
| `.openai/hosting.json` | Rattachement au site déjà publié sur OpenAI (ne pas supprimer sans recréer le projet côté hébergeur) |
| `dist/assets/` | Logo KOPERA et logos des connecteurs |

## Modifier le contenu

1. Éditer les fichiers dans `dist/` (pas de build intermédiaire).
2. Prévisualiser en local :

   ```bash
   cd dist && python3 -m http.server 8080
   ```

   Ouvrir [http://localhost:8080](http://localhost:8080).

3. Vérifier le responsive et les liens (`#demo`, mailto `contact@kairros.ai`).

## URL publique (équipe)

**GitHub Pages :** https://kairrosai.github.io/kopera-website/

Chaque push sur `main` redéploie automatiquement le contenu de `dist/` (workflow `.github/workflows/pages.yml`).

## Publier (OpenAI Hosting, optionnel)

Le déploiement Codex passe aussi par **OpenAI Hosting** (`.openai/hosting.json`, répertoire `dist/`).

- Ne pas commiter de secrets ; le site est entièrement statique.

## Historique Git

Trois commits initiaux (maquette hero, logos applications, connecteurs Gmail/HubSpot/Boond). Pour un remote GitHub Kairros, ajouter `origin` et pousser quand le dépôt est créé.
