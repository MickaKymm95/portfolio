# CLAUDE.md

Ce fichier fournit des informations contextuelles pour Claude Code afin de l'aider à comprendre et travailler efficacement sur ce projet.

## Vue d'ensemble du projet

Portfolio personnel construit avec **Astro** et **TailwindCSS**, intégrant **Decap CMS** (anciennement Netlify CMS) pour la gestion de contenu. Le site est optimisé pour le SEO et déployé sur Netlify.

## Stack technique

- **Framework** : Astro 2.5.5
- **Styling** : TailwindCSS 3.3.2
- **CMS** : Decap CMS (git-based)
- **Fonts** : Open Sans (@fontsource)
- **SEO** : astro-seo
- **Optimisation** : jampack
- **Langage** : TypeScript

## Structure du projet

```
src/
├── components/       # Composants Astro réutilisables
│   ├── seo/          # Composants SEO
│   └── shared/       # Composants partagés (BlurCircle, Link)
├── content/          # Contenu géré par le CMS
│   └── portfolio/    # Projets du portfolio
├── data/             # Configuration des données
│   ├── config.ts     # URL du site
│   ├── presentation.ts # Informations personnelles
│   ├── projects.ts   # Liste des projets
│   └── theme.ts      # Couleurs du thème
├── layouts/          # Layouts Astro
├── pages/            # Pages du site
│   ├── index.astro   # Page d'accueil
│   └── posts/        # Blog posts
├── styles/           # Styles globaux
└── utils/            # Fonctions utilitaires
```

## Commandes de développement

```bash
npm install          # Installer les dépendances
npm run dev          # Serveur de développement (localhost:3000)
npm run build        # Build de production (./dist/)
npm run preview      # Prévisualiser le build
```

## Points de personnalisation

### Données personnelles
- `src/data/presentation.ts` : Nom, description, email, liens sociaux
- `src/data/projects.ts` : Liste des projets à afficher
- `src/data/config.ts` : URL du site (SITE_URL)
- `src/data/theme.ts` : Couleurs du thème (primary, blur)

### Couleurs disponibles (TailwindCSS)
Les couleurs du thème acceptent les valeurs Tailwind standard : orange, violet, blue, red, green, etc.

### Contenu
- Articles de blog : écrire en Markdown dans `src/content/posts/`
- Projets portfolio : `src/content/portfolio/`

## Conventions de code

- Composants Astro avec extension `.astro`
- TypeScript pour les fichiers de données et utilitaires
- Formatage avec Prettier (plugin Astro + TailwindCSS)
- Linting avec ESLint (plugin Astro)

## Déploiement

Le site est conçu pour être déployé sur **Netlify** avec authentification GitHub OAuth pour le CMS. Voir le README.md pour la configuration OAuth.

## Notes importantes

- Le markdown supporte la coloration syntaxique Shiki avec le thème "nord"
- Le sitemap est généré automatiquement via @astrojs/sitemap
- Les images sont optimisées automatiquement par jampack lors du build
