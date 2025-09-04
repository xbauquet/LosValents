🚀 Stack technique

Astro
 → framework statique moderne, ultra-rapide, compatible avec React/Vue/Svelte si besoin.

Tailwind CSS
 (+ daisyUI
 si besoin de composants prêts à l’emploi) → design flexible et cohérent.

Decap CMS
 → back-office “headless CMS” qui édite directement les fichiers du dépôt (Markdown/YAML/JSON).

Déploiement : GitHub Pages
 (via GitHub Actions).

Stockage du contenu : fichiers Markdown/YAML/JSON dans le dossier /content.

Gestion des images : placées dans /public/images, optimisées à la build avec Astro.

🔑 Authentification (Admin)

L’interface d’administration est accessible à /admin.

Connexion via OAuth GitHub (par défaut avec Decap CMS).

Possibilité d’étendre avec Google (via un proxy ou Cloudflare Access) pour restreindre l’accès aux membres de l’association.

Les modifications se font via des commits ou PRs automatiques sur le dépôt.

📂 Structure du projet
/src            → Composants et pages Astro
/content        → Contenu éditable (pages, actus, événements, équipe...)
/public/images  → Images publiques (logos, photos, galeries)


Exemple de contenu :

/content/pages/accueil.md

/content/actus/2025-09-01-rentree.md

/content/equipe/effectif.yaml

⚙️ Workflow d’édition

Un éditeur se connecte à /admin avec son compte autorisé.

Il modifie une page, ajoute une actu ou téléverse une image.

Le CMS génère un commit (ou une Pull Request) dans le dépôt GitHub.

GitHub Actions reconstruit le site avec Astro.

Le site est automatiquement mis à jour sur GitHub Pages.

✅ Avantages

0 coût d’hébergement (GitHub Pages + Actions gratuits).

Édition simple via un back-office accessible en ligne.

Historique des contenus grâce à Git/GitHub.

Performances excellentes (site statique optimisé par Astro).

Accessible et inclusif : design responsive, bonnes pratiques d’accessibilité.

👉 Objectif : permettre à l’association de gérer son site en autonomie, sans dépendre d’un développeur au quotidien.