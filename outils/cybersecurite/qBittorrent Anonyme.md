---
layout: default
title: qBittorrent Anonyme
parent: Cybersécurité
grand_parent: Outils
nav_order: 5
---

# Tuto qBittorrent + WireGuard (WARP) + Blocklist
### Prérequis

1. Client WireGuard :
    - [Télécharger pour Windows](https://download.wireguard.com/windows-client/wireguard-installer.exe)
    - [Télécharger pour macOS](https://apps.apple.com/us/app/wireguard/id1451685025?mt=12)
2. qBittorrent : [Télécharger ici](https://www.qbittorrent.org/download)

---

## Étape 1 : Générer le Tunnel VPN (wgcf)
### Pour Windows

1. Télécharger : Prenez le fichier `wgcf_2.2.xx_windows_amd64.exe` sur [cette page](https://github.com/ViRb3/wgcf/releases)
2. Préparer : Créez un dossier `C:\vpn`, mettez le fichier dedans et renommez-le en `wgcf.exe`
3. Commandes : Ouvrez l'invite de commande (`cmd`) et tapez :
```
cd C:\vpn
wgcf.exe register
```
(Tapez `yes` et Entrée)
```
wgcf.exe generate
```
Vous avez maintenant un fichier `wgcf-profile.conf`

### Pour macOS

1. Télécharger : Sur [cette page](https://github.com/ViRb3/wgcf/releases)
    - Mac ARM : `wgcf_2.2.xx_darwin_arm64`
    - Mac Intel : `wgcf_2.2.xx_darwin_amd64`
2. Préparer : Allez dans Téléchargements, renommez le fichier en **`wgcf`** (tout court)
3. Commandes : Ouvrez le Terminal et tapez :
```bash
cd ~/Downloads
chmod +x wgcf
./wgcf register
```
(⚠️ Si bloqué par la sécurité : Allez dans "Réglages Système" > "Confidentialité et sécurité" > "Ouvrir quand même", puis réessayez la commande). Tapez `yes`
```bash
./wgcf generate
```
Vous avez maintenant un fichier `wgcf-profile.conf`

---

## Étape 2 : Activer WireGuard

1. Ouvrez l'application WireGuard
2. Cliquez sur "Importer un tunnel depuis un fichier" (Import Tunnel from File).
3. Sélectionnez le fichier `wgcf-profile.conf` créé à l'étape 1.
4. Cliquez sur Activer (Activate). Le bouton devient vert.

---

## Étape 3 : Sécuriser qBittorrent (Kill Switch)

Cette étape oblige qBittorrent à passer par le VPN. Si le VPN plante, le téléchargement s'arrête net

1. Ouvrez qBittorrent
2. Allez dans Options (Windows) ou Préférences (Mac) > Onglet Avancé
3. Cherchez la ligne Interface réseau (Network Interface).
4. Sélectionnez l'interface du VPN :
    - Windows : Souvent nommée `wgcf-profile` ou `WireGuard Tunnel`
    - Mac : Souvent nommée `utun3`, `utun4`... (Cherchez celle avec une IP type `172.16...` ou `10...`)
5. Cliquez sur OK

---

## Étape 4 : Ajouter la Blocklist (Anti-Espions)

1. Télécharger : [Cliquez ici pour `bt_blocklists.gz`](https://github.com/Naunter/BT_BlockLists/raw/master/bt_blocklists.gz)
2. Préparer :
    - Décompressez le fichier (double-clic).
    - Renommez le fichier extrait en : **`bt_blocklists.p2p`**. (Important : l'extension `.p2p` est obligatoire pour que qBittorrent le voie).
3. Activer :
    - Dans qBittorrent : Options/Préférences > Onglet Connexion.
    - Cochez Filtrage IP (IP Filtering).
    - Cochez Appliquer aux traqueurs.
    - Cliquez sur l'icône dossier 📁 et sélectionnez votre fichier `bt_blocklists.p2p`.
    - Cliquez sur la flèche de rafraîchissement 🔄 (ou OK).

---

## Étape 5 : Vérification (Obligatoire)

1. Allez sur [ipleak.net](https://ipleak.net)
2. Section "Torrent Address detection" > Cliquez sur Activate
3. Ouvrez le lien Magnet dans qBittorrent
4. Vérifiez l'IP affichée sur le site 
    - Si c'est Cloudflare : Tout est bon
    - Si c'est Orange/Free/SFR/Bouygues : DANGER. Recommencez l'étape 3