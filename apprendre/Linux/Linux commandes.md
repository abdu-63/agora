---
layout: default
title: Linux commandes
parent: Linux
grand_parent: Apprendre
nav_order: 3
---

# Linux commandes

## Commandes de base
`cd`ouvrir un dossier<br>
`cd ..` revenir au dossier parent<br>
`ls`voir les fichiers dans un dossier<br>
	`ls -l` donne plus d'infos sur chaque fichier<br>
	`ls -r` affichera les résultats dans l'ordre alphabétique inverse<br>
		`ls -lr` fait les commande `-l` et `-r`<br>
`pwd` affiche le répertoire de travail<br>
`~$`aller dans le répertoire personnel de l'utilisateur<br>

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
Pour se login<br>
`su -`<br>
`su -l`<br>
`su --login`<br>
`exit` déconnecter<br>
`sudo` exécuter des commandes avec des privilèges d'administrateur<br>
`sudo passwrd root` change le mot de passe du root<br>
## Modification des permissions de fichier
ajouter `./` pour exécuter un script<br>
`chmod` changer les permissions d'accès<br>
	u = user, g = group, o = others<br>
	r = read, w = write, x = execute<br>
exemple : `chmod u+rw,g=w,o= run.sh`<br>
## Modification de la propriété des fichiers
`chown` modifier la propriété des fichiers<br>
## Affichage des fichiers
`touch` créer un fichier<br>
`cat` lire un fichier<br>
`head`affiche les 10 premières lignes d'un fichier<br>
`tail` affiche les 10 dernières lignes d'un fichier<br>
## Copie de fichiers
`cp`copier un fichier<br>
## Déplacement de fichiers
`mv` déplacer des fichiers<br>
## Suppression de fichiers
`rm` pour supprimer des fichiers<br>
	`rm -r` supprimer un dossier<br>
## Filtrage d'entrée
`grep` filtrer les informations sur un utilisateur spécifique<br>
tableau avec `egrep`<br>
## Expressions régulières

| Caractères regex étendus | Signification                                                            |
| ------------------------ | ------------------------------------------------------------------------ |
| `+`                      | Un ou plusieurs du motif précédent                                       |
| `?`                      | Le motif précédent est optionnel                                         |
| `{ }`                    | Spécifier correspondances minimum, maximum ou exactes du motif précédent |
| `\|`                     | Alternance - un "ou" logique                                             |
| `( )`                    | Utilisé pour créer des groupes                                           |
## Arrêt
`shutdown` `now` arrêter la machine maintenant<br>
## Configuration réseau
`ifconfig` afficher les informations de configuration réseau<br>
`ping` vérifier la connectivité entre deux ordinateurs<br>
	`-c` limiter le nombre de pings envoyés<br>
	ex `-c 4` limité à 4 itérations<br>
## Affichage des processus
`ps` lister les processus<br>
`-e` affichera tous les processus<br>
`-f` plus de détails dans l'affichage de la commande<br>
## Gestion des paquets
Nécessite souvent un accès admin<br>
*Installation de paquets*<br>
`apt-get update` réactualiser la liste des paquets<br>
`apt-cache search` rechercher des mots-clés dans ces paquets<br>
`apt-get install` installer un paquet<br>
*Mise à jour des paquets*<br>
`apt-get update` mise à jour du cache<br>
`apt-get upgrade` mise à jour des paquet<br>
*Suppression de paquets*<br>
`apt-get remove` supprimer un paquet<br>
`apt-get purge` purger un paquet entièrement du système<br>
## Mise à jour des mots de passe utilisateur
`passwd` modifier le mot de passe<br>
	`-S` voir l'état de son mot de passe<br>
## Éditeur de texte
`nano` afficher l'éditeur de texte<br>
`sudo nano` afficher l'éditeur de texte "en mieux"<br>
`vi` Éditeur de texte<br>
	ex `vi newfile.txt`<br>

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
`>` écraser un texte par un autre dans un fichier<br>
`>>` ajouter un nouveau texte après un autre dans un fichier<br>

## Gestion des utilisateurs
### Les utilisateurs
`useradd USERNAME` Ajout d'un utilisateur<br>
	`passwd USERNAME` donner un mot de passe<br>
`deluser --remove-home USERNAME` Supprimer un utilisateur<br>
			Supprime son rep perso<br>
`su - USERNAME` Changer d'utilisateur<br>
`su USERNAME` Changer d'utilisateur juste pour la commande suivante<br>

Pour passer en mode root :<br>
`su root` root juste pour la commande suivante (répertoire personnel ne change pas)<br>
`su - root` ou `sudo -i` changement complet de session `en root` (répertoire personnel change (/root)<br>
Pour vérifier qui on est : `whoami` et pour voir le répertoire courant : `pwd`<br>
### Les groupes
Un utilisateur appartient à plusieurs groupes : un principal et plusieurs secondaires<br>
`addgroup GROUPNAME` Créer un groupe<br>
`usermod -aG GROUPNAME USERNAME` Ajouter un utilisateur à un groupe (secondaire) :<br>
`usermod -g GROUPNAME USERNAME` Pour changer le groupe principal d'un utilisateur<br>
`groups USERNAME` Aﬃcher les groupes d'un utilisateur<br>
	le 1er est le groupe principal suivi par les secondaires<br>
	`groups` sans argument aﬃche tous les groupes de l'`utilisateur en cours`<br>
Pour attribuer des privilèges root à un utilisateur on doit l'ajouter au groupe `sudo usermod -aG sudo USERNAME`<br>
## Authentification, autorisation et journalisation
`cat /etc/group` Vérifie que le nouveau groupe a été ajouté<br>
`usermod –G HR jenny` Intègre l'utilisateur jenny dans le groupe HR<br>
`cat /etc/passwd` Vérifie les nouveaux utilisateurs créés dans le fichier passwd<br>
`cat /etc/shadow` Affiche les utilisateurs créés dans le fichier shadow<br>

`CTRL+ALT+F3` Accéder au terminal tty3<br>
`CTRL+ALT+F4` Accéder au terminal tty4<br>
`ALT + flèche de gauche` Quitte le terminal tty<br>

## Le mode octal
exemple : `chmod 574 run.sh` défini les droits r-x pour user (le 5), etc...<br>

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
`find . -name "*.txt"` find chercher des fichiers ou des répertoires<br>
	`.` indique le répertoire (ici le répertoire actuel)<br>
	`-name` fichier ou répertoire dont le nom correspond exactement<br>
	`-type f` recherche uniquement les fichiers<br>
	`-type d` recherche uniquement les répertoires<br>
	`"nom_du_fichier_ou_extension"` affiche le nom correspondant exactement<br>
	`"*.txt"` affiche tous les .txt peu importe le nom du fichier<br>