---
layout: default
title: Cours HTML, CSS
parent: Apprendre
nav_order: 3
---

# Cours HTML, CSS (pas à jours)

## Base d'un code HTML
```html
<!DOCTYPE html>  
<html>  
<head>
  <meta charset="UTF-8">
  <title>Titre de ma page</title>
</head>
<body>  
  
<h1>Mon premier titre</h1>  
<p>Mon premier paragraphe.</p>  
  
</body>  
</html>
```

`<!DOCTYPE html>` : informe le navigateur que le document est un HTML5<br>
`<html>` : englobant tous les autres éléments HTML<br>
`<head>` : métadonnées sur le document<br>
`<body>` : contenu visible de la page Web<br>
`<meta>` : métadonnées comme l'encodage de caractère (`charset="UTF-8"`) assurer un affichage de texte approprié.<br>
### Commentaire
`<!-- je suis un commentaire -->`

## Tags textuels
`<h1>` jusqu'à `<h6>` : Titres<br>
`<title>` : titre de la page<br>
`<p>` : paragraphe<br>
***Bloc*** <br>
	`<div>` : balise entière (largeur)<br>
	`<span>` : uniquement la balise incluse<br>
`class` : sélectionner uniquement les balises avec un tag<br>
	exemple : `‹p class="my-group"›This is another paragraph. ‹/p›`<br>

## Tag 
`<center>` : centrer un texte
`<br>` : saut de lignes<br>
`<hr>` : ligne pour séparer<br>
`<pre>` : afficher comme écrit dans le code (afficher du code)<br>
`&nbsp;` : ajout d'un espace blanc<br>
`<ul>` : liste a puce<br>
`<ol>` : liste numéroté<br>
	`<li>` : pour les éléments de la liste<br>

## Formatage
`<b>` : <b>Texte en gras</b><br>
`<strong>` : <strong>Texte important</strong> (généralement affiché en gras)<br>
`<i>` : <i>Texte en italique</i><br>
`<em>` : <em>Texte mis en valeur</em> (accentuation, généralement en italique)<br>
`<mark>` : <mark>Texte marqué ou surligné</mark><br>
`<small>` : <small>Texte plus petit</small><br>
`<del>` : <del>Texte supprimé</del> (barré)<br>
`<ins>` : <ins>Texte inséré (souligné)</ins><br>
`<sub>` : Texte en <sub>indice</sub><br>
`<sup>` : Texte en <sup>exposant</sup><br>

## Attribues
`style` : ajouter des styles à un élément (CSS)<br>
	exemple : `<p style="color:red;">This is a red paragraph.</p>`<br>
`title` : extra Information sur un élément (texte avec la souris dessus)<br>
	exemple : `<p title="I'm a tooltip">This is a paragraph.</p>`<br>

`lang` : définir la langue de la page<br>
	exemple : `<html lang="en">`<br>

`<id>` : retrouver plus facilement une balise<br>
	exemple : `<h1 id="myHeader"› My Header</h1>`<br>
		exemple : `‹a href="#C12"›Jump to Chapter</a>` (sommaire)<br>

## Balise d'action
`<a>` : Insérer un lien <br>
	`href` : URL de la page <br>
		exemple : `<a href="https://url.com">This is a link</a>` <br>
`<img>` : Insérer une image <br>
	`src` : chemin d'accès à l'image <br>
	`alt` : texte alternatif pour une image <br>
	`width`, `height` : largeur et hauteur de l'image <br>
		exemple : `<img src="image.jpg" alt="image.com" width="104" height="142">` <br>

## Meta
`<meta >` : balise pour les métadonnées d'une page
exemple :
```
<meta charset="UTF-8"›
‹meta name="description" content="Free HTML tutorial for beginners"›
‹meta name="keywords" content="HTML, tutorial, beginners"›
‹meta name="author" content="Bro Code"> I
‹meta name="viewport" content="width=device-width, initial-scale=1.0"›
‹meta http-equiv="refresh" content="30"])
```

*Résponsive*
`<meta name="viewport" content="width=device-width"/>` : s'adapte aux différentes tailles d'écran<br>
	`name="viewport"` :  zone visible de la page dans la fenêtre du navigateur.<br>
	`content="width=device-width"` : la largeur de la page web doit s'adapter à la largeur de l'appareil<br>

### Entités
& : `&amp;`<br>
< : `&lt;`<br>
`>` : `&gt;`<br>
" : `&quot;`<br>
' : `&apos;`<br>
(Espace) : `&nbsp;`<br>
– : `&ndash;`
— : `&mdash;`<br>
© : `&copy;`<br>
® : `&reg;`<br>
™ : `&trade;`<br>
≈ : `&asymp;`<br>
≠ : `&ne;`<br>
£ : `&pound;`<br>
€ : `&euro;`<br>
° : `&deg;`<br>

	exemple : `<p>Distance : 10&nbsp;km</p>`
<p>Distance : 10&nbsp;km</p>

# CSS
Changer le style d'un `<span>` et `<div>`<br>
`<p><span style="background-color:tomato; "> Ceci est un span</span></p>`<br>
<span style="background-color:tomato; "> Ceci est un span rouge</span><br>
<div style="background-color:green; "> Ceci est une div</div><br>

Changer le style de la class "my-group"<br>
exemple : 
```
.my-group {
background-color: red;
}
```

Sélectionner une balise spécifique pour lui ajouter un style<br>
```
#myHeader {
	background-color: lightblue;
	color: black;
	padding: 40px;
	text-align: center;
}
```