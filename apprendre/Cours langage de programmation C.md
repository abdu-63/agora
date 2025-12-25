---
layout: default
title: Cours langage de programmation C
parent: Apprendre
nav_order: 1
---

# Cours langage de programmation C
**Un guide complet pour débuter en programmation C**

## Introduction au langage C

> Le langage C est un langage de programmation créé en 1972 par Dennis Ritchie. C'est un langage de bas niveau très performant, encore largement utilisé aujourd'hui pour le développement système, les systèmes embarqués, et comme base d'apprentissage de la programmation.

## 1. Structure d'un programme C

Tout programme C suit une structure de base :
```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```
**Explications :**
- `#include <stdio.h>` : directive du préprocesseur qui inclut la bibliothèque standard d'entrées/sorties
- `int main()` : fonction principale, point d'entrée du programme
- `printf()` : fonction pour afficher du texte
- `return 0` : indique que le programme s'est terminé correctement

***
## 2. Les variables et types de données
### Types de base

```c
int age = 25;              // Entier
float prix = 19.99;        // Nombre décimal (simple précision)
double pi = 3.14159265;    // Nombre décimal (double précision)
char lettre = 'A';         // Caractère
char nom[50] = "Alice";    // Chaîne de caractères
```
### Affichage des variables
```c
printf("Age: %d\n", age);
printf("Prix: %.2f\n", prix);
printf("Pi: %.8lf\n", pi);
printf("Lettre: %c\n", lettre);
printf("Nom: %s\n", nom);
```
### Contrôler la précision après la virgule
```c
printf("Prix: %.2f\n", prix);   // Affiche 2 décimales : 19.99
printf("Pi: %.8lf\n", pi);      // Affiche 8 décimales : 3.14159265
printf("Pi: %.2lf\n", pi);      // Affiche 2 décimales : 3.14
```
### Déclaration et initialisation

```c
int x;           // Déclaration
x = 10;          // Initialisation
int y = 20;      // Déclaration et initialisation combinées
```
***
## 3. Les opérateurs

### Opérateurs arithmétiques

```c
int a = 10, b = 3;
int somme = a + b;        // Addition (13)
int difference = a - b;   // Soustraction (7)
int produit = a * b;      // Multiplication (30)
int quotient = a / b;     // Division entière (3)
int reste = a % b;        // Modulo (1)
```
### Opérateurs de comparaison

```c
a == b    // Égal à
a != b    // Différent de
a > b     // Supérieur à
a < b     // Inférieur à
a >= b    // Supérieur ou égal à
a <= b    // Inférieur ou égal à
```
### Opérateurs logiques

```c
&&    // ET
||    // OU
!     // NON (inverse)
```
***
## 4. Les structures de contrôle

### Conditions (if/else)
Pour un choix simple

```c
int age = 18;

if (age >= 18) {
    printf("Vous êtes majeur\n");
} else if (age >= 13) {
    printf("Vous êtes adolescent\n");
} else {
    printf("Vous êtes enfant\n");
}
```
### Switch
Les switch cases sont souvent utilisés pour les menus avec beaucoup de choix

```c
int jour = 3;

switch (jour) {
    case 1:
        printf("Lundi\n");
        break;
    case 2:
        printf("Mardi\n");
        break;
    case 3:
        printf("Mercredi\n");
        break;
    default:
        printf("Autre jour\n");
}
```
***
## 5. Les boucles

### Boucle for
Répète de 0 à 5 exclus avec une incrémentation de 1 (comme Un+1)

```c
for (int i = 0; i < 5; i++) {
    printf("Itération %d\n", i);
}
```
### Boucle while
Répète jusqu'à atteindre 5 exclus

```c
int compteur = 0;
while (compteur < 5) {
    printf("Compteur: %d\n", compteur);
    compteur++;
}
```
### Boucle do-while
Répète jusqu'à atteindre 5 exclus en essayant au moins une fois

```c
int i = 0;
do {
    printf("i = %d\n", i);
    i++;
} while (i < 5);
```
***
## 6. Les fonctions

