---
layout: default
title: TP 1.5 Boris Johnson
parent: TP
grand_parent: Apprendre
nav_order: 4
---

# TP 1.5 Boris Johnson (Chronolocalisation)

**Objectif :** Déterminer l'heure exacte de la photo prise au 10 Downing Street en utilisant la trigonométrie et Google Earth Pro.

<img src="../../assets/images/tp_1.5_boris_johnson.png" width="200px">

### Données de base

- **Lieu :** 10 Downing Street (`51° 30′ 12″ N, 0° 07′ 40″ O`)1.
- **Date :** 8 mai 20202.
- **Sujet :** Boris Johnson (Taille estimée : $a = 1.75\text{m}$)3.

### Détail de l'Analyse Trigonométrique avec Google Earth Pro

Pour trouver l'heure, nous avons besoin de l'élévation du soleil. La formule est un triangle rectangle formé par l'objet et son ombre.

#### 1. Le principe mathématique

- **$a$ (Opposé)** = Hauteur de Boris Johnson ($1.75\text{m}$).
- **$b$ (Adiacent)** = Longueur de l'ombre au sol (Inconnue sur la photo 2D).
- **$\alpha$ (Angle)** = Élévation du soleil.
- **Formule :** $\tan(\alpha) = \frac{a}{b}$ donc $\alpha = \arctan(\frac{a}{b})$.

#### 2. Utilisation de Google Earth Pro (Mesure de $b$)

Puisque nous ne pouvons pas mesurer l'ombre en mètres sur une photo JPG, nous utilisons Google Earth Pro pour mettre l'image à l'échelle.

1. **Ouvrir Google Earth Pro** et aller au `10 Downing Street`.
2. **Repérer des points fixes :** Identifiez deux points visibles sur la photo originale et sur la vue satellite (ex: la distance entre deux barrières ou la largeur du trottoir).
3. **Outil Règle :** Mesurez cette distance de référence en mètres sur Google Earth (disons que la distance entre les barrières est de $X$ mètres).
4. **Produit en croix (Règle de trois) :**
    - Si sur l'image, l'écart entre les barrières fait $Y$ pixels et l'ombre fait $Z$ pixels.
    - Alors la taille réelle de l'ombre $b = (Z \times X) / Y$.
5. **Alternative (Direction) :**
    - Utilisez l'outil **Règle/Ligne** pour tracer une ligne qui suit l'angle de l'ombre projetée sur le sol (en se fiant aux repères au sol).
    - Relevez l'**Azimut** (l'angle par rapport au Nord) indiqué par l'outil règle.

#### 3. Résolution avec SunCalc

1. Reportez les coordonnées et la date sur SunCalc.
2. Cherchez l'heure où l'ombre s'aligne avec votre Azimut ou lorsque l'altitude du soleil correspond à votre calcul d'angle $\alpha$.
3. **Résultat :** L'heure estimée est **9h00 ou 9h30**.