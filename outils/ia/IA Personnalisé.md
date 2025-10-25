---
layout: default
title: IA Personnalisé
parent: IA
grand_parent: Outils
nav_order: 6
---

# IA Personnalisé
## Contexte
> Je souhaiterais obtenir des recommandations de films adaptées à mes goûts. Pour cela, je propose de créer une intelligence artificielle qui s'appuie sur une base de données de films afin de suggérer les titres les plus pertinents.
## Exigence
- Base de données comprenant :
    - Films déjà visionnés (plus il y en a, mieux c'est)
    - Liste de films à regarder
Ces critères permettront à l'IA d'analyser vos préférences en matière de films.
### Exemple
- Invite : Propose-moi un film de ma liste de souhaits ainsi qu'un film qui correspond au style des films que j'ai déjà vus.
- Le fichier contenant les films visionnés et la liste des films à voir est joint au message.
## Étapes à suivre
1. Créer un compte sur [poe](https://poe.com/)
2. Aller sur la page de [création de bot](https://poe.com/create_bot)
3. Sélectionner "Bot d'invite"
4. Personnalisez le nom, la photo et la description selon vos préférences
5. Dans le champ "invite", indiquez le contexte (voir l'exemple)
6. Dans la section "base de connaissance" importer le fichier texte contenant les films vus et la liste de films à voir (voir l'exemple dans le fichier)
    1. Il est préférable de décocher "Citer les sources" afin d'avoir un résultat plus propre
7. Puis publier le bot et tester

Ce tuto est évidemment applicable sur d'autres utilisations. Je l'ai personnellement utilisé pour créer une IA répondant à des clients à ma place avec des exemples de réponse déjà faite et des indications sur diverses choses telles que le prix de déplacement, une grille tarifaire, etc.

Exemple de base de donnée
```
Watchlist:
Hundreds of Beavers (2022)
Memoir of a Snail (2024)
Wallace & Gromit: The Curse of the Were-Rabbit (2005)
Black Swan (2010)
The Call (2020)
The Chaos Class (1975)
Speed Racer (2008)
Mind Game (2004)
Quarantine (2008)
Missing (2023)


Films vus:
[Rec] (2007)
The Wrong Trousers (1993)
The Blair Witch Project (1999)
Alien (1979)
Perfect Blue (1997)
```