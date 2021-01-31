Liens, images, vidéos, musiques, ...
=======
*HTML - Niveau 1 - Créer par meteoff - 31/01/21*
------

A la fin, voilà le resultat :

[RESULTAT](https://codepen.io/skptricks/embed/GRNgmVo)

```html
<body>
  <img src="https://i.imgur.com/8S86aEv.png" width="25%">
  <video controls>
    <source src="https://www.dropbox.com/s/fh4ylk14vdtc074/article-4.mp4?raw=1" type="video/mp4">
    Désolé, mais votre navigateur ne prends pas en charge les vidéos :\
  </video><br>
  La suite sur <a href="https://www.meteoff.cf/articles/liens-images-videos/" target="_blank">meteoff</a><br>
  <audio controls>
    <source src="https://www.dropbox.com/s/vdh97v8nrixiv6f/Hymn%20to%20the%20Sea.mp3?raw=1" type="audio/mpeg">
    Votre navigateur ne prends pas en charge les audios :\
  </audio>
</body>
```
*html*

Images
------


Pour ajouter des images, vous avez besoin de la balises `<img>`.

**Attention :Cette balise est une balise qui ne se ferme pas, c'est a dire qu'il n'y a pas besoin de "&lt;/img&gt;" mais seulement de la balise "&lt;img&gt;"**

Donc il faut commencer par trouver une image, et l'upload sur votre serveur ou ordinateur. Une fois l'image trouver, il faut signifier le chemin, avec l'attribut `src="chemin"`.

![Image d'explication](https://www.meteoff.cf/img/articles/art4/img_1.png)
*Image d'explication pour les fichiers*

maginons, votre fichier est situé dans le dossier principal, et que vous voulez l'image image_2.jpg, située un dossier plus haut.
Pour signifier qu'il faut aller dans un dossier, il suffit de mettre un `/` dans le lien. Par exemple, si il y aurait un dossier "jeu", on aurait écris : `jeu/fichier.extension`.

![Image](https://www.meteoff.cf/img/articles/art4/img_2.png)
*Image d'explication pour les dossiers*

```html
<img src="jeu/img/im.png">
```
*html*

Il existe plusieurs attributs pour la balise img, en voici quelques-un : (<img ...)
|Arguments|Explications|
|---------|------------|
|`src="valeur"`|Définir le chemin à emprunter pour trouver l'image.|
|`width="valeur"`|Définir la taille de l'image. En %,px,em,...|
|`height="valeur"`|Définir la hauteur de l'image. En %,px,em,...|
|`title="valeur"`|Afficher un titre à l'image lorsque l'utilisateur laisse sa souris sur l'image.|
|`alt="valeur"`|Afficher un texte si l'image ne peut pas s'afficher.|
|`class="valeur"`|Styliser l'image avec le css|
|`id="valeur"`|Styliser l'image avec le css ou pour l'utiliser avec javascript|
|`draggable="valeur"`|Définit si l'image peut être attrapée par l'utilisateur. TRUE-FALSE|

![Image](https://www.meteoff.cf/img/articles/art4/img_3.png)
*Exception pour les dossiers*

Mais imaginons que pour x ou y raison, votre fichier .html doit être dans un dossier, et non dans le dossier racine, et que vous voulez afficher l'image située dans `Images/Images/img1.png`.
Si vous essayez de mettre ceci, l'image ne s'affichera pas,

Pour revenir à un dossier situé en dessous, vous devez mettre `../` devant le nom, ce qui indique qu'il faut remonter d'un dossier.
Et donc si il y a plusieurs dossiers à remonter pour aller sur le fichier, il faudrait donc indiquer :

```html
<img src="../../../Images/Images/img1.png">
```
*html/

Liens
--------

Pour créer des liens hypertextes [aide](https://fr.wikipedia.org/wiki/Hyperlien), vous aurez besoin de la balise `<a>...</a>`

Le lien doit être écrit avec l'attribut `href="lien"`.
Le lien peut fonctionner comme avec l'image, c'est à dire que au lieu de pointer une image, il pointe vers un fichier **".html"** (ou autre).

![Image](https://www.meteoff.cf/img/articles/art4/img_4.png)
*Comment trouver votre fichier .html*

Exemple de code pour cet usage :

```html
<a href="fichier/html/index.html">Lien vers le menu</a>
```
*html*

Tout ce qui est écris entre les balises **a**, sera sous forme de lien.
Ensuite, pour aller sur un site web, vous avez juste à mettre le lien, par exemple pour aller sur `"www.google.fr"` :

```html
<a href="https://www.google.fr">google</a>
```
*html*

Il doit toujours y avoir le protocole, `http://` ou `https://` pour visiter des sites web externes.

La balise **a** comporte aussi beaucoup d'attributs, en voici la plupart : (<a ...)

|Arguments|Explications|
|---------|------------|
|`href="lien"`|Indique le chemin ou l'URL du fichier.|
|`title="valeur"`|Affiche un titre lorsque la souris reste sur le lien.|
|`target="valeur"`|Indique la cible du lien. Le plus souvent `_blank`, pour ouvrir dans un nouvel onglet.|
|`class="valeur"`|Styliser le lien avec du CSS.|
|`id="valeur"`|	Styliser le lien avec du CSS ou pour l'utiliser avec du Javascript.|
|`draggable="valeur"`|	Indique si le lien peut être attrapé par l'utilisateur. TRUE FALSE|

Vidéos
--------

Pour afficher des vidéos, il faut utiliser les balises `<video>...</video>`

Mais les balises vidéos et audios sont plus complexes que les liens et images 😒.

Pour ces balises, il faut signifier la source, le type, les contrôles, etc...
Par exemple pour une vidéo en MP4 :

```html
<video controls fullscreen>
  <source src="https://www.dropbox.com/s/fh4ylk14vdtc074/article-4.mp4?raw=1" type="video/mp4">
  Désolé, votre navigateur ne prends pas en charge les vidéos :\
</video>
```

**Avertissement :Cette vidéo provient d'un lien externe, mais peut provenir d'un fichier local.**

**Attention :Les vidéos youtube ne sont pas compatibles avec l'élèment <video> mais fonctionne avec un iframe.**

En gros, pour ajouter une vidéo il faut :

* Ajouter les balises `<video></video>`
* Ajouter la balise `<source>`
* Signifier la source (comme les images) `<source src="votre source">`
* Signifier le type de vidéo `type=video/mp4`
* Afficher un message pour les navigateurs qui ne prennent pas en charge les vidéos
* Et enfin, fermer les balises

Pour la balise video, voici la plupart des arguments : (<video ...)

|Arguments|Explications|
|---------|------------|
|`controls`|Indique si la vidéo doit contenir des contrôles (pause, pleine écran, son,...)|
|`fullscreen`|Indique si la vidéo peut être lu en plein écran ou non.|
|`autoplay`|Indique si la vidéo est lu automatiquement au chargement de la page.|
|`loop`|Activer la lecture à infini|
|`muted`|Mettre le volume de la vidéo à 0.|
|`width="valeur"`|Définit la taille de la vidéo.|
|`height="valeur"`|Définit la hauteur de la vidéo.|
|`class="valeur"`|Styliser la vidéo en CSS.|
|`id="valeur"`|	Styliser la vidéo en CSS ou l'utiliser en javascript.|

La vidéo peut contenir plusieurs source, avec plusieurs type : (<source type=...)

|Types|Explications|
|-----|------------|
|`video/mp4`|Pour les vidéos en MP4.|
|`video/ogg`|Pour les vidéos en ogg.|
|`video/webm`|Pour les vidéos en webm.|

```html
<video controls autoplay>
  <source src="video/ma_video.mp4" type="video/mp4">
  <source src="video/ma_video.ogg" type="video/ogg">
  Désolé, votre navigateur ne prends pas en charge les vidéos :\
</video>
```
*html*

Musiques
------

Pour signifier qu'il faut ajouter une musique (ou un audio), il faut ajouter les balises `<audio>...</audio>`

Les balises audios fonctionnent comme les balises videos, c'est à dire qu'il faut signifier la source.

```html
<audio controls>
  <source src="https://www.dropbox.com/s/vdh97v8nrixiv6f/Hymn%20to%20the%20Sea.mp3?raw=1" type="audio/mpeg">
  Désolé, votre navigateur ne prends pas en charge les audios :\
</audio>
```
*html*

La balise audio comporte exactement les mêmes arguments que la balise vidéo, il faut juste changer le type pour les sources, et voici la plupart des types : (<source type="...)

|Types|Explications|
|-----|------------|
|`audio/mpeg`|Fichier au format mp3|
|`audio/ogg`|Fichier au format ogg|
|`audio/wav`|	Fichier au format wav|

Merci d'avoir lu cet article ! Répondez au quiz pour gagner du niveau et bonne journée !
-Meteoff
