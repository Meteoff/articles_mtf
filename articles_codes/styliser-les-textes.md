Les balises pour "styliser" vos textes
=====
*HTML - Niveau 1 - Créer par meteoff - 30/01/21*
------

Bienvenue sur l'article pour "styliser" vos textes, ou les *formater*

**Avertissement :Il existe plein de balise pour styliser votre texte, dans cette article, il y a seulement les balises les plus utilisées**

Tout d'abord, les balises pour créer un paragraphe sont : `<p></p>`.
L'utilisation se fait dans le body, ou dans un autre élément.

```html
<body>
  <p>Bonjour, ceci est un paragraphe !</p>
<body>
```
*html*

La balise s'ouvre et se ferme, comme sur l'article [précédent](https://meteoff.cf/articles/les-bases-du-html-et-css). Mais bon, le texte ne ressemble à rien.

<p>Bonjour, ceci est un paragraphe !</p>

Nous pouvons donc ajouter certains balises pour styliser le texte :
|Balises|Explications|
|-------|------------|
|`<p>...</p>`|Créer un paragraphe|
|`<b>...</b>`|Mettre en gras moins important|
|`<strong>...</strong>`|Mettren en gras plus important|
|`<i>...</i>`|Mettre en italic moins important|
|`<em>...</em>`|Mettre en italic plus important|
|`<u>...</u>`|Souligner un texte|
|`<del>...</del>`|Barrer un texte|
|`<br>`|Changer de ligne|

Si on ajoute tout ça, voici ce que ça donne :

 [RESULTAT](https://codepen.io/skptricks/embed/eYBYwPq)
 
 ```html
 <body>
  <p>
    <u>Bonjour !</u><br>
    Bienvenue sur mon <em>tout</em> <b>nouveau</b> site.<br>
    Vous trouverez <strong>des astuces</strong>, au prix de <del>9,99€</del>0,00€ ! <i>Bonne journée</i>
  </p>
</body>
```
*html*

Le texte ressemble déjà plus à quelques chose !

Couleur, police, taille,...
------

Mais pour changer la couleur, la police, etc..., il y a plusieurs solutions :

* Avec la balise `<font>...</font>`
* Avec les balises `<span>...</span> / <div>...</div> / ...`
* Via CSS

Pour le moment, nous allons utiliser la 1er version, `<font>...</font>`
Cette balise, contient plusieurs arguments, c'est à dire des options entre la balise, par exemple pour changer la couleur :

```html
<body>
  <font color="green">Texte en vert</font>
</body>
```

Plusieurs balises utilisent des arguments.
La balise font, comporte plein d'arguments, en voici les principaux pour styliser le texte : (ajouter <font devant)

|Balises|Explications|Valeurs|
|-------|------------|-------|
|`color="valeur"`|Change la couleur du texte entre les balises|blue, green, #2f0145, #deee, etc|
|`size="valeur"`|Change la taille du texte entre les balises|Comprise entre 1 et 7|
|`face="valeur"`|Changer la police d'écriture|Arial, Sans-serif, Elephant, Cooper black, ...|

[RESULTAT](https://codepen.io/skptricks/embed/oNYNKze)

```html
<body>
  <font color="green">Texte en vert</font><br>
  <font size="5">Texte important</font><br>
  <font face="Times New Roman">Police Times New Roman</font><br>
  <font face="Elephant" color="blue" size="4">Tout ensemble</font>
</body>
```
Pour les autres options, il faudrat attendre un peu !

Merci d'avoir lu cette article, effectuez le quiz maintenant !
Bonne journée !