```c
// Déclaration et définition d'une fonction
int additionner(int a, int b) {
    return a + b;
}

// Utilisation
int main() {
    int resultat = additionner(5, 3);
    printf("Résultat: %d\n", resultat);
    return 0;
}
```
### Fonction sans retour (void)

```c
void afficherMessage() {
    printf("Bonjour!\n");
}
```
***
## 7. Les tableaux

### Tableaux unidimensionnels

```c
int nombres[5] = {10, 20, 30, 40, 50};

// Accès aux éléments
printf("%d\n", nombres[0]);  // Affiche 10

// Parcourir un tableau
for (int i = 0; i < 5; i++) {
    printf("%d ", nombres[i]);
}
```
### Tableaux multidimensionnels

```c
int matrice[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

printf("%d\n", matrice[1][2]);  // Affiche 6
```
***
## 8. Les pointeurs (introduction)
Les pointeurs sont une notion fondamentale, mais complexe en C.

```c
int x = 10;
int *ptr = &x;  // ptr contient l'adresse de x

printf("Valeur de x: %d\n", x);
printf("Adresse de x: %p\n", &x);
printf("Valeur pointée par ptr: %d\n", *ptr);
```

Pour accéder à une valeur pointé sur une structure, on ne met pas ex:
`*p.element` mais on met `*p -> element`

***
## 9. Les structures

```c
// Définition du nouveau type "Etudiant"
typedef struct {
    char nom[50];
    int age;
    float moyenne;
} Etudiant;  // "Etudiant" devient le nom du type
```
**Avec Pointeur**
> déclaration fonction=> .h

`(void proc1(mastruct* p));`
p= adresse d'une variable mastruct

`p -> a = 2;`
`*p.a` (identique, mais à ne pas écrire mauvaise syntaxe)
Accès à la variable a à l'intérieur de la structure pointée par p

Exemple dans un `main`
```c
#include <stdio.h>
#include <string.h> // Nécessaire pour strcpy

int main() {
    // Déclaration simple (comme: int x;)
    Etudiant e1;
    
    // Initialisation des champs
    e1.age = 20;
    e1.moyenne = 15.5;
    
    // Attention : pour les chaînes, on utilise strcpy (String Copy)
    // On ne peut pas faire : e1.nom = "Thomas";
    strcpy(e1.nom, "Thomas");

    // Autre méthode : Déclaration et initialisation immédiate
    Etudiant e2 = {"Marie", 22, 18.0};

    // Affichage
    printf("Etudiant 1 : %s, Moyenne : %.2f\n", e1.nom, e1.moyenne);
    printf("Etudiant 2 : %s, Moyenne : %.2f\n", e2.nom, e2.moyenne);

    return 0;
}
```

## 10. Aléatoire
```
# include <time.h> // Nécessaire pour utiliser time()

rand()           // Aléatoire simple (répétitif)
rand(time(NULL)) // Aléatoire avec le temps
```
***
## 11. Les entrées/sorties

### Affichage (printf)

```c
int age = 25;
float taille = 1.75;

printf("J'ai %d ans\n", age);
printf("Je mesure %.2f m\n", taille);
```
### Saisie (scanf)

```c
int nombre;
printf("Entrez un nombre: ");
scanf("%d", &nombre);
printf("Vous avez saisi: %d\n", nombre);
```
***
## 12. Exemple complet

Voici un programme qui calcule la moyenne de notes :

```c
#include <stdio.h>

float calculerMoyenne(float notes[], int taille) {
    float somme = 0;
    for (int i = 0; i < taille; i++) {
        somme += notes[i];
    }
    return somme / taille;
}

int main() {
    float notes[5];
    int nbNotes = 5;
    
    printf("Entrez 5 notes:\n");
    for (int i = 0; i < nbNotes; i++) {
        printf("Note %d: ", i + 1);
        scanf("%f", &notes[i]);
    }
    
    float moyenne = calculerMoyenne(notes, nbNotes);
    printf("\nMoyenne: %.2f\n", moyenne);
    
    if (moyenne >= 10) {
        printf("Admis!\n");
    } else {
        printf("Recalé!\n");
    }
    
    return 0;
}
```

