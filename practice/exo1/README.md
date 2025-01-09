# Responsive web

> Vous allez adapter ce site pour les formats mobile !
> [Robbie Lens](https://openclassrooms-student-center.github.io/1603881-creez-votre-site-web-avec-html5-et-css3/portfolio.html)

## Todo

 1. Analyser le code du site desktop de Robbie Lens
 2. Créer une version mobile du site.

 2.1 Réduisez la taille des titres à `2em`

 2.2 Remplacez les  width  pour `.accueil-introduction`  et  `form`  par la propriété  `max-width`  sur la page d'accueil, avec une valeur de `1000px`  .

 2.3 Cachez la section "Tarifs" sur la page "À propos".

 2.4 Tous les éléments qui sont disposés à l'horizontale basculent à la verticale à partir de la taille d'écran  996px  (introduction, grilles photos et formulaire).

 2.5 Le  padding  sur le côté des pages passe de  80px  à  20px  .

 2.6 Les liens de navigation du header passent à la verticale et sont centrés.

## En bref

Pour adapter un site internet aux différentes tailles d'écran, plusieurs techniques sont nécessaires :

Il faut tout d'abord réussir à sélectionner les différentes tailles d'écran disponibles, afin d'appliquer le style souhaité.
Pour cela, on a recours aux `media queries` qui sont la manière de "conditionner" le style appliqué : "Si l'écran de l'utilisateur est plus petit que la taille `XXXpx`, alors appliquer ce style".

Il est ensuite possible d'utiliser les différentes astuces :

`display: none`  pour cacher un élément qui ne rentre pas sur les tailles d'écran plus petites ;

`overflow`  pour permettre de scroller avec la souris dans un élément container ;

`min-width`  et  `max-width`  pour définir des tailles minimum et maximum.

🤖 HAPPY CODING !