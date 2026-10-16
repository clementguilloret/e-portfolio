# Guide de personnalisation et de publication

## 1. Ce que j'ai adapté

Tu pars bien du vrai template **al-folio (v1.x)**. J'ai conservé son moteur Jekyll, son design, sa gestion responsive et ses workflows GitHub.

- `_pages/about.md` : page principale en Markdown avec six sections + sous-sections et menu d'ancres.
- `_config.yml` : nom, langue, adresse GitHub Pages, démos masquées à la publication.
- `_data/socials.yml` : suppression des contacts et réseaux d'exemple (seul ton GitHub est prérempli).
- `assets/css/eportfolio.css` : mini barre de navigation collante, compatible avec les modes clair/sombre.
- `assets/img/profil_cg.png` : image provisoire avec initiales, **pas une vraie photo**.
- `README.md` : documentation du dépôt.

Les démos al-folio restent dans le code source mais **ne sont pas publiées** grâce au paramètre `exclude:` de `_config.yml` ; tu pourras les réactiver si tu décides d'ajouter des pages plus tard.

## 2. Mettre en ligne

### Option conseillée : modifier ton dépôt existant avec les quelques fichiers changés

1. Décompresse `fichiers-a-ajouter-au-depot.zip`.
2. Copie les fichiers et dossiers **dans ton dépôt existant** en conservant la même arborescence (`_pages/about.md` doit écraser l'ancien `_pages/about.md`).
3. Valide les modifications (GitHub Desktop ou `git add ...`, `git commit`, `git push`).
4. Dans GitHub : **Settings → Actions → General → Workflow permissions**, autorise **Read and write permissions** si nécessaire.
5. Dans **Actions**, attends que le workflow **Deploy site** soit vert. Il doit créer / alimenter la branche `gh-pages`.
6. Dans **Settings → Pages**, sélectionne **Deploy from a branch**, branche **gh-pages**, dossier **/(root)**.
7. Visite https://clementguilloret.github.io/e-portfolio/ (l'adresse fonctionne après la première publication réussie).

> Ne téléverse **pas** le fichier ZIP directement comme s'il était le site : il faut **décompresser** et ajouter les vrais fichiers dans le dépôt.

### Autre option : archive complète

`e-portfolio-complet-personnalise.zip` est une copie complète de ton ZIP source, déjà modifiée. Décompresse-la localement, puis remplace les fichiers du dépôt par son contenu si tu préfères repartir de cette version. Cela contient beaucoup de fichiers de démonstration inutiles à changer.

## 3. Contenu à remplacer

Le contenu de chaque rubrique se trouve dans `_pages/about.md`. Remplace les passages `[À renseigner]`, `[Nom du projet]`, etc. sans supprimer les identifiants ` {#...}` des titres : ce sont les cibles des liens de navigation.

- La photo actuelle est un emplacement réservé ; pour utiliser ta photo, place une image dans `assets/img/` et mets son nom dans `profile.image` de `_pages/about.md`.
- Pour ajouter des PDF, range-les dans `assets/pdf/` et utilise des liens Markdown compatibles avec le sous-chemin du site, par exemple :
  `[Rapport (PDF)]({{ '/assets/pdf/mon-rapport.pdf' | relative_url }})`
- Pour ajouter un projet, duplique simplement le modèle du **Projet 01** dans la section Engineering course.
- Si tu changes le nom du dépôt GitHub, adapte `baseurl` dans `_config.yml`.
- Si tu ajoutes des pages, retire-les de `exclude:` et remets `nav: true` dans leur en-tête si tu veux les afficher dans le menu du thème.

## 4. À savoir

- La barre de navigation des 6 sections utilise les ancres HTML de la **même page**, et non des pages distinctes.
- Les intitulés des six rubriques sont en anglais, comme sur ton plan initial. Les descriptions sont actuellement en français : tu peux les traduire.
- Le CSS a un fallback clair/sombre basé sur les variables du thème al-folio.
- **Le déploiement réel n'a pas été exécuté** dans cet environnement ; vérifie le résultat dans l'onglet Actions de ton dépôt après avoir poussé les fichiers.
