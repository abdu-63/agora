---
layout: default
title: TP 1 HTML
parent: TP
grand_parent: Apprendre
nav_order: 2
---

# TP 1 Créer "Ma Page de Profil"

#### Objectif
Créer un fichier nommé `index.html` qui présente une personne, ses compétences et un moyen de la contacter, en utilisant les balises vues dans tes notes.
***
### Étape 1 : La Structure de base
Crée le squelette de ton fichier HTML. Comme indiqué dans tes notes, tu dois informer le navigateur que c'est du HTML5 et définir l'encodage.

- **Consigne :**
    1. Commence par le `<!DOCTYPE html>`.
    2. Ajoute les balises `<html>`, `<head>` et `<body>`.
    3. Dans le `<head>`, ajoute l'encodage `UTF-8` et un `<title>` (par exemple : "Profil de [Ton Nom]").
    4. Ajoute aussi la balise meta viewport pour que la page soit _responsive_ (s'adapte aux écrans).

### Étape 2 : Le Titre et la Présentation
Dans le `<body>` (contenu visible), nous allons ajouter les titres et les paragraphes.

- **Consigne :**
    1. Ajoute un titre principal `<h1>` avec ton nom (ou celui du personnage).
    2. Ajoute un sous-titre `<h2>` (de `<h1>` à `<h6>`) intitulé "Qui suis-je ?".
    3. Rédige un paragraphe `<p>` de présentation. À l'intérieur de ce paragraphe, utilise :
        - Une balise `<b>` ou `<strong>` pour mettre un mot important en gras.
        - Une balise `<i>` ou `<em>` pour mettre un mot en italique.

### Étape 3 : Liste de compétences et Loisirs
Utilisons les listes pour structurer l'information.

- **Consigne :**
    1. Sépare cette section de la précédente avec une ligne horizontale `<hr>`.
    2. Ajoute un titre "Mes Compétences".
    3. Crée une liste à puces `<ul>` avec au moins 3 éléments `<li>` (ex: HTML, CSS, Sport).
    4. Ajoute un titre "Mon Top 3 Films/Jeux".
    5. Crée une liste numérotée `<ol>` avec 3 éléments `<li>`.

### Étape 4 : Multimédia et Liens
Il est temps d'ajouter une image et un lien vers une autre page.

- **Consigne :**
    1. Ajoute une photo de profil (ou une image quelconque) avec la balise `<img>`. N'oublie pas les attributs `src`, `alt`, et définis une `width` (largeur) de 200px.
    2. Ajoute un saut de ligne `<br>` après l'image.
    3. Ajoute un lien `<a>` vers ton site préféré (ex: Google ou Wikipédia) avec 

### Étape 5 : Un peu de Style (CSS)
Tes notes mentionnent comment ajouter du style directement dans les balises ou via un ID.

- **Consigne :**
    1. Change la couleur de ton titre `<h1>` en utilisant l'attribut `style="color:red;"` (ou une autre couleur).
    2. Ajoute un `id="mon-footer"` au dernier paragraphe de ta page.
    3. (Optionnel) Dans le `<head>`, ajoute une balise `<style>` pour cibler cet ID et lui donner une couleur de fond, comme montré dans la section CSS de tes notes :
```css
#mon-footer {
	background-color: lightblue;
	text-align: center;
}
```
***
### Correction (Code attendu)

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Profil de Développeur</title>
  
  <style>
    /* Style basé sur la section CSS de tes notes */
    #mon-footer {
        background-color: lightblue;
        padding: 20px;
        text-align: center;
    }
    .important {
        background-color: yellow; /* Exemple d'usage de classe */
    }
  </style>
</head>
<body>

  <h1 style="color: navy;">Bienvenue sur mon profil</h1>

  <h2>Qui suis-je ?</h2>
  <p>
    Bonjour ! Je suis un étudiant en <strong>développement Web</strong>. 
    J'apprends le HTML et c'est <em>très intéressant</em>.
  </p>

  <hr>

  <h2>Mes Compétences</h2>
  <ul>
    <li>HTML5</li>
    <li>CSS3</li>
    <li>Logique de programmation</li>
  </ul>

  <h2>Mon Top 3</h2>
  <ol>
    <li>The Matrix</li>
    <li>Interstellar</li>
    <li>Inception</li>
  </ol>

  <h2>Ma Photo</h2>
  <img src="https://via.placeholder.com/150" alt="Photo de profil générique" width="150" height="150">
  
  <br><br>

  <p>Visitez mon moteur de recherche favori : <a href="https://www.google.com">Google</a></p>

  <div id="mon-footer">
    <p>Contactez-moi : email@exemple.com</p>
    <p>&copy; 2024 - Tous droits réservés</p>
  </div>

</body>
</html>
```

