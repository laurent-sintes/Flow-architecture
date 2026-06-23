# FLOW Architecture

Mini-site statique de cadrage pour le programme d’entreprise FLOW.

## Objectif

Ce dépôt sert à prototyper rapidement une documentation navigable autour de :

1. Vision & ambition
2. Programme d’entreprise
3. Business capabilities
4. Architecture cible
5. Roadmap

## Structure

```text
.
├── index.html
├── assets/
│   └── styles.css
└── pages/
    ├── 01-vision.html
    ├── 02-programme.html
    ├── 03-capabilities.html
    ├── 04-architecture.html
    └── 05-roadmap.html
```

## Publication GitHub Pages

Dans GitHub :

1. Aller dans **Settings > Pages**.
2. Source : **Deploy from a branch**.
3. Branch : **main**.
4. Folder : **/** root.
5. Sauvegarder.

Le site sera ensuite accessible via l’URL GitHub Pages du dépôt.

## Prochaines évolutions possibles

- Ajouter une page de glossaire FLOW.
- Ajouter une cartographie applicative SVG.
- Ajouter une page par capability.
- Ajouter un dossier `docs/` ou `content/` si l’on veut séparer contenu et rendu.
- Transformer ensuite le site en Astro, VitePress ou Docusaurus si le besoin grandit.
