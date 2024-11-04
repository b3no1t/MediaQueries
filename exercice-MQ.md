
# Exercice : Création d'une mise en page responsive avec Media Queries

### Objectif
Créer une page web simple avec une en-tête, une barre latérale et un contenu principal qui s'adapte à différentes tailles d'écran.

### Instructions

1. Créez un fichier HTML avec la structure de base suivante :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercice Media Queries</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Mon Site Web</h1>
    </header>
    <div class="container">
        <aside>
            <h2>Barre latérale</h2>
            <ul>
                <li>Lien 1</li>
                <li>Lien 2</li>
                <li>Lien 3</li>
            </ul>
        </aside>
        <main>
            <h2>Contenu Principal</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam auctor, nunc id aliquam tincidunt, nisl nunc tincidunt nunc, vitae aliquam nunc nunc vitae nunc.</p>
        </main>
    </div>
</body>
</html>
```

2. Créez un fichier CSS nommé `styles.css` et ajoutez les styles de base suivants :

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    padding: 1rem;
    text-align: center;
}

.container {
    display: flex;
    flex-wrap: wrap;
}

aside {
    background-color: #f0f0f0;
    padding: 1rem;
}

main {
    padding: 1rem;
}
```

3. Ajoutez les media queries suivantes à votre fichier CSS pour rendre la mise en page responsive :

```css
/* Pour les écrans larges (par défaut) */
aside {
    width: 25%;
}

main {
    width: 75%;
}

/* Pour les écrans moyens */
@media screen and (max-width: 768px) {
    aside {
        width: 30%;
    }
    
    main {
        width: 70%;
    }
}

/* Pour les petits écrans */
@media screen and (max-width: 480px) {
    .container {
        flex-direction: column;
    }
    
    aside, main {
        width: 100%;
    }
}
```

### Défi supplémentaire

Ajoutez une media query pour les écrans très larges (plus de 1200px) qui limite la largeur maximale du contenu et le centre sur la page.

### Résultat attendu

- Sur les grands écrans, la barre latérale occupe 25% de la largeur et le contenu principal 75%.
- Sur les écrans moyens, la barre latérale occupe 30% et le contenu principal 70%.
- Sur les petits écrans, la barre latérale apparaît au-dessus du contenu principal, chacun occupant 100% de la largeur.

Testez votre page en redimensionnant la fenêtre du navigateur pour voir comment la mise en page s'adapte aux différentes tailles d'écran.

Cet exercice vous permettra de pratiquer l'utilisation des media queries pour créer un design responsive qui s'adapte à différentes tailles d'écran.