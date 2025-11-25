## Rappels

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



