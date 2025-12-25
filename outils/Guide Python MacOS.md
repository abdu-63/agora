---
layout: default
title: Guide Python MacOS
parent: Outils
nav_order: 16
---

# Guide Python MacOS
`cd` /chemin_d’accès_au_dossier : Ouvrir un dossier dans le Terminal
`find . -name` nom_du_fichier
`pip3` : installer un paquet
`python3` : exécuter un script

## Environnement virtuel
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
Après avoir fini
```bash
deactivate
```