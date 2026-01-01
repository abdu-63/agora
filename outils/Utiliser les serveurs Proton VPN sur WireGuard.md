---
layout: default
title: Utiliser les serveurs Proton VPN sur WireGuard
parent: Outils
nav_order: 18
---

# Utiliser les serveurs Proton VPN sur WireGuard

### Phase 1 : Générer le fichier de configuration (Sur le site Proton)

Cette étape est identique pour Mac et Windows. Elle permet de créer la "clé" pour se connecter.

1. Connectez-vous à votre [Tableau de bord Proton VPN](https://account.protonvpn.com).
2. Dans le menu à gauche, allez sur **Téléchargements** > **Configuration WireGuard**.
3. **Nommez la configuration (optionnel) :** Donnez un nom simple (ex: `MonMac-Free` ou `PC-Free`).
4. **Options techniques :**
**NAT-PMP :** Laissez décoché (option payante, grisée).
**VPN Accelerator :** Laissez **coché** (activé) pour maximiser la vitesse.

5. **Filtrer les serveurs gratuits :**
* Sous la mention "Ou sélectionnez un serveur spécifique", cochez le bouton du milieu : **Configurations des serveurs Free**.

6. **Télécharger le fichier :**
* Dans la liste qui s'affiche juste en dessous, choisissez un serveur dans un pays qui vous convient (ex: Pays-Bas `NL-FREE#...` ou États-Unis `US-FREE#...`).
* Cliquez sur l'icône **Télécharger** (la flèche vers le bas) à droite de la ligne.
* Vous obtenez un fichier `.conf`.

---

### Phase 2 : Installation sur macOS

C'est la méthode "propre" via l'App Store.

1. **Télécharger l'application :**
* Ouvrez le **Mac App Store**.
* Recherchez **"WireGuard"** et installez l'application (gratuite).

2. **Importer le fichier :**
* Ouvrez l'application WireGuard (icône dans la barre des menus en haut).
* Cliquez sur **"Import Tunnel(s) from File"**.
* Sélectionnez le fichier `.conf` que vous venez de télécharger.
* Cliquez sur **Autoriser** si macOS vous demande la permission d'ajouter une configuration VPN.

3. **Se connecter :**
* Cliquez sur le bouton **Activate**.
* Si le point devient vert, c'est gagné.

---

### Phase 3 : Installation sur Windows

1. **Télécharger l'application :**
* Allez sur [wireguard.com/install](https://www.wireguard.com/install/).
* Cliquez sur **Download Windows Installer**.
* Installez le logiciel.

2. **Importer le fichier :**
* Ouvrez WireGuard.
* Cliquez sur le bouton **"Import tunnel(s) from file"** en bas à gauche (ou faites `Ctrl + O`).
* Sélectionnez votre fichier `.conf`.

3. **Se connecter :**
* Cliquez sur le bouton **Activate**.
* Vérifiez que l'état passe à "Active".