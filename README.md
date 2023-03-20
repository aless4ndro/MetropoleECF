# MegalopoleECF

Le site web est un guide de voyage en ligne pour les touristes qui souhaitent visiter trois capitales différentes.

## Run Locally

Clone the project

```bash
  git clone https://github.com/aless4ndro/MetropoleECF
```

Go to the project directory

```bash
  cd MetropoleECF
```

## UX/UI

### Color Reference

| Color             | Hex                                                                |
| ----------------- | ------------------------------------------------------------------ |
|  Color | ![#0a192f](https://via.placeholder.com/10/0a192f?text=+) #0a192f |
|  Color | ![#f8f8f8](https://via.placeholder.com/10/f8f8f8?text=+) #f8f8f8 |
|  Color | ![#00545d](https://via.placeholder.com/10/00b48a?text=+) #00545d |
|  Color | ![#666](https://via.placeholder.com/10/00b48a?text=+)       #666 |
|  Color | ![#99b1b1](https://via.placeholder.com/10/00b48a?text=+) #99b1b1 |
|  Color | ![#da4747](https://github.com/aless4ndro/MetropoleECF) #da4747 |

### Police

- 'Playfair Display' pour le footer

- 'Arial' pour les Titre du all.css

- 'Dancing'

### Screenshots

![App Screenshot](/imgEcf/Capture%20d%E2%80%99%C3%A9cran%20Hello.png)
![App Screenshot](/imgEcf/Capture%20d%E2%80%99%C3%A9cran%20megalopole3.png)
![App Screenshot](/imgEcf/Capture%20d'%C3%A9cran%20london.png)

## Code/Examples

Le dossier css contien style.css->index.html

Le dossier scss contien style.scss->infoGlobal.html

### Ce code correspond a style.scss->infoGlobal.html

- Voici une explication de ce qu'il fait
  Cette règle définit que l'élément qui précède et celui qui suit chaque élément de la page auront une boîte de contenu qui inclut les bordures, les rembourrages et les marges. Les propriétés padding et margin sont définies à 0.

```CSS
::before,
::after * {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
```

- Cette règle définit le style pour le corps (body) de la page. Elle ajoute un dégradé linéaire en arrière-plan avec des couleurs allant du gris foncé (#2c3e50) au gris clair (#b9c4cf). Elle ajoute également une ombre intérieure sur toute la page, avec une couleur de blanc transparent (rgba(255, 255, 255, 0.415)). La police de caractères utilisée est Montserrat.

```CSS
body {
  background: linear-gradient(to bottom, #2c3e50, #b9c4cf);
  box-shadow: inset 0px 0px 200px rgba(255, 255, 255, 0.415), 0px 0px 50px rgba(220, 220, 220, 0.872);
  display: block;
  align-items: center;
  justify-content: center;
  font-family: "Montserrat", sans-serif;
}
```

- La première règle de style déclare les propriétés pour la classe "point". La règle définit un curseur pointer lorsque l'utilisateur passe la souris sur l'élément, définit la position absolue de l'élément, définit une largeur et une hauteur de 1,6 rem, et définit la couleur d'arrière-plan de l'élément à #00acc1. Elle définit également un rayon de bordure de 50% pour créer un cercle, une transition en douceur de toutes les propriétés CSS pendant 0,3 seconde, une modification de transform et de box-shadow lorsqu'une animation est déclenchée, et un décalage de transformation de 50% à partir du centre de l'élément. Elle ajoute également une ombre à l'élément avec une opacité de 0,4, mais sans étendre la longueur et la largeur de l'ombre. Enfin, elle définit une animation de pulse pendant 3 secondes, qui est infinie.

- La deuxième règle de style définit les propriétés pour la classe "map-container". La règle définit un rembourrage de 3,2 rem en haut et en bas et de 0,8 rem à gauche et à droite, une position relative pour l'élément, un affichage en ligne pour l'élément, un alignement central et une largeur de 80% pour l'élément.

```CSS
.map-container .point {
  cursor: pointer;
  position: absolute;
  width: 1.6rem;
  height: 1.6rem;
  background-color: #00acc1;
  border-radius: 50%;
  transition: all 0.3s ease;
  will-change: transform, box-shadow;
  transform: translate(-50%, -50%);
  box-shadow: 0 0 0 rgba(0, 172, 193, 0.4);
  animation: pulse 3s infinite;
}
.map-container {
  padding: 3.2rem 0.8rem;
  position: relative;
  display: inline-block;
  justify-content: center;
  width: 80%;
}
```

- Ce code CSS définit les styles pour une carte interactive dans un site web. Les styles sont appliqués à des éléments HTML qui ont une classe "map-container" et une classe "point".

Les éléments avec la classe "point" ont les propriétés suivantes:

"cursor: pointer;" permet de changer l'apparence du curseur de la souris lorsque l'utilisateur passe dessus.
"position: absolute;" place l'élément en position absolue par rapport à son parent (qui doit avoir une position relative).
"width: 1.6rem;" et "height: 1.6rem;" définissent la taille de l'élément.
"background-color: #00acc1;" définit la couleur de fond de l'élément.
"border-radius: 50%;" arrondit les coins de l'élément pour créer un cercle.
"transition: all .3s ease;" ajoute une transition d'une durée de 0,3 seconde pour les propriétés qui changent.
"will-change: transform, box-shadow;" optimise les performances en indiquant au navigateur quelles propriétés seront modifiées.
"transform: translate(-50%, -50%);" place l'élément au centre de son parent.
"box-shadow: 0 0 0 rgba(0, 172, 193, 0.4);" ajoute une ombre autour de l'élément.
"animation: pulse 3s infinite;" lance une animation nommée "pulse" d'une durée de 3 secondes qui se répète indéfiniment.
Ensuite, pour chaque pays représenté sur la carte, une classe spécifique est définie (par exemple ".venezuela" pour le Venezuela). Chacune de ces classes définit les propriétés "top" et "left" pour placer l'élément correspondant à la bonne position sur la carte.

Enfin, il y a deux media queries qui ajustent la taille des éléments avec la classe "point" pour les écrans de petite taille (moins de 768 pixels de largeur).

```CSS
.point {
  cursor: pointer;
  position: absolute;
  width: 1.6rem;
  height: 1.6rem;
  background-color: $primary;
  border-radius: 50%;
  transition: all .3s ease;
  will-change: transform, box-shadow;
  transform: translate(-50%, -50%);
  box-shadow: 0 0 0 rgba($primary, 0.4);
  animation: pulse 3s infinite;

  &:hover {
    animation: none;
    transform: translate(-50%, -50%)scale3D(1.35, 1.35, 1);
    box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
  }
}

.venezuela {
  top: 54%;
  left: 24%;
}

/*...*/

@media(max-width: 768px) {
  .map-container.point {
    width: 10px;
    height: 10px;
  }
}

@media(max-width: 576px) {
  .map-container.point {
    width: 5px;
    height: 5px;
  }
}
```

## MediaQuerys

Code all.css

- Ces mediaquerys redimensionne la taille du body a partir de 500px, modifient l'aspct du back-to-top-btn

```CSS
@media (min-height: 500px) {
  body {
    position: relative;
  }

  #back-to-top-btn {
    display: block;
  }

  #back-to-top-btn:hover {
    text-decoration: none;
  }

  #back-to-top-btn:active {
    top: 1px;
  }

  #back-to-top-btn:focus {
    outline: none;
  }
}
```

Mediaquery footer styles.css

- le but de ce script est de redimensionner le footer pour les ecrans de max 768px

```CSS
@media only screen and (max-width: 768px) {
  .footer-left-col {
    flex-basis: 100%;
  }

  .footer-right-col {
    flex-basis: 100%;
  }

  .footer-info {
    justify-content: center;
  }

  .footer-logo {
    flex-basis: 100%;
    text-align: center;
  }

  .footer-logo button {
    margin-top: 10px;
  }

  .footer-left-col,
  .footer-right-col {
    flex-basis: 100%;
  }
}
```

### Ce code correspond au dossier css->all.css

- Ce code CSS permet de réaliser plusieurs effets :

Le premier bloc de code concerne une animation d'une photo. Lorsque la souris passe sur cette photo, elle se met à pivoter légèrement et à grossir. Lorsqu'on clique dessus, elle pivote dans l'autre sens et rétrécit légèrement.
Le deuxième bloc de code concerne un bouton "Back to top" qui s'affiche en bas à droite de la page lorsque la hauteur de la fenêtre dépasse 500 pixels. Ce bouton est initialement caché (display: none), mais lorsqu'il s'affiche, il peut être survolé et cliqué. Lorsqu'il est cliqué, il remonte la page vers le haut.
Le troisième bloc de code concerne la personnalisation des barres de défilement verticales et horizontales du navigateur, en ajoutant une couleur de fond, des dégradés de couleurs pour les "thumb" et des bordures arrondies.
En résumé, ce code CSS permet de personnaliser les effets visuels d'une photo, d'un bouton et des barres de défilement.

```CSS
#animatePhoto {
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  transition: transform 0.3s ease-in-out;
}

#animatePhoto:hover {
  cursor: pointer;
  transform: rotate(10deg) scale(1.1);
}

#animatePhoto:active {
  transform: rotate(-10deg) scale(0.9);
}

#back-to-top-btn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  display: none;
}

#back-to-top-btn img {
  width: 90px;
}

@media (min-height: 500px) {
  body {
    position: relative;
  }

  #back-to-top-btn {
    display: block;
  }

  #back-to-top-btn:hover {
    text-decoration: none;
  }

  #back-to-top-btn:active {
    top: 1px;
  }

  #back-to-top-btn:focus {
    outline: none;
  }
}

/* Barre de défilement verticale */
::-webkit-scrollbar {
  width: 12px;
}

::-webkit-scrollbar-track {
  background-color: #ffffff;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(to bottom, #da4747, #f9f9f9, #da4747);
  border-radius: 10px;
}

/* Barre de défilement horizontale */
::-webkit-scrollbar-horizontal {
  height: 12px;
}

::-webkit-scrollbar-thumb:horizontal {
  background: linear-gradient(#2341e9, #ffffff, #ffffff);
  border-radius: 10px;
}
```

### Ce code correspond au dossier css->style.css

- Il decrit la class ocean, cette class sers a englober la section 2, 3, 4
Elle permet de mettre du style dans le fichier css.

```HTML
    <div class="ocean">
        <div class="navbar">
            <a href="login.html"><img src="imgEcf/bubble.png" alt="logo" id="logo"></a>
        </div>
        <div class="content">
            <div class="background-text">HELLO.</div>
            <a href="infoGlobal.html"><button type="button">Faire un Tour</button></a>
        </div>
        <div class="sideBar">
            <img src="imgEcf/menu.png" alt="menu" class="menu">
            <div class="menuItems">
                <img src="imgEcf/fb.png">
                <img src="imgEcf/ig.png">
                <img src="imgEcf/tw.png">
            </div>
            <div class="usefulLinks">
                <img src="imgEcf/share.png">
                <img src="imgEcf/info.png">
            </div>
        </div>
        <div class="bubbles">
            <img src="imgEcf/bubble.png" alt="boules">
            <img src="imgEcf/bubble.png" alt="boules">
            <img src="imgEcf/bubble.png" alt="boules">
            <img src="imgEcf/bubble.png" alt="boules">
            <img src="imgEcf/bubble.png" alt="boules">
            <img src="imgEcf/bubble.png" alt="boules">
            <img src="imgEcf/bubble.png" alt="boules">
            <img src="imgEcf/bubble.png" alt="boules">
        </div>
    </div>
```

### Ce code correspond au dossier css->all.css

- Il décrit le back-to-top-btn ce code a un id "top" cette id est appelé au bas de page pour faire apparaitre l'animation et il repart vers le haut une fois qu'on appuie dessous afin de  fiare remoter la page vers le haut.

```HTML
<a id="top"></a>
...
<a href="#top" id="back-to-top-btn"><img src="imgEcf/avion.png" alt="logoAvion"></a>
```

## Scrollbar

J'ai utiliser les pseudo-éléments ::-webkit-scrollbar, ::-webkit-scrollbar-track, ::-webkit-scrollbar-thumb pour personnaliser la barre de défilement sur les navigateurs Webkit (tels que Google Chrome et Safari). J'ai également ajouté des pseudo-éléments pour personnaliser la barre de défilement horizontale.

## SVG

Signifie Scalable Vector Graphics. Il s'agit d'un format de fichier d'image vectorielle qui utilisedes formules mathématiques pour dessiner des images plutôt que des pixels. Les images vectoriellespeuvent être agrandies ou réduites sans perte de qualité, ce qui les rend idéales pour lesgraphiques, les icônes, les logos et les illustrations sur le web. Les fichiers SVG peuvent êtrecréés à l'aide d'un éditeur d'images vectorielles, tels que Adobe Illustrator ou Inkscape, ou enécrivant directement le code SVG à la main dans un éditeur de texte.
Les nombres dans un SVG représentent les coordonnées, les dimensions et d'autres propriétés des éléments graphiques. Les coordonnées x et y représentent la position horizontale et verticale d'un élément par rapport à l'origine du système de coordonnées. Les propriétés de largeur et de hauteur définissent les dimensions de l'élément. Les nombres peuvent également être utilisés pour définir des attributs tels que la couleur, l'épaisseur de la ligne et la transparence.

## La conception neumorphique

 (ou neumorphisme) est une tendance récente en matière de conception d'interfaces utilisateur qui utilise des éléments de conception similaires à ceux de la conception skeuomorphique et de la conception plate.

La conception neumorphique utilise des éléments d'interface utilisateur qui semblent être en relief ou en creux, comme si l'interface était faite de matière molle et flexible. Les éléments ont des ombres douces et diffuses, des bordures floues et des couleurs pastel. Cette approche donne une apparence et une sensation plus douces et plus organiques à l'interface utilisateur.

- Les avantages de la conception neumorphique

La conception neumorphique offre une expérience utilisateur plus immersive et plus réaliste, en donnant l'impression que les éléments de l'interface sont réels et peuvent être touchés ou manipulés.
Elle est plus facile à utiliser pour les utilisateurs qui ont des difficultés à distinguer les éléments de l'interface, car elle utilise des éléments plus grands et plus contrastés.
Elle est plus accessible pour les utilisateurs souffrant de fatigue visuelle, car elle utilise des couleurs pastel plus douces et des bordures floues pour réduire la fatigue oculaire.
Cependant, la conception neumorphique peut également présenter des inconvénients, tels que :

Elle peut être plus difficile à réaliser pour les développeurs web, car elle nécessite des techniques de codage plus avancées pour créer les effets de relief et de creux.
Elle peut rendre l'interface utilisateur plus lente à charger, car elle utilise des images plus grandes et plus complexes pour créer les effets de relief et de creux.
Elle peut sembler trop douce ou trop organique pour certains utilisateurs qui préfèrent une apparence plus nette et plus structurée.
