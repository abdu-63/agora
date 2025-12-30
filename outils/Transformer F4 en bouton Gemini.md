---
layout: default
title: Transformer F4 en bouton Gemini
parent: Outils
nav_order: 17
---

# Transformer F4 en bouton Gemini
### Prérequis

1. Firefox installé.
2. Karabiner-Elements installé et configuré (avec les permissions accordées).
3. L'application native Raccourcis (Shortcuts) de macOS.

---

### 1. Créer l'action dans Raccourcis

1. Ouvrez l'application Raccourcis sur votre Mac.
2. Cliquez sur le + (en haut à droite) pour créer un nouveau raccourci.
3. Dans la barre de recherche à droite, cherchez "*Exécuter un script shell*" et ajoutez-le.
4. Dans la zone de texte du script, collez cette commande :
```bash
open -a "Firefox" "https://gemini.google.com"
```
1. Nommez votre raccourci (par ex: Gemini F4) en haut à gauche.
2. Laissez cette fenêtre ouverte pour l'instant.

---

### 2. Préparer la règle "Code Secret" pour Karabiner

Nous allons dire à la touche F4 d'envoyer une combinaison de touches complexe et invisible (`Cmd` + `Option` + `Ctrl` + `P`) pour éviter tout conflit avec le système.

1. Ouvrez l'application TextEdit.
2. Important : Allez dans le menu Format > Convertir au format texte (pour avoir du texte brut).
3. Copiez et collez le code JSON suivant :
```json
{
  "title": "Gemini F4 Ultime",
  "rules": [
    {
      "description": "F4 vers Code Secret (Cmd+Ctrl+Opt+P)",
      "manipulators": [
        {
          "type": "basic",
          "from": {
            "key_code": "f4",
            "modifiers": {
              "optional": ["any"]
            }
          },
          "to": [
            {
              "key_code": "p",
              "modifiers": ["right_command", "right_control", "right_option"]
            }
          ]
        }
      ]
    }
  ]
}
```
4. Enregistrez le fichier sous le nom : `gemini.json`.

---

### 3. Installer la règle dans Karabiner

4. Ouvrez une fenêtre Finder.
5. Faites la combinaison `Maj + Cmd + G` (ou menu Aller > Aller au dossier).
6. Collez ce chemin :
    `~/.config/karabiner/assets/complex_modifications`
7. Glissez votre fichier `gemini.json` dans ce dossier.
8. Ouvrez Karabiner-Elements et allez dans l'onglet *Complex Modifications*.
9. Cliquez sur *Add predefined rule*.
10. Trouvez la ligne "Gemini F4 Ultime" et cliquez sur *Enable*.

---

### 4. Lier le tout

1. Retournez dans votre raccourci Gemini F4 (créé à l'étape 1).
2. Dans la barre latérale droite (cliquez sur le petit "*i*" si elle est masquée), cliquez sur le champ Ajouter un raccourci clavier.
3. Appuyez physiquement sur votre touche F4.
4. Au lieu de voir F4, vous devriez voir apparaître les symboles : **`⌘⌥⌃P`**.

C'est terminé ! Vous pouvez fermer l'app Raccourcis.
