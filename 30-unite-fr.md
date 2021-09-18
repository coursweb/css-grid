---
layout: page
title: L’unité fr
permalink: unite-fr.html
---

#### L'unité fr

On peut aussi utiliser une nouvelle unité CSS, conçue spécialement pour faciliter la conception de grilles: l'unité `fr`, qui signifie "fraction". Cette unité désigne une fraction de l'espace disponible.

Ainsi, si on écrit:

```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr;
}
```

La première colonne aura une largeur de 200 pixels. La seconde colonne occupera tout l'espace restant.

Si on veut créer une grille de 4 colonnes, avec ces proportions: 25% 25% 25% 25%. On pourra écrire: `grid-template-columns: 1fr 1fr 1fr 1fr;`