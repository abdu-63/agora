---
layout: default
title: Github git
parent: Tutoriels
nav_order: 2
---

# Github git
## Télécharger le repo sur son disque
1. Aller sur la page du repo
2. Cliquer sur <> Code et copier l'URL
3. Ecrire dans le terminal `git clone url_du_repo_copié`
4. Le dossier du repo sera ensuite téléchargé et des modifications pourront y être apportées
## Envoyer ses modifications sur le repo
1. Aller dans le dossier du projet `cd mon_projet`
2. Ajouter les fichiers avec la commande `git add .` (le . veut dire tous les fichiers)
3. Envoyer un "commit" `git commit -m "Ajout de mes nouveaux fichiers"` (décrire le nom du commit entre les guillemets)
4. Envoyer les fichiers avec `git push`
## Autres
- Retirer les fichiers DS_Store `git rm --cached "**/.DS_Store"`