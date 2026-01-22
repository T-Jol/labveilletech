+++
title = "Marketing Skills for Claude Code"
date = 2026-01-21T10:00:00+01:00
draft = false
description = "Une collection de 24 compétences IA pour agents marketing : CRO, copywriting, SEO, analytics et growth engineering. Des skills markdown qui donnent à Claude Code les frameworks et meilleures pratiques pour optimiser automatiquement les tâches marketing."
categories = ["AI & Automatisation (MarTech)", "Web-UX & CRO"]
tags = ["IA", "Automatisation", "MarTech", "CRO", "SEO", "Copywriting", "Analytics", "Growth", "Productivité"]
externalLink = "https://github.com/coreyhaines31/marketingskills"
+++

## Sujet Principal

Corey Haines a créé une collection open-source de 24 compétences (skills) pour agents IA, spécialement conçues pour les marketeurs techniques et fondateurs qui utilisent Claude Code (ou assistants IA similaires). Ces skills sont des fichiers markdown qui donnent aux agents IA des connaissances spécialisées et des workflows pour des tâches marketing spécifiques : optimisation de conversion, copywriting, SEO, analytics et growth engineering. Le projet permet à Claude Code de reconnaître automatiquement les tâches marketing et d'appliquer les bons frameworks et meilleures pratiques.

## Points Clés

### 1. Le concept de "Skills" pour agents IA

Les Skills sont des fichiers markdown qui :
- Donnent aux agents IA des connaissances spécialisées pour des tâches spécifiques
- Fournissent des workflows structurés et des frameworks éprouvés
- Permettent à Claude Code de reconnaître automatiquement le contexte marketing
- Appliquent les meilleures pratiques sans avoir à les réexpliquer à chaque fois

**Exemple d'utilisation :**
- Demander "Help me optimize this landing page for conversions" → Utilise automatiquement le skill `page-cro`
- Demander "Write homepage copy for my SaaS" → Utilise automatiquement le skill `copywriting`

### 2. Les 24 compétences disponibles

**Optimisation de Conversion (6 skills) :**
- `page-cro` : Optimisation de n'importe quelle page marketing
- `signup-flow-cro` : Flux d'inscription et d'enregistrement
- `onboarding-cro` : Activation post-inscription
- `form-cro` : Formulaires de capture de leads
- `popup-cro` : Modals et overlays
- `paywall-upgrade-cro` : Moments d'upgrade in-app

**Contenu & Copy (4 skills) :**
- `copywriting` : Copy pour pages marketing
- `copy-editing` : Édition et polissage de copy existant
- `email-sequence` : Flux d'emails automatisés
- `social-content` : Contenu pour réseaux sociaux

**SEO & Découverte (4 skills) :**
- `seo-audit` : SEO technique et on-page
- `programmatic-seo` : Génération de pages à grande échelle
- `competitor-alternatives` : Pages de comparaison et alternatives
- `schema-markup` : Données structurées

**Paid & Distribution (2 skills) :**
- `paid-ads` : Campagnes Google Ads, Meta, LinkedIn
- `social-content` : Stratégie et planification réseaux sociaux

**Mesure & Tests (2 skills) :**
- `analytics-tracking` : Configuration du tracking d'événements
- `ab-test-setup` : Design d'expériences

**Growth Engineering (2 skills) :**
- `free-tool-strategy` : Outils marketing et calculateurs
- `referral-program` : Programmes de parrainage et affiliation

**Stratégie & Monétisation (4 skills) :**
- `marketing-ideas` : 140 idées marketing SaaS
- `marketing-psychology` : Modèles mentaux et psychologie (70+)
- `launch-strategy` : Lancements produits et annonces
- `pricing-strategy` : Pricing, packaging et monétisation

### 3. Installation et intégration

**Option 1 : CLI Install (Recommandé)**
```bash
# Installer toutes les compétences
npx add-skill coreyhaines31/marketingskills

# Installer des compétences spécifiques
npx add-skill coreyhaines31/marketingskills --skill page-cro copywriting
```

**Option 2 : Plugin Claude Code**
- Installation via le système de plugins intégré de Claude Code
- Ajout du marketplace et installation des marketing skills

**Option 3 : Clone et copie manuelle**
- Clone du repository et copie du dossier skills dans `.claude/skills/`

**Option 4 : Git Submodule**
- Ajout comme submodule pour des mises à jour faciles

### 4. Structure et format des Skills

Chaque skill est un répertoire contenant un fichier `SKILL.md` :

```
skills/
  skill-name/
    SKILL.md
```

Le format suit une structure standardisée :
- Métadonnées (name, description) pour la sélection automatique
- Instructions complètes pour l'agent IA
- Frameworks et meilleures pratiques
- Exemples et cas d'usage

### 5. Cas d'usage concrets

**Optimisation de conversion :**
- "Optimize this landing page" → Skill `page-cro` applique les frameworks CRO
- "Improve my signup form" → Skill `form-cro` suggère des optimisations basées sur les meilleures pratiques

**Création de contenu :**
- "Write homepage copy" → Skill `copywriting` applique les principes de copywriting marketing
- "Create a 5-email welcome sequence" → Skill `email-sequence` structure le flux automatiquement

**SEO et découverte :**
- "Set up GA4 tracking for signups" → Skill `analytics-tracking` configure le tracking correctement
- "SEO audit my site" → Skill `seo-audit` analyse technique et on-page

**Stratégie :**
- "Marketing ideas for my SaaS" → Skill `marketing-ideas` propose 140 idées structurées
- "Design pricing tiers" → Skill `pricing-strategy` applique les modèles de pricing

### 6. Avantages pour les marketeurs techniques

**Gain de temps :** Plus besoin de réexpliquer les frameworks à chaque interaction avec l'IA.

**Cohérence :** Les meilleures pratiques sont appliquées systématiquement, pas seulement quand on s'en souvient.

**Scalabilité :** Les skills peuvent être partagés entre équipes et projets.

**Amélioration continue :** Le repository open-source permet d'améliorer les skills collectivement.

**Spécialisation :** Chaque skill est optimisé pour sa tâche spécifique, plutôt qu'une approche générique.

## Conclusion

Marketing Skills for Claude Code transforme la façon dont les marketeurs techniques interagissent avec les assistants IA. Au lieu de prompts génériques qui produisent des résultats variables, les skills fournissent des connaissances spécialisées et des workflows structurés pour chaque tâche marketing. Le projet open-source (3.3k stars sur GitHub) montre l'intérêt de la communauté pour standardiser l'utilisation de l'IA en marketing. Pour les équipes qui utilisent déjà Claude Code ou des assistants similaires, c'est un moyen d'améliorer immédiatement la qualité et la cohérence des outputs marketing, tout en accélérant le workflow quotidien.
