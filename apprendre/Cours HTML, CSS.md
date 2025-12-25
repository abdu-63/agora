---
layout: default
title: Cours HTML, CSS
parent: Apprendre
nav_order: 3
---

# Cours HTML, CSS (pas à jours)
- [[#Base d'un code HTML|Base d'un code HTML]]
	- [[#Tags textuels|Tags textuels]]
	- [[#Balise d'action|Balise d'action]]
- [[#CSS|CSS]]

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

`<!DOCTYPE html>` : informe le navigateur que le document est un HTML5
`<html>` : englobant tous les autres éléments HTML
`<head>` : métadonnées sur le document
`<body>` : contenu visible de la page Web
`<meta>` : métadonnées comme l'encodage de caractère (`charset="UTF-8"`) assurer un affichage de texte approprié.
### Commentaire
`<!-- je suis un commentaire -->`

## Tags textuels
`<h1>` jusqu'à `<h6>` : Titres
`<title>` : titre de la page
`<p>` : paragraphe
***Bloc***
	`<div>` : balise entière (largeur)
	`<span>` : uniquement la balise incluse
`class` : sélectionner uniquement les balises avec un tag
	exemple : `‹p class="my-group"›This is another paragraph. ‹/p›`

## Tag 
`<center>` : centrer un texte
`<br>` : saut de lignes
`<hr>` : ligne pour séparer
`<pre>` : afficher comme écrit dans le code (afficher du code)
`&nbsp;` : ajout d'un espace blanc
`<ul>` : liste a puce
`<ol>` : liste numéroté
	`<li>` : pour les éléments de la liste

## Formatage
`<b>` : <b>Texte en gras</b>
`<strong>` : <strong>Texte important</strong> (généralement affiché en gras)
`<i>` : <i>Texte en italique</i>
`<em>` : <em>Texte mis en valeur</em> (accentuation, généralement en italique)
`<mark>` : <mark>Texte marqué ou surligné</mark>
`<small>` : <small>Texte plus petit</small>
`<del>` : <del>Texte supprimé</del> (barré)
`<ins>` : <ins>Texte inséré (souligné)</ins>
`<sub>` : Texte en <sub>indice</sub>
`<sup>` : Texte en <sup>exposant</sup>

## Attribues
`style` : ajouter des styles à un élément (CSS)
	exemple : `<p style="color:red;">This is a red paragraph.</p>`
`title` : extra Information sur un élément (texte avec la souris dessus)
	exemple : `<p title="I'm a tooltip">This is a paragraph.</p>`

`lang` : définir la langue de la page
	exemple : `<html lang="en">`

`<id>` : retrouver plus facilement une balise
	exemple : `<h1 id="myHeader"› My Header</h1>`
		exemple : `‹a href="#C12"›Jump to Chapter</a>` (sommaire)
## Balise d'action
`<a>` : Insérer un lien 
	`href` : URL de la page
		exemple : `<a href="https://url.com">This is a link</a>`
`<img>` : Insérer une image 
	`src` : chemin d'accès à l'image
	`alt` : texte alternatif pour une image
	`width`, `height` : largeur et hauteur de l'image
		exemple : `<img src="image.jpg" alt="image.com" width="104" height="142">`

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
`<meta name="viewport" content="width=device-width"/>` : s'adapte aux différentes tailles d'écran
	`name="viewport"` :  zone visible de la page dans la fenêtre du navigateur.
	`content="width=device-width"` : la largeur de la page web doit s'adapter à la largeur de l'appareil

### Entités
& : `&amp;`
< : `&lt;`
`>` : `&gt;`
" : `&quot;`
' : `&apos;`
(Espace) : `&nbsp;`
– : `&ndash;`
— : `&mdash;`
© : `&copy;`
® : `&reg;`
™ : `&trade;`
≈ : `&asymp;`
≠ : `&ne;`
£ : `&pound;`
€ : `&euro;`
° : `&deg;`

	exemple : `<p>Distance : 10&nbsp;km</p>`
<p>Distance : 10&nbsp;km</p>

# CSS
Changer le style d'un `<span>` et `<div>`
`<p><span style="background-color:tomato; "> Ceci est un span</span></p>`
<span style="background-color:tomato; "> Ceci est un span rouge</span>
<div style="background-color:green; "> Ceci est une div</div>

Changer le style de la class "my-group" - [[#Tags textuels|Tags textuels]]
exemple : 
```
.my-group {
background-color: red;
}
```

Sélectionner une balise spécifique pour lui ajouter un style  - [[#Attribues|Attribues]]
```
#myHeader {
	background-color: lightblue;
	color: black;
	padding: 40px;
	text-align: center;
}
```