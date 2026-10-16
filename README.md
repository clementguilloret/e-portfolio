# E-Portfolio — Clément Guilloret

Site personnel réalisé avec [al-folio](https://github.com/alshedivat/al-folio) et hébergé par **GitHub Pages**.

**Adresse prévue :** https://clementguilloret.github.io/e-portfolio/

## Navigation

Les six rubriques sont sur **une seule page**, avec des liens qui font défiler le site :

- Welcome
- Engineering course (Projects, Productions)
- International Mobility (PCE, LV2)
- Sustainability & Civic Engagement
- Sport & other activities
- Career Development (Internships, PEP)

## Modifier le contenu

- **Textes et sections :** [`_pages/about.md`](_pages/about.md)
- **Informations générales et URL :** [`_config.yml`](_config.yml)
- **Photo de profil :** remplace `assets/img/profil_cg.png` par ton image (ou change la propriété `profile.image` dans `about.md`)
- **Liens sociaux :** [`_data/socials.yml`](_data/socials.yml)
- **Styles du menu de navigation :** [`assets/css/eportfolio.css`](assets/css/eportfolio.css)

Voir [GUIDE_PERSONNALISATION.md](GUIDE_PERSONNALISATION.md) pour les étapes de publication et les conseils de personnalisation.

## Hébergement

Le dépôt utilise le workflow al-folio existant `.github/workflows/deploy.yml` pour construire et publier le site sur la branche `gh-pages`. Dans GitHub **Settings → Pages**, sélectionner la branche **`gh-pages`**, dossier **`/(root)`**.

Le template al-folio original est conservé ; les pages de démonstration et collections d'exemples sont exclues de la publication dans `_config.yml`.
