---
layout: default
title: Astuces Mac
parent: Outils
nav_order: 13
---

# Astuces Mac
  
- **Afficher / masquer les fichiers cachés**
Cmd shift .
  
- **Afficher / masquer les fichiers cachés avec terminal**
defaults write com.apple.finder AppleShowAllFiles TRUE
defaults write com.apple.finder AppleShowAllFiles FALSE
  
- **clean "Others" storage**
[https://www.reddit.com/r/jailbreak/comments/gkn3yb/discussionguys_i_found_the_way_to_clean_your/?utm_source=share&utm_medium=ios_app&utm_name=iossmf](https://www.reddit.com/r/jailbreak/comments/gkn3yb/discussionguys_i_found_the_way_to_clean_your/?utm_source=share&utm_medium=ios_app&utm_name=iossmf)
  
- **Importer des signets**
[https://support.apple.com/fr-fr/guide/safari/ibrw1015/mac](https://support.apple.com/fr-fr/guide/safari/ibrw1015/mac)
  
- **Dock plus rapide** (Terminal)
`defaults write com.apple.dock autohide-delay -float 0`
`defaults write com.apple.dock autohide-time-modifier -float 0.4; killall Dock`
enlevé
`defaults delete com.apple.dock autohide-delay && killall Dock`
  
- **“app” is damaged and can’t be opened**
![[app is damaged.png|app is damaged.png]]
Open Terminal
For a certain application
`sudo xattr -rd com.apple.quarantine /Applications/appname.app`
Disable checks globally (dl from “Anywhere”)
`sudo spctl --master-disable`
Activate checks globally
`sudo spctl --master-enable`
  
- **Clavier custom**
[custom-keyboard](https://suragch.medium.com/how-to-make-a-custom-keyboard-for-mac-os-c9f607428372)
  
- **Recover Deleted Pictures From USB**
[https://youtu.be/XZbR0U9Ir9w](https://youtu.be/XZbR0U9Ir9w)
  
- **Disable SIP**
1. Restart your computer in [Recovery mode](https://support.apple.com/en-us/HT201314).
2. Launch Terminal from the Utilities menu.
3. Run the command `csrutil disable`.
4. Restart your computer.
**Enable SIP**
1. Restart your computer in [Recovery mode](https://support.apple.com/en-us/HT201314).
2. Launch Terminal from the Utilities menu.
3. Run the command `csrutil enable`.
4. Restart your computer.
  
- **Speedtest dans terminal**
`networkquality`
  
- **Afficher HUD Metal**
Activer HUD: `/bin/launchctl setenv MTL_HUD_ENABLED 1`
Désactiver HUD:  
`/bin/launchctl setenv MTL_HUD_ENABLED 0`
Toggle HUD: `ftion shift f9`
  
- **Clean ._ files**
    Open Terminal, `cd` _`directory`_  
    `find . -type f -name '._*'`  
    `find . -type f -name '._*' -delete`

- **TextEdit ouvre un document vierge**
```bash
defaults write -g NSShowAppCentricOpenPanelInsteadOfUntitledFile -bool false
defaults write com.apple.TextEdit NSShowAppCentricOpenPanelInsteadOfUntitledFile -bool false
```
Annuler
```bash
defaults delete com.apple.TextEdit NSShowAppCentricOpenPanelInsteadOfUntitledFile
defaults delete -g NSShowAppCentricOpenPanelInsteadOfUntitledFile
```

- **Utiliser f1 et f2 pour contrôler la luminosité du clavier**
1. Coller ceci dans un documents texte
```bash
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
		<key>Label</key>
		<string>com.local.KeyRemapping</string>
		<key>ProgramArguments</key>
		<array>
				<string>/usr/bin/hidutil</string>
				<string>property</string>
				<string>--set</string>
				<string>{"UserKeyMapping": [
						{
							"HIDKeyboardModifierMappingSrc": 0x70000003A, 									"HIDKeyboardModifierMappingDst": 0xFF00000009
						},
						{
							"HIDKeyboardModifierMappingSrc": 0x70000003B, 									"HIDKeyboardModifierMappingDst": 0xFF00000008
						}
				]}</string>
		</array>
		<key>RunAtLoad</key>
		<true/>
</dict>
</plist>
```
2. Renommer par `com.local.keyRemapping.plist`
3. Déplacer le fichier vers `~/Library/LaunchAgents`