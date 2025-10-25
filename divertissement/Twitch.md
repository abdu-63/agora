---
layout: default
title: Twitch
parent: Divertissement
nav_order: 8
---

# Contourner les pubs Twitch
### Extension TwitchNoSub
1. Télécharger la dernière version de TwitchNoSub
2. Dézipper le fichier
3. Aller sur l’onglet extension chrome://extensions/
4. Activer le mode développeur dans l’onglet extension (en haut a droite)
5. Empaqueter l'extension et choisir le dossier associé (voir l'image)
![Empaqueter](Empaqueter_lextension.png)
6. Envoyé le fichier .crx crée dans l’onglet extension

### Script (uBlock Origin)
1. Installer l'extension uBlock Origin
2. Naviguez vers les paramètres de uBlock Origin
3. Sous l’onglet `Mes filtres`, ajoutez `twitch.tv##+js(twitch-videoad)`
4. Sous l’onglet `Paramètres`, activer `Je suis un utilisateur avancé`, puis cliquez sur l'engrenage qui apparaît
5. En bas de la page modifier la valeur de `userResourcesLocation`remplacer`unset` avec cette url `https://raw.githubusercontent.com/pixeltris/TwitchAdSolutions/master/video-swap-new/video-swap-new-ublock-origin.js`
6. Appliquer ensuite en haut à gauche


**Script (Tapermonkey)**
1. Installer l'extension Tapermonkey ([Firefox](https://addons.mozilla.org/fr/firefox/addon/tampermonkey/), [Chrome](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo))
2. Installer [ce script](https://github.com/pixeltris/TwitchAdSolutions/raw/master/video-swap-new/video-swap-new.user.js)