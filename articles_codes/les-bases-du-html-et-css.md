Les bases du HTML et CSS
===
*HTML - Niveau 1 - Créer par meteoff - 29/01/21*
----

Bonjour et bienvenue dans le 1er **vrai** article de développement.

Pour commencer, il faut débuter avec le HTML (HyperText Markup Language) [AIDE](https://developer.mozilla.org/fr/docs/Web/HTML)

Le HTML fonctionne grâce à des Balises, qui s'ouvre `<html>`, et qui se ferme `</html>`. Il existe beaucoup de balises, que ce soit pour le texte, pour les images, pour les liens, etc...

Commencer votre première page
------

Une page HTML se créer sur n'importe quel éditeur de texte, le fichier doit juste fini par `.html`, par exemple : `index.html`. Je vous conseille d'utiliser [Sublime Text](https://www.sublimetext.com/), qui est un logiciel gratuit, mais qui demande une clé de licence.

Les pages HTML doivent toujours comporter ces balises :

**Avertissement : Certaines pages peuvent faire exception, et les pages sont structurées comme ça depuis HTML 5**

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
  </body>
</html>
```
<a href="salut">salut</a>
*html*

Vous avez remaqué que toutes les balises se ferment, sauf une : `<!DOCTYPE html>`

En effet, cette balise sert à annoncer au navigateur la version de HTML utilisée et le type de document. Voici un tableau pour vous aider sur les balises utilisées :

| Balises | Explications |
|---------|--------------|
|`<!DOCTYPE html`|Tout les documents HTML doivent commencer par cette balise, elle décrit la version utilisée et le type de document. Cette balise ne se ferme pas.|
|`<html>...</html>`|Cette balise est la racine du fichier. Cette balise doit se fermer à la fin du fichier.|
|`<head>..</head>`|	Elle sert à indiquer l'en-tête du fichier, ce qui ne sera pas affiché sur la page par l'utilisateur.|
