# Les media queries en CSS3

## Introduction aux Media Queries

Les media queries sont une fonctionnalité puissante de CSS3 qui permet de créer des designs responsifs, c'est-à-dire des sites web qui s'adaptent à différentes tailles d'écrans et appareils.

## Syntaxe de base

La syntaxe de base d'une media query est la suivante :

```css
@media type-de-media and (condition) {
  /* Règles CSS */
}
```

## Types de média

Les types de média les plus courants sont :

- `screen` : pour les écrans d'ordinateurs, tablettes, smartphones
- `print` : pour l'impression
- `all` : pour tous les types de médias

## Conditions courantes

Les conditions les plus utilisées sont :

- `min-width` : largeur minimale de l'écran
- `max-width` : largeur maximale de l'écran
- `orientation` : orientation de l'appareil (portrait ou paysage)

## Exemple pratique

Voici un exemple simple :

```css
/* Style par défaut */
body {
  background-color: white;
}

/* Pour les écrans de moins de 600px de large */
@media screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

Dans cet exemple, le fond sera blanc par défaut, mais deviendra bleu clair sur les écrans de moins de 600px de large.

## Points de rupture courants

Voici quelques points de rupture couramment utilisés :

- Mobile : jusqu'à 600px
- Tablette : de 601px à 900px
- Desktop : au-dessus de 901px

## Combinaison de conditions

Vous pouvez combiner plusieurs conditions :

```css
@media screen and (min-width: 600px) and (max-width: 900px) {
  /* Styles pour les tablettes */
}
```

## ❗️Approche Mobile First

Une bonne pratique est d'adopter l'approche "Mobile First". Cela signifie que vous écrivez d'abord les styles pour les petits écrans, puis vous utilisez des media queries pour ajuster le design sur les écrans plus grands.

```css
/* Styles de base pour mobile */
.element {
  width: 100%;
}

/* Ajustements pour les écrans plus larges */
@media screen and (min-width: 768px) {
  .element {
    width: 50%;
  }
}
```

## Conclusion

Les media queries sont essentielles pour créer des sites web modernes et responsifs. En maîtrisant cette technique, vous pourrez adapter vos designs à une grande variété d'appareils, offrant ainsi une meilleure expérience utilisateur.

👉 N'oubliez pas de tester vos media queries sur différents appareils pour vous assurer que votre site s'affiche correctement partout.
