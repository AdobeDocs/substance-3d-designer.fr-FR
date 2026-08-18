---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Utilisez le nœud Éclaboussure pour dispersion des formes entre les textures afin de créer des motifs aléatoires et des détails de texture organique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Éclaboussure

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## Éclaboussure (couleur)

**Entrée :** *Générateurs de textures**/Motifs*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Splatter est un générateur de motif destiné au placement aléatoire d&#39;une entrée de carte. Il dispose de nombreuses commandes pour le placement à motifs géométriques et est plus simple d&#39;utilisation que le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Cette dernière solution peut donner des résultats similaires, mais elle est beaucoup plus complexe.

Splatter fonctionne bien pour tamponner rapidement certaines formes, sans avoir besoin de trop de retouches.

Gardez à l’esprit que les paramètres par défaut Éclaboussure ne semblent pas du tout aléatoires : vous devez en régler quelques-uns pour obtenir une randomisation (principalement les paramètres Trouble). Gardez également à l’esprit que Splatter nécessite une entrée de mappage pour fonctionner.

## Paramètres

* **Largeur de la taille du motif** : *0,0 - 1000,0* nombre de motifs à utiliser sur l’axe X.
* **Height de la taille du motif** : *0,0 - 1000,0* nombre de motifs à utiliser sur l’axe Y.
* **Rotation** : *-360.0 - 360.0* Fait pivoter chaque motif selon une valeur définie.
* **Variation de rotation** : *0.0 - 360.0* Introduit une rotation aléatoire pour chaque forme distincte.
* **Zoom** :*100.0 - 10000.0* Agrandit le résultat final. Gardez à l’esprit que cela casse le carrelage !
* **Gain** : *0.0 - 10.0* ajuste le gain de fusion de chaque motif. Les fait ressortir davantage.
* **Panoramique X** : *-100.0 - 100.0* Résultat du panoramique entier sur l&#39;axe X.
* **Panoramique Y** : *-100.0 - 100.0* Résultat du panoramique entier sur l’axe Y.
* **Trouble** : *0,0 - 100,0*\
  Décale les formes de manière aléatoire.
* **Numéro de grille** : *0 - 8* Parcourt différentes tailles de grille pour ajuster l’échelle des résultats. Conserve la mosaïque.
* **Angle du trouble** : *0,0 - 360,0* contrôle l&#39;angle du déplacement du trouble.
* **Désordre aléatoire** :*Faux/Vrai* aléatoire l&#39;angle du trouble, ajoutant beaucoup plus de chaos.
* **Taille du motif** : *5 - 12*
* **Variation de taille** : *0.0 - 100.0* Introduit la mise à l’échelle aléatoire pour chaque forme.
* **Filtrage d&#39;entrée d&#39;image (moteur > v4 uniquement)** : *Bilinéaire + Mipmaps, Bilinéaire, Au plus proche* Filtrage à appliquer à l&#39;image d&#39;entrée.
* **Niveau de sortie minimal** : *0,0 - 1,0* réglage du niveau de sortie minimum.
* **Niveau de sortie max** : *0,0 - 1,0* Réglage du niveau maximal de sortie.
* **Couleur d&#39;arrière-plan** : *(valeur Niveaux de gris)*Définit une couleur d&#39;arrière-plan unie.
* **Variation de luminance** : *0,0 - 1,0 (version en niveaux de gris uniquement)*Introduit la variation de luminance.
* **Variation de couleur** : *0.0 - 1.0 (version couleur uniquement)*Introduit la variation de couleur.

## Exemples d’images

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>
