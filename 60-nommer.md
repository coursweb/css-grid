---
layout: page
title: Zones nommées
permalink: nommer.html
---

## Nommer les zones, nommer les lignes.

On a utilisé jusqu'ici les numéros des lignes pour placer des éléments. CSS Grid permet aussi d'attribuer des noms aux lignes et zones de la grille.

### Nommer les zones (zones nommées)

Il est possible d'assigner des noms à des zones de la grille. Cela facilite le placement des éléments. Les noms et emplacements des zones sont définis par la propriété "grid-template-areas". Exemple:

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas:
    "hd  hd   hd"
    "sd  main main"
    "ft  ft   ft";
}
```

On peut ensuite placer un élément sur l'un des emplacements, avec "grid-area":

```css
.footer {
  grid-area: ft;
}
```

Exemple:

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="jOwxvPy" data-editable="true" data-user="eracom" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/eracom/pen/jOwxvPy">
  Grid Layout</a> by Manuel Schmalstieg (<a href="https://codepen.io/eracom">@eracom</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Plus de détails dans la [documentation MDN](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas)

### Nommer les zones (zones nommées)

Il est également possible de nommer les "Grid Lines". Cela permet de les désigner autrement que par des numéros. On peut les nommer p.ex.  "content-start", "content-end".

La syntaxe pour nommer les Grid Lines:

```css
.container {
  grid-template-columns: 1fr [center-start] 1fr [center-end] 1fr;
}
```

Comme on le voit, on les définit en même temps que les colonnes.

- Article sur MDN: [Utiliser des lignes nommées](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines)
- Un article [explique cela en détail](https://mastery.games/post/naming-css-grid-lines/).

