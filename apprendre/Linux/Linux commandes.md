---
layout: default
title: Linux commandes
parent: Linux
grand_parent: Apprendre
nav_order: 3
---

# Linux commandes

## Commandes de base
`cd`ouvrir un dossier
`cd ..` revenir au dossier parent
`ls`voir les fichiers dans un dossier
	`ls -l` donne plus d'infos sur chaque fichier
	`ls -r` affichera les résultats dans l'ordre alphabétique inverse
		`ls -lr` fait les commande `-l` et `-r`
`pwd` affiche le répertoire de travail
`~$`aller dans le répertoire personnel de l'utilisateur

| Symbole | Type de fichier                        | Description                                                                                          |
| ------- | -------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `d`     | répertoire                             | Un fichier utilisé pour stocker d'autres fichiers.                                                   |
| `-`     | fichier                                | Inclut des fichiers lisibles, des fichiers images, des fichiers binaires et des fichiers compressés. |
| `l`     | lien symbolique                        | Pointe vers un autre fichier.                                                                        |
| `s`     | prise (socket)                         | Permet la communication entre les processus.                                                         |
| `p`     | tuyau (pipe)                           | Permet la communication entre les processus.                                                         |
| `b`     | fichier bloc (block file)              | Utilisé pour communiquer avec le matériel.                                                           |
| `c`     | fichier de caractères (character file) | Utilisé pour communiquer avec le matériel.                                                           |
## Accès administratif
Pour se login
`su -`
`su -l`
`su --login`
`exit` déconnecter
`sudo` exécuter des commandes avec des privilèges d'administrateur
`sudo passwrd root` change le mot de passe du root
## Modification des permissions de fichier
ajouter `./` pour exécuter un script
`chmod` changer les permissions d'accès
	u = user, g = group, o = others
	r = read, w = write, x = execute
exemple : `chmod u+rw,g=w,o= run.sh`
## Modification de la propriété des fichiers
`chown` modifier la propriété des fichiers
## Affichage des fichiers
`touch` créer un fichier
`cat` lire un fichier
`head`affiche les 10 premières lignes d'un fichier
`tail` affiche les 10 dernières lignes d'un fichier
## Copie de fichiers
`cp`copier un fichier
## Déplacement de fichiers
`mv` déplacer des fichiers
## Suppression de fichiers
`rm` pour supprimer des fichiers
	`rm -r` supprimer un dossier
## Filtrage d'entrée
`grep` filtrer les informations sur un utilisateur spécifique
tableau avec `egrep`
## Expressions régulières

| Caractères regex étendus | Signification                                                            |
| ------------------------ | ------------------------------------------------------------------------ |
| `+`                      | Un ou plusieurs du motif précédent                                       |
| `?`                      | Le motif précédent est optionnel                                         |
| `{ }`                    | Spécifier correspondances minimum, maximum ou exactes du motif précédent |
| `\|`                     | Alternance - un "ou" logique                                             |
| `( )`                    | Utilisé pour créer des groupes                                           |
## Arrêt
`shutdown` `now` arrêter la machine maintenant
## Configuration réseau
`ifconfig` afficher les informations de configuration réseau
`ping` vérifier la connectivité entre deux ordinateurs
	`-c` limiter le nombre de pings envoyés
	ex `-c 4` limité à 4 itérations
## Affichage des processus
`ps` lister les processus
`-e` affichera tous les processus
`-f` plus de détails dans l'affichage de la commande
## Gestion des paquets
Nécessite souvent un accès admin
*Installation de paquets*
`apt-get update` réactualiser la liste des paquets
`apt-cache search` rechercher des mots-clés dans ces paquets
`apt-get install` installer un paquet
*Mise à jour des paquets*
`apt-get update` mise à jour du cache
`apt-get upgrade` mise à jour des paquet
*Suppression de paquets*
`apt-get remove` supprimer un paquet
`apt-get purge` purger un paquet entièrement du système
## Mise à jour des mots de passe utilisateur
`passwd` modifier le mot de passe
	`-S` voir l'état de son mot de passe
