# Site Ludiverse Traduction - Jekyll

Site web bilingue (FR/EN) pour Ludiverse Traduction, spécialisé dans la traduction de jeux de société.

## Prérequis

- Ruby 3.0+ et Bundler
- Jekyll 4.3+
- Node.js (optionnel, pour les outils de développement)

## Installation

1. **Cloner le repository**
   ```bash
   git clone [URL-DU-REPO]
   cd ludiverse-traduction
   ```

2. **Installer les dépendances**
   ```bash
   bundle install
   ```

3. **Lancer le serveur de développement**
   ```bash
   bundle exec jekyll serve --livereload
   ```

4. **Accéder au site**
   - Site français : http://localhost:4000/
   - Site anglais : http://localhost:4000/en/

## Structure du projet

```
ludiverse-traduction/
├── _config.yml           # Configuration Jekyll
├── _data/
│   ├── translations.yml  # Traductions UI
│   ├── portfolio.yml     # Données portfolio
│   ├── pricing.yml       # Données tarifs
│   └── navigation.yml    # Menu navigation
├── _includes/
│   ├── header.html
│   ├── footer.html
│   └── language-switcher.html
├── _layouts/
│   ├── default.html
│   ├── page.html
│   ├── post.html
│   └── portfolio-item.html
├── assets/
│   ├── css/main.scss     # Styles principaux
│   ├── js/main.js        # JavaScript
│   └── images/           # Images du site
├── fr/                   # Pages françaises
└── en/                   # Pages anglaises
```

## Configuration multilingue

Le site utilise le plugin `jekyll-polyglot` pour la gestion multilingue :

- **Langue par défaut** : Français (fr)
- **Langues disponibles** : Français (fr) et Anglais (en)
- **URLs** :
  - FR : `/` ou `/fr/page`
  - EN : `/en/page`

### Ajouter du contenu multilingue

1. **Pages** : Créer les fichiers dans `/fr/` et `/en/`
2. **Traductions UI** : Modifier `_data/translations.yml`
3. **Données** : Ajouter les sections correspondantes dans les fichiers `_data/`

## Pages disponibles

### Français
- Accueil : `/`
- Portfolio : `/portfolio/`
- À propos : `/a-propos/`
- Tarifs : `/tarifs/`
- Blog : `/blog/`
- Contact : `/contact/`

### Anglais
- Home : `/en/`
- Portfolio : `/en/portfolio/`
- About : `/en/about/`
- Pricing : `/en/pricing/`
- Blog : `/en/blog/`
- Contact : `/en/contact/`

## Gestion du portfolio

Les projets du portfolio sont définis dans `_data/portfolio.yml` :

```yaml
fr:
  projects:
    - title: "Nom du jeu"
      client: "Nom du client"
      category: "board-games" # board-games, card-games, role-playing
      image: "/assets/images/portfolio/image.jpg"
      languages: "Français → Anglais"
      word_count: "5000"
      services:
        - "Service 1"
        - "Service 2"
      description: "Description du projet"
      testimonial: "Témoignage client"
```

## Tarifs

Les formules tarifaires sont configurées dans `_data/pricing.yml` :

```yaml
fr:
  plans:
    - name: "Classique"
      price: "0,08€"
      unit: "par mot"
      features:
        - "Feature 1"
        - "Feature 2"
      popular: false # true pour mettre en avant
```

## Déploiement

### GitHub Pages
1. Pousser le code sur GitHub
2. Activer GitHub Pages dans les paramètres
3. Le site sera disponible sur `username.github.io/repo-name`

### Netlify
1. Connecter le repository GitHub à Netlify
2. Configuration build :
   - Build command : `bundle exec jekyll build`
   - Publish directory : `_site`
3. Variables d'environnement :
   - `JEKYLL_ENV` = `production`

### Serveur personnalisé
```bash
# Build du site
bundle exec jekyll build

# Les fichiers sont générés dans _site/
# Copier le contenu sur votre serveur web
```

## Personnalisation

### Couleurs et design
Modifier les variables SCSS dans `assets/css/main.scss` :

```scss
$primary-color: #2951d5;
$secondary-color: #26262c;
$accent-color: #ff6b6b;
```

### Polices
Les polices sont définies dans le layout `default.html` :
- Titres : "DM Serif Display"
- Corps de texte : "Work Sans"

### Images
- Logos et favicons : `/assets/images/`
- Portfolio : `/assets/images/portfolio/`
- Blog : `/assets/images/blog/`

## Développement

### Structure CSS
Le CSS est organisé en SCSS avec une architecture modulaire :

```
assets/css/main.scss
├── Variables (couleurs, polices, breakpoints)
├── Reset & Base styles
├── Layout (header, footer, navigation)
├── Components (buttons, cards, forms)
└── Pages (styles spécifiques par page)
```

### JavaScript
Le JavaScript principal est dans `assets/js/main.js` et inclut :
- Navigation mobile
- Filtres portfolio
- Lazy loading images
- Smooth scroll

## SEO et Performance

- **SEO** : Plugin `jekyll-seo-tag` configuré
- **Sitemap** : Généré automatiquement avec `jekyll-sitemap`
- **RSS** : Feed RSS avec `jekyll-feed`
- **Images** : Lazy loading implémenté
- **Compression** : HTML compressé en production

## Support navigateurs

- Chrome, Firefox, Safari, Edge (dernières versions)
- Mobile responsive (breakpoints à 768px et 992px)
- Support IE11 avec polyfills si nécessaire

## Contribuer

1. Fork le projet
2. Créer une branche feature (`git checkout -b feature/amelioration`)
3. Commit les changements (`git commit -am 'Ajout fonctionnalité'`)
4. Push la branche (`git push origin feature/amelioration`)
5. Créer une Pull Request

## Support

Pour toute question ou problème :
- Créer une issue sur GitHub
- Consulter la documentation Jekyll : https://jekyllrb.com/docs/