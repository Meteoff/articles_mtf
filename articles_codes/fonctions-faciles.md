Fonctionnalités faciles et intéressantes
======
*HTML - Niveau 1 - Créer par meteoff - 12/02/2021*
------

Bonsoir,

Dans cet article vous allez découvrir comment intégrer à votre site web des fonctionnalités faciles et intéressantes, comme ajouter une vidéo youtube, un icône,...

Ajouter des vidéos youtube
------

Pour ajouter des vidéos youtube, les balises `<video>...</video>` ne fonctionnent pas !

Par exemple, pour ajouter cette vidéo, voilà les étapes :

* Cliquez droit sur la vidéo pour obtenir un menu
* Selectionnez "*copier le code d'intégration*"
* Collez le code dans votre fichier .html

[RESULTAT](https://codepen.io/skptricks/embed/poNRgYR)

```html
<body>
  <iframe width="1280" height="720" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</body>
```
*html*

Et vous voila avec votre vidéo youtube !

Ajouter les erreurs 404,403, etc
-----

Vous êtes sûrement déjà aller sur un site, et sûrement déjà tomber sur une erreur 404 (codes HTTP [AIDE](https://fr.wikipedia.org/wiki/Liste_des_codes_HTTP))

**Avertissement :Cet article est seulement un résumé des codes HTTP, il sert juste à faire le principal !**

Pour commencer, vous devez déjà avoir un fichier `404.html`, `403.html` et `500.html`.

|Type|Explication|
|----|-----------|
|404|Impossible de trouver le fichier|
|403|Accès refusé|
|500|	Erreur de serveur|

**Astuce :Le fonctionnement qui va suivre à été réalisé dans le cas où un serveur web est disponible ! Pour le faire en local, vous devez remplacer les `https://meteoff.cf/404` par `/lien/vers/le/404.html`**

Une fois les fichiers mis sur votre serveur, ouvrez le fichier `.htaccess`, si vous en n'avez pas, créer en un.

Si votre fichier est nouveau, une page blanche s'ouvre.

Pour signifier que pour les erreurs 404, on veut afficher votre fichier `404.html`, on doit le signifier dans ce fichier (.htaccess)

```text
ErrorDocument 404 https://meteoff.cf/404.html
```
*texte*

|Code|Explication|
|----|-----------|
|ErrorDocument|	Signifie le lien d'un fichier lorsqu'une erreur est rencontrée|
|404|	Le type d'erreur (code HTTP)|
|https://meteoff.cf/404.html|Le lien vers le document|

Maintenant, lorsque le serveur ne trouvera pas le fichier, il renverra vers `https://meteoff.cf/404.html`.

Pour les autres types d'erreur, voilà le résultat :

```text
ErrorDocument 404 https://meteoff.cf/404.html
ErrorDocument 403 https://meteoff.cf/403.html
ErrorDocument 500 https://meteoff.cf/500.html
```
*texte*

Ajouter un icône à votre site web
-------

Comme vous l'avez remarque, mais la plupart des sites web contiennent des icônes.

Or, vos fichiers n'ont aucun icônes...

Pour ajouter un icône, il faut quelques conditions.

* Votre logo doit être carré (16X16, 32X32, ...)
* Doit être au format .ico
* Doit être compréhensible

Pour convertir votre image en .ico, vous pouvez utiliser ce [site](https://www.freeconvert.com/png-to-ico).

Une fois votre fichier en .ico, renommez votre fichier en `favicon`, et placez le dans le dossier racine de votre site.

Normalement, le logo est automatiquement affichée dans le navigateur, mais si il ne s'affiche pas, vous avez une autre solution, le `<link>` !
Ce qui donnerait :

```html
<head>
  <link rel="shortcut icon" href="votre_icone.ico">
</head>
```
*html*

Et pouf ! Votre site web contient votre icône !
<hr>

Merci d'avoir suivi ce cours et à bientôt !