## Éditeur de texte
`nano` afficher l'éditeur de texte
`sudo nano` afficher l'éditeur de texte "en mieux"
`vi` Éditeur de texte
	ex `vi newfile.txt`

|Mouvement|Résultat|
|---|---|
|`h`|Un caractère à gauche|
|`j`|Descendre d'une ligne|
|`k`|Monter d'une ligne|
|`l`|Un caractère à droite|
|`w`|Un mot en avant|
|`b`|Un mot en arrière|
|`^`|Début de ligne|
|`$`|Fin de ligne|
`>` écraser un texte par un autre dans un fichier
`>>` ajouter un nouveau texte après un autre dans un fichier

## Gestion des utilisateurs
### Les utilisateurs
`useradd USERNAME` Ajout d'un utilisateur
	`passwd USERNAME` donner un mot de passe
`deluser --remove-home USERNAME` Supprimer un utilisateur
			Supprime son rep perso
`su - USERNAME` Changer d'utilisateur
`su USERNAME` Changer d'utilisateur juste pour la commande suivante

Pour passer en mode root :
`su root` root juste pour la commande suivante (répertoire personnel ne change pas)
`su - root` ou `sudo -i` changement complet de session `en root` (répertoire personnel change (/root)
Pour vérifier qui on est : `whoami` et pour voir le répertoire courant : `pwd`
### Les groupes
Un utilisateur appartient à plusieurs groupes : un principal et plusieurs secondaires
`addgroup GROUPNAME` Créer un groupe
`usermod -aG GROUPNAME USERNAME` Ajouter un utilisateur à un groupe (secondaire) :
`usermod -g GROUPNAME USERNAME` Pour changer le groupe principal d'un utilisateur
`groups USERNAME` Aﬃcher les groupes d'un utilisateur
	le 1er est le groupe principal suivi par les secondaires
	`groups` sans argument aﬃche tous les groupes de l'`utilisateur en cours`
Pour attribuer des privilèges root à un utilisateur on doit l'ajouter au groupe `sudo usermod -aG sudo USERNAME`
## Authentification, autorisation et journalisation
`cat /etc/group` Vérifie que le nouveau groupe a été ajouté
`usermod –G HR jenny` Intègre l'utilisateur jenny dans le groupe HR
`cat /etc/passwd` Vérifie les nouveaux utilisateurs créés dans le fichier passwd
`cat /etc/shadow` Affiche les utilisateurs créés dans le fichier shadow

`CTRL+ALT+F3` Accéder au terminal tty3
`CTRL+ALT+F4` Accéder au terminal tty4
`ALT + flèche de gauche` Quitte le terminal tty

## Le mode octal
exemple : `chmod 574 run.sh` défini les droits r-x pour user (le 5), etc...

| ---: 000 | 0+0+0 | 0   |
| -------- | ----- | --- |
| --x: 001 | 0+0+1 | 1   |
| -w-: 010 | 0+2+0 | 2   |
| -wx: 011 | 0+2+1 | 3   |
| r--: 100 | 4+0+0 | 4   |
| r-x: 101 | 4+0+1 | 5   |
| rw-: 110 | 4+2+0 | 6   |
| rwx: 111 | 4+2+1 | 7   |

## Chercher des fichiers
`find . -name "*.txt"` find chercher des fichiers ou des répertoires
	`.` indique le répertoire (ici le répertoire actuel)
	`-name` fichier ou répertoire dont le nom correspond exactement
	`-type f` recherche uniquement les fichiers
	`-type d` recherche uniquement les répertoires
	`"nom_du_fichier_ou_extension"` affiche le nom correspondant exactement
	`"*.txt"` affiche tous les .txt peu importe le nom du fichier 