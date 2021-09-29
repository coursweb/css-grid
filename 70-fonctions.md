---
layout: page
title: Fonctions CSS
permalink: fonctions.html
---

Le module Grid Layout permet d'utiliser des fonctions CSS pour faciliter la création de grilles responsives:

- `repeat()` : pour éviter de devoir se répéter dans le code.
- `auto-fit` : pour ne pas spécifier le nombre de rangées ou colonnes, qui s'adaptera selon les contenus.
- `minmax()` : unité de mesure souple, permet de définir un minimum et maximum.

## La fonction repeat()

Au lieu de répéter les unités des colonnes, on peut faire usage de cette fonction. Ainsi, ce code:

```css
.container {
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
}
```

est équivalent à ceci :

```css
.container {
  grid-template-columns: repeat(6, 1fr);
}
```

La première valeur donne le nombre de colonnes à créer, la deuxième la largeur.

## auto-fit et auto-fill

Il y a encore mieux: on peut décider que le nombre de colonnes s'adapte selon la largeur de l'écran. Au lieu d'indiquer un chiffre, on utilisera le mot-clé `auto-fit` (ou `auto-fill`).

Exemple:

```css
.container {
  grid-template-columns: repeat(auto-fit, 250px);
}
```

Voir sur Codepen: [https://codepen.io/eracom/pen/yLXjxbP?editors=1100](https://codepen.io/eracom/pen/yLXjxbP?editors=1100)


## Tailles flexibles avec minmax()

C'est pas mal... mais il y a encore mieux: on peut rendre la largeur des boîtes flexible avec `minmax()`. On définit un minimum et un maximum.

```css
.container {
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
}
```

<p class="codepen" data-height="300" data-default-tab="css,result" data-slug-hash="OJgZozR" data-editable="true" data-user="eracom" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/eracom/pen/OJgZozR">
  repeat, autofill et minmax</a> by Manuel Schmalstieg (<a href="https://codepen.io/eracom">@eracom</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## grid-auto-flow : dense

Dernière astuce: on peut demander à l'algorithme de placement automatique d'utiliser une méthode de « regroupement dense » où il essaie de remplir les trous dans la grille, en changeant l'ordre des éléments si nécessaire. 

Il faut ajouter cette déclaration sur le conteneur:

```css
.container {
  grid-auto-flow : dense;
}
```

Voilà! Avec cette technique, vous pouvez définir des grilles qui s'adapteront de manière très flexible à l'espace disponible.
