---
layout: page
title: Initialisation
permalink: initialisation.html
---

## Initialisation de la grille

Voici comment déclarer une grille CSS:

```css
.container {
  display: grid;
}
```

Avec la propriété `display: grid`, on définit le conteneur. Pour que la grille fonctionne visuellement, il faut aussi spécifier les colonnes et rangées.

### Déclaration des colonnes et rangées

Les trois propriétés suivantes permettent différentes manières de définir des colonnes ou rangées:

- `grid-template-rows` : spécifie le nombre et la hauteur des rangées (rows)
- `grid-template-columns` : spéficie le nombre et la largeur des colonnes.
- `grid-template-areas` : permet d'associer un nom aux zones de la grille.

Exemple: pour déclarer deux colonnes de largeur égale, on peut procéder ainsi:

```css
.container {
  display: grid;
  grid-template-columns: 50% 50%;
}
```