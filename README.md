# Culture Quotidienne — Site statique (gratuit)
Un mini-site qui affiche chaque jour **10 fiches de culture générale** et un **quiz de 10 questions**. Tout fonctionne en **pur HTML/CSS/JS**, prêt pour **GitHub Pages** (gratuit).

## Structure
```
/content
  ├─ day001.json   # Jour 1 (exemple complet)
  └─ day002.json   # Modèle à compléter
index.html         # Le site (une seule page)
```

## Comment publier (GitHub Pages)
1. Crée un compte sur https://github.com si besoin.
2. Crée un **nouveau dépôt public** (par ex. `culture-quotidienne`).
3. **Glisse-dépose** les fichiers de ce dossier à la racine du dépôt.
4. Va dans **Settings → Pages**.
5. Dans **Build and deployment**, choisis **Source: Deploy from a branch**.
6. Choisis **Branch: main** et **/ (root)**, puis **Save**.
7. Dans 1–2 minutes, ton site sera accessible à l’URL : `https://TON-PSEUDO.github.io/culture-quotidienne`.

## Ajouter des jours
- Duplique `content/day001.json` en `content/day003.json`, `day004.json`…
- Mets à jour `meta.day` et `meta.title`.
- Conserve pour chaque sujet : `category`, `title`, `summary`, `points[]`, `quiz{question,choices[],answer,explanation}`.
- Dans `index.html`, ajuste la constante `AVAILABLE_DAYS` au **nombre total** de jours disponibles.

## Astuces
- La page détecte automatiquement le jour via la date courante et charge `content/dayXXX.json`. Tu peux aussi forcer un jour avec `?day=7` dans l’URL.
- Les scores sont mémorisés en local (`localStorage`), propre à chaque navigateur.

## Licence
MIT — fais-en ce que tu veux.
