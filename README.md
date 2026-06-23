# FLOW - Référentiel d'Architecture

Ce dépôt contient le site documentaire MkDocs du programme FLOW.

## Objectif

Le référentiel vise à structurer progressivement :

1. l'introduction et la raison d'être du référentiel ;
2. la vision du programme FLOW ;
3. les principes directeurs d'architecture ;
4. les décisions d'architecture ;
5. l'architecture de référence FLOW ;
6. la cartographie du SI ;
7. la roadmap de transformation ;
8. la gouvernance du programme ;
9. les standards et patterns ;
10. le glossaire.

## Structure

```text
.
├── mkdocs.yml
├── requirements.txt
├── docs/
│   ├── index.md
│   ├── 1-introduction/
│   ├── 2-vision/
│   ├── 3-principes-directeurs/
│   ├── 4-adr/
│   ├── 5-architecture-reference/
│   ├── 6-cartographie-si/
│   ├── 7-roadmap-transformation/
│   ├── 8-gouvernance-programme/
│   ├── 9-standards-patterns/
│   └── 10-glossaire/
└── .github/workflows/deploy-mkdocs.yml
```

## Lancer en local

```bash
pip install -r requirements.txt
mkdocs serve
```

Le site local est disponible par défaut sur `http://127.0.0.1:8000`.

## Publication GitHub Pages

Le déploiement est géré par le workflow GitHub Actions `.github/workflows/deploy-mkdocs.yml`.

À vérifier dans GitHub :

1. **Settings > Pages**
2. Source : **GitHub Actions**
3. Le workflow `Deploy MkDocs site` se déclenche sur push vers `main` ou manuellement.

## Règle de contribution

Le contenu éditorial doit être ajouté en Markdown sous `docs/` puis référencé dans `mkdocs.yml`.

Ne pas ajouter de site HTML parallèle à la racine : MkDocs est la source de vérité du référentiel FLOW.
