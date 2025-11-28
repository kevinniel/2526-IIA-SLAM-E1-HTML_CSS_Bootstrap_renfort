## Rappels

- C'est le W3C (World Wide Web Consortium) qui gère les évolutions du HTML/CSS.
- Un CTA, est un "Call To Action" : c'est à dire un lien ou un bouton qui déclenche une action.


### Modèle de boite

<img src="./images/mdb.png">

Cela concerne tous les blocs (= élément HTML). Chacun dispose de 4 parties qui le composent : 

1. `content` : le contenu du bloc
2. `padding` : la marge intérieure du bloc
3. `border` : la bordure du bloc
4. `margin` : la marge extérieure du bloc

Lorsque l'on découpe "visuellement" une maquette, on suit l'ordre suivant : 
1. Définir l'emplacement de la bordure, s'il y en avait une (elle n'est pas forcément visible)
2. Déterminer l'emplacement du contenu
3. Vérifier les margins
4. Vérifier les paddings

*Note* : Les margins et les paddings sont presque tout le temps égaux à l'opposé, pour respecter une symétrie.

### RWD (Responsive Web Design)

Le principe est que le contenu s'adapte parfaitement à toutes les tailles d'écran. 

Pour le faire, on utilise des BreakPoints, appelées "Media Queries" en CSS. Le principe, est de définir une largeur en pixels,
et d'adapter le contenu de la page, en fonction de sa largeur. En gros, vous appliquer certaines règles CSS en fonction de la
largeur de votre écran.

### Display

Le display est une propriété CSS qui permet de gérer la manière dont les éléments doivent être affichés.

Il en existe 6 principaux : 
- `None` : N'affiche pas l'élément
- `Block` : Prend 100% de la largeur disponible. S'adapte en hauteur, en prenant le minimum nécessaire pour afficher le contenu. On peut redéfinir sa taille en dur.
- `Inline` : Prend uniquement l'espace nécessaire en hauter et en largeur pour afficher son contenu. On ne peut pas redéfinir sa taille.
- `Inline-Block` : C'est le même comportement que "Inline", à ceci près qu'on peut modifier sa tailler et son padding.
- `Flex` : cf : <a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox/" target="_blank">CSS Tricks</a>
- `Grid` : respecte le principe d'une grille.

Source pour s'entraîner au display flex : <a href="https://flexboxfroggy.com/#fr" target="_blank">Flexbox Froggy</a>

## Bootstrap

Bootstrap est un framework (cadre de travail) qui vous fourni un code CSS déjà prêt à l'emploi.

<a href="https://getbootstrap.com/docs/5.3/getting-started/introduction/" title="Lien de la doc de bootstrap" target="_blank">Lien de la doc de bootstrap</a>

### La Grid Bootstrap

#### Les bases

Bootstrap est prévu pour fonctionné sur un modèle de 12 colonnes découpables. Ces colonnes s'utilisent grâce aux classes suivantes : 
- `col-1` : Prend l'espace de 1 colonne dans le bloc parent.
- `col-2` : Prend l'espace de 2 colonnes dans le bloc parent.
- `col-3` : Prend l'espace de 3 colonnes dans le bloc parent.
- `col-4` : Prend l'espace de 4 colonnes dans le bloc parent.
- `col-5` : Prend l'espace de 5 colonnes dans le bloc parent.
- `col-6` : Prend l'espace de 6 colonnes dans le bloc parent.
- `col-7` : Prend l'espace de 7 colonnes dans le bloc parent.
- `col-8` : Prend l'espace de 8 colonnes dans le bloc parent.
- `col-9` : Prend l'espace de 9 colonnes dans le bloc parent.
- `col-10` : Prend l'espace de 10 colonnes dans le bloc parent.
- `col-11` : Prend l'espace de 11 colonnes dans le bloc parent.
- `col-12` : Prend l'espace de 12 colonnes dans le bloc parent.


Chaque colonne doit **Obligatoirement** être disposée dans un autre élément qui dispose de la classe `.row`

```HTML
<!-- 1 ligne -->
<div class="row">
    <!-- qui prend tout l'espace -->
    <div class="col-12">
    </div>
</div>
<!-- 1 ligne -->
<div class="row">
    <!-- qui prend 50% de l'espace -->
    <div class="col-6">
    </div>
    <!-- qui prend 50% de l'espace -->
    <div class="col-6">
    </div>
</div>
```

Dernière spécificité, tous les `row` doivent être dans un élément contenant la class `container` ou `container-fluid`.

le `container` laisse des marges droite / gauche de visibles tandis que le `container-fluid` prend 100% de la largeur.

#### Le Responsive (RWD)

Bootstrap inclu ses propres breakpoints (<a href="https://getbootstrap.com/docs/5.3/layout/breakpoints/#available-breakpoints" target="_blank">breakpoints bootstrap</a>) que voici : 

| Breakpoint            | Class infix | Dimensions |
|-----------------------|-------------|------------|
| Extra small           | None        | <576px     |
| Small                 | sm          | ≥576px     |
| Medium                | md          | ≥768px     |
| Large                 | lg          | ≥992px     |
| Extra large           | xl          | ≥1200px    |
| Extra extra large     | xxl         | ≥1400px    |

Ce qui signifie que pour les colonnes, vous pouvez préciser :

- `col-6` : Prend 6 colonnes sur 12 dans le bloc parent.
- `col-sm-6` : Prend 6 colonnes sur 12 à partir du breakpoint small.
- `col-md-6` : Prend 6 colonnes sur 12 à partir du breakpoint medium.
- `col-lg-6` : Prend 6 colonnes sur 12 à partir du breakpoint large.
- `col-xl-6` : Prend 6 colonnes sur 12 à partir du breakpoint extra large.
- `col-xxl-6` : Prend 6 colonnes sur 12 à partir du breakpoint extra extra large.