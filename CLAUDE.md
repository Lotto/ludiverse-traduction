# Site Ludiverse Traduction - Jekyll

## Vue d'ensemble
Site web bilingue (FR/EN) pour Ludiverse Traduction, spécialisé dans la traduction de jeux de société.

## Objectifs
- Présenter les services de traduction ludique
- Afficher un portfolio des jeux traduits
- Proposer trois formules tarifaires (Classique, Premium, Ultimate)
- Site moderne et adapté au secteur ludique
- Navigation bilingue complète

## Structure des pages

### Page d'accueil
- Présentation rapide de l'activité
- Aperçu visuel du portfolio
- Mise en avant des formules tarifaires
- Call-to-action vers contact

### Portfolio
- Galerie des jeux traduits
- Visuels et descriptifs pour chaque jeu
- Filtres par type/catégorie

### À propos
- Présentation du parcours
- Compétences et expertise
- Valeurs de l'entreprise

### Formules & Tarifs
- Détail des trois formules :
  - Classique : Services de base
  - Premium : Services intermédiaires
  - Ultimate : Services complets
- Prix et services inclus pour chaque formule

### Contact
- Formulaire de contact
- Informations de contact directes
- Liens réseaux sociaux

### Blog
- Articles sur la traduction ludique
- Actualités du secteur
- Conseils et ressources

## Technologies utilisées
- **Jekyll** : Générateur de site statique
- **Liquid** : Templating
- **SCSS** : Styles
- **JavaScript** : Interactions
- **Jekyll-polyglot** : Gestion multilingue

## Configuration multilingue
- Langues : Français (défaut) et Anglais
- URLs : 
  - FR : /fr/page ou /page
  - EN : /en/page
- Traductions dans _data/translations.yml

## Design
- **Couleurs principales** :
  - Bleu : #2951d5
  - Gris foncé : #26262c
  - Blanc : #ffffff
  - Accent : À définir
- **Typographie** :
  - Titres : "DM Serif Display"
  - Corps : "Work Sans"
- **Style** : Moderne, épuré, professionnel avec touches ludiques

## Fonctionnalités
- Navigation responsive
- Galerie photo avec lightbox
- Formulaire de contact
- Switch de langue
- Animations subtiles
- SEO optimisé
- Performance optimisée

## Structure des fichiers
```
ludiverse-traduction/
├── _config.yml           # Configuration Jekyll
├── _data/
│   ├── translations.yml  # Traductions UI
│   ├── portfolio.yml     # Données portfolio
│   └── pricing.yml       # Données tarifs
├── _includes/
│   ├── header.html
│   ├── footer.html
│   ├── navigation.html
│   └── language-switcher.html
├── _layouts/
│   ├── default.html
│   ├── page.html
│   ├── post.html
│   └── portfolio.html
├── _posts/
│   ├── fr/              # Articles FR
│   └── en/              # Articles EN
├── _sass/
│   ├── base/
│   ├── components/
│   └── pages/
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
├── fr/                   # Pages FR
│   ├── index.html
│   ├── portfolio.html
│   ├── about.html
│   ├── pricing.html
│   └── contact.html
└── en/                   # Pages EN
    ├── index.html
    ├── portfolio.html
    ├── about.html
    ├── pricing.html
    └── contact.html
```

## Commandes
```bash
# Installation
bundle install

# Développement
bundle exec jekyll serve --livereload

# Build production
bundle exec jekyll build

# Linter SCSS
npm run lint:scss
```

## Déploiement
- Hébergement : À définir (GitHub Pages, Netlify, ou autre)
- Domaine : ludiverse-traduction.fr
- SSL : Certificat Let's Encrypt

## Notes importantes
- Optimiser toutes les images (WebP avec fallback)
- Implémenter lazy loading pour les images
- Assurer l'accessibilité WCAG 2.1 AA
- Tester sur tous les navigateurs modernes
- Responsive design mobile-first