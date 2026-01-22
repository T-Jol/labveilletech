# LabVeiltech

> Laboratoire de veille technologique sur le Growth Marketing, l'IA et l'optimisation

Blog statique documentant l'exploration continue à l'intersection du marketing data-driven, de l'intelligence artificielle, de l'automatisation et de l'optimisation publicitaire/web.

🌐 **Site en ligne :** [https://t-jol.github.io/labveilletech/](https://t-jol.github.io/labveilletech/)

## À propos

**LabVeiltech** est un blog de veille technologique structuré autour de 7 piliers (taxonomies) qui représentent les leviers majeurs de la croissance moderne :

1. **AI & Automatisation (MarTech)** - LLM, Chatbots, Personnalisation IA, MarTech Stack
2. **Meta-Creative & Ads** - Stratégie créative, Hooks visuels, Formats publicitaires
3. **Web-UX & CRO** - Design minimaliste, Performance web, Conversion Rate Optimization
4. **Activation & Psychologie** - Biais cognitifs, Nudges, Onboarding utilisateur
5. **Benchmarks & Stratégie** - Analyses concurrentielles, Market Insights, Études de cas
6. **Modeling & Analytics** - Media Mix Modeling, Attribution Data-Driven, Prédictif
7. **Impact & Growth Positif** - Growth pour causes utiles, Fundraising Tech, ONG/Impact

### Contexte

Ce projet a été développé dans le cadre d'un cours de veille technologique (M52-1). Il répond aux exigences suivantes :

- Blog traitant du domaine de veille (Growth Marketing & Optimisation)
- 3 articles (résumés d'informations dénichées)
- 1 article sur l'utilisation des LLM pour se former
- 1 article expliquant le système d'écoute mis en place
- Page "À propos" expliquant le domaine, l'Ikigai, les taxonomies et le choix du SSG

## Technologies

- **Hugo** (Static Site Generator) - Version minimale : 0.124.0
- **Thème Coder** - Thème minimaliste et responsive
- **Markdown** - Rédaction des articles
- **Git** - Version control
- **GitHub** - Hébergement du code source et déploiement via GitHub Pages
- **GitHub Actions** - CI/CD pour le déploiement automatique

## Installation et lancement

### Prérequis

- [Hugo](https://gohugo.io/installation/) (version 0.124.0 ou supérieure)
- Git

### Installation

1. Cloner le repository :
```bash
git clone https://github.com/T-Jol/labveilletech.git
cd labveilletech/labveiletech
```

2. Le thème Coder est inclus comme sous-module dans `themes/Coder/`

### Développement local

Lancer le serveur de développement :

```bash
hugo serve -F
```

Le site sera accessible sur `http://localhost:1313`

**Note :** Le flag `-F` permet d'afficher les articles avec une date future.

### Build de production

Générer le site statique :

```bash
hugo
```

Les fichiers générés seront dans le dossier `public/`.

### Déploiement

Le site est automatiquement déployé sur **GitHub Pages** via GitHub Actions à chaque push sur la branche `main`.

Le workflow GitHub Actions :
1. Déclenchement automatique lors d'un push sur `main`
2. Build du site avec Hugo
3. Déploiement sur `https://t-jol.github.io/labveilletech/`

Le site est accessible à l'adresse : [https://t-jol.github.io/labveilletech/](https://t-jol.github.io/labveilletech/)

## Structure du projet

```
labveiletech/
├── content/              # Contenu du site
│   ├── about.md         # Page "À propos"
│   └── posts/           # Articles du blog
├── layouts/             # Templates personnalisés
│   ├── _default/        # Templates par défaut
│   ├── _partials/       # Partials réutilisables
│   └── posts/           # Templates spécifiques aux articles
├── static/              # Fichiers statiques (images, etc.)
│   └── images/          # Images optimisées
├── themes/              # Thèmes Hugo
│   └── Coder/           # Thème Coder
├── hugo.toml            # Configuration Hugo
└── public/              # Site généré (ignoré par Git)
```

## Fonctionnalités

### Articles

- **Articles réguliers** : Résumés d'informations dénichées sur le Growth Marketing
- **Articles personnels** : Articles méthodologiques avec badge "Taxonomie" ou "Méthodologie"
  - Layout deux colonnes pour les articles personnels
  - Bannières d'images en haut des cartes (support via paramètre `bannerImage`)
- **Filtrage par catégorie** : Système de filtres multiples sur la page `/posts`
  - Filtres par catégorie avec sélection multiple
  - Affichage des filtres actifs
  - Animation fade-in/fade-out lors du filtrage
- **Charger plus d'articles** : Affichage progressif (2 articles initialement)
- **Lien externe** : Chaque article peut inclure un lien vers la source originale
- **Design uniforme** : Cartes avec style minimaliste et cohérent sur toute la page

### Navigation

- **Page d'accueil** : Liste des articles récents
- **Page Articles** (`/posts`) : Liste complète avec filtres par catégorie
- **Page À propos** (`/about`) : Présentation du domaine, Ikigai, taxonomies et outils
- **Pages catégories** : Filtrage automatique par taxonomie
- **Pages tags** : Navigation par mots-clés

### UX/UI

- **Mode sombre/clair** : Adaptation automatique selon les préférences système
- **Design responsive** : Optimisé pour mobile, tablette et desktop
- **Animations** : Effets de survol sur les articles et boutons
  - Hover avec élévation subtile (`translateY(-4px)`)
  - Zoom sur les bannières d'images au survol
  - Transitions fluides avec `cubic-bezier`
- **Design minimaliste** : Cartes uniformes avec bordures subtiles et espacements cohérents
- **Accessibilité** : Structure sémantique et navigation clavier

## Créer un nouvel article

1. Créer un fichier `.md` dans `content/posts/`
2. Ajouter le front matter :

```yaml
+++
title = "Titre de l'article"
date = 2026-01-XXT10:00:00+01:00
draft = false
description = "Description courte de l'article"
categories = ["Catégorie"]
tags = ["Tag1", "Tag2"]
externalLink = "https://lien-externe.com"  # Optionnel
articleType = "formation"  # Optionnel, pour articles personnels
badgeLabel = "Taxonomie"   # Optionnel, label du badge
bannerImage = "/images/nom-image.jpg"  # Optionnel, bannière en haut de la carte
+++
```

3. Rédiger le contenu en Markdown

## Personnalisation

### Modifier les templates

Les templates personnalisés se trouvent dans `layouts/` :
- `layouts/posts/list.html` : Page de liste des articles
- `layouts/posts/single.html` : Page d'article individuel
- `layouts/posts/li.html` : Template d'un article dans une liste
- `layouts/_default/single.html` : Template pour pages simples (About)

### Modifier la configuration

Éditer `hugo.toml` pour modifier :
- Titre du site
- Auteur
- Format de date
- Menu de navigation
- Paramètres du thème

## Articles disponibles

### Articles réguliers
- Google's AI Chat & Shopping
- L'IA dans les campagnes Marketing 2026
- Growth Positif pour ONG & Fundraising
- 30 ans de publicité en ligne
- Psychologie des boutons
- Psychologie des landing pages
- Lovable System After 45+ MVPs
- Marketing Skills for Claude Code

### Articles personnels (Méthodologie)
- Pagination et Ikigai : Comment structurer sa veille
- Ma méthode de recherche et de veille
- Transformer l'IA en tuteur personnel

## Contribution

Ce projet est un travail académique, mais les suggestions d'amélioration sont les bienvenues via des issues ou pull requests.

## Licence

Ce projet est un travail académique. Le thème [Coder](https://github.com/luizdepra/hugo-coder) est sous licence MIT.

## Développement

### Étapes de développement

1. **Initialisation du projet Hugo** avec le thème Coder
2. **Personnalisation des templates** :
   - Création de templates personnalisés pour les articles (`layouts/posts/`)
   - Amélioration de l'UX/UI avec design minimaliste et uniforme
   - Implémentation du système de filtrage par catégorie
3. **Optimisation des images** : Conversion PNG vers JPEG pour améliorer les performances
4. **Configuration GitHub Pages** : Déploiement automatique via GitHub Actions
5. **Refactorisation du design** : Uniformisation des cartes d'articles avec bannières d'images
6. **Amélioration de l'espacement** : Uniformisation des espacements pour une meilleure lisibilité

### Workflow de développement

1. Développement local avec `hugo serve -F`
2. Tests et ajustements
3. Commit et push sur GitHub
4. Déploiement automatique via GitHub Actions
5. Site mis à jour sur GitHub Pages

## Auteur

**Thibaud J - M52-1**

- Site : [LabVeiltech](https://t-jol.github.io/labveilletech/)
- GitHub : [@T-Jol](https://github.com/T-Jol)

---

*Dernière mise à jour : Janvier 2026*
