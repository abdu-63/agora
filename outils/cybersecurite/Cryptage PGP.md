---
layout: default
title: Cryptage PGP
parent: Cybersécurité
grand_parent: Outils
nav_order: 3
---

# Cryptage PGP
>Tutoriel pour GPG Suite

Après avoir installé [GPG Suite](https://gpgtools.org/), ouvrir GPG Keychain, puis cliquer sur le "+" et créer sa clé personnelle (pour plus de sécurité, utiliser ne pas mettre de mail OU utiliser Proton Mail ou DNMX).

Pour décrypter un message, il va falloir importer la clé publique de la personne en question. Pour ce faire, copier sa clé publique, ouvrir GPG Keychain, un popup va apparaître pour ajouter le contact. Sinon, cliquer sur le bouton "Importer" et ouvrir le fichier PGP en .asc envoyer par la personne.
Maintenant que la clé publique de la personne est importée, on peut décrypter son message.

Pour ce faire sélectionner son message et faire clic droit dessus, sélectionner "Services" et cliquer sur "OpenPGP : déchiffrer la sélection" ou "OpenPGP : déchiffrer la sélection dans une nouvelle fenêtre"

Pour chiffrer et partager ses messages, écrire son message, puis sélectionner le message et faire clic droit dessus, sélectionner "Services" et cliquer sur "OpenPGP : chiffrer la sélection" ou "OpenPGP : chiffrer la sélection dans une nouvelle fenêtre".
Bien sûr, afin que la personne puisse décrypter votre message, votre clé publique doit être enregistrée dans son répertoire, sinon le déchiffrage sera impossible.

Merci d'avoir lu. Bisous !
Pour un tuto pour Windows, visionnez [cette vidéo](https://www.youtube.com/watch?v=cdE5haNGa28&t=292s)