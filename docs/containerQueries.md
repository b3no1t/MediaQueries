# Container queries en CSS

## Introduction aux Container Queries

Les container queries sont une nouvelle fonctionnalité CSS qui permet de styler des éléments en fonction de la taille de leur conteneur parent, plutôt que de la taille de la fenêtre du navigateur comme le font les media queries traditionnelles.

## Pourquoi utiliser les Container Queries ?

Les container queries résolvent plusieurs problèmes :

1. Elles permettent de créer des composants vraiment réutilisables qui s'adaptent à leur contexte.
2. Elles offrent un contrôle plus précis sur le style des éléments dans différentes mises en page.
3. Elles simplifient la création de designs responsifs complexes.

## Syntaxe de base

### Définir un conteneur

Pour utiliser les container queries, vous devez d'abord définir un élément comme conteneur :

```css
.container {
  container-type: inline-size;
}
```

### Écrire une container query

Ensuite, vous pouvez écrire des règles CSS qui s'appliquent en fonction de la taille du conteneur :

```css
@container (min-width: 400px) {
  .element {
    /* Styles à appliquer quand le conteneur fait au moins 400px de large */
  }
}
```

## Types de conteneurs

Il existe deux types principaux de conteneurs :

1. `inline-size` : permet de faire des requêtes basées sur la largeur du conteneur.
2. `size` : permet de faire des requêtes basées sur la largeur et la hauteur du conteneur.

## Unités spécifiques aux container queries

Les container queries introduisent de nouvelles unités relatives à la taille du conteneur :

- `cqw` : 1% de la largeur du conteneur
- `cqh` : 1% de la hauteur du conteneur
- `cqi` : 1% de la taille inline du conteneur
- `cqb` : 1% de la taille block du conteneur

## Exemple pratique

Voici un exemple concret d'utilisation des container queries :

```html
<div class="card-container">
  <div class="card">
    <img src="image.jpg" alt="Card image">
    <h2>Titre de la carte</h2>
    <p>Description de la carte</p>
  </div>
</div>
```

```css
.card-container {
  container-type: inline-size;
}

.card {
  display: flex;
  flex-direction: column;
}

@container (min-width: 300px) {
  .card {
    flex-direction: row;
  }
  
  .card img {
    width: 40%;
  }
}
```

Dans cet exemple, la disposition de la carte change de verticale à horizontale lorsque son conteneur atteint une largeur de 300px.

## Avantages par rapport aux Media Queries

1. Modularité : les composants peuvent s'adapter indépendamment de la taille de l'écran.
2. Réutilisabilité : un même composant peut s'adapter à différents contextes.
3. Précision : permet un contrôle plus fin sur le comportement des éléments.

## Compatibilité et utilisation

Les container queries sont supportées dans les versions récentes des principaux navigateurs. Cependant, pour une utilisation en production, il est recommandé de vérifier la compatibilité et d'envisager des fallbacks pour les navigateurs plus anciens.

## Conclusion

Les container queries représentent une avancée majeure dans la création de designs web responsifs et modulaires. En permettant aux composants de s'adapter à leur contexte immédiat plutôt qu'à la taille globale de l'écran, elles offrent aux développeurs une flexibilité et une précision sans précédent dans la conception d'interfaces web adaptatives.

