---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Utilisez le nœud Créer une mosaïque pour corriger et créer des textures de mosaïque homogènes à partir des images d’entrée.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Créer un correctif de mosaïque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Créer un correctif de mosaïque

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-patch.png)

![](../../../../../../assets/make-it-tile-patch-grayscale.png)

## Créer un patch de mosaïque (niveaux de gris)

**Entrée :** *Filtres/Limites*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud est un carreau semi-aléatoire basé sur une grille. Il prend un correctif d’entrée et le tamponne, en essayant de le transformer en une image de mosaïque sans trop de répétitions, en fonction de vos paramètres.

Utile lorsque vous avez une petite tache de texture et que vous souhaitez créer une texture mosaïque à plus grande échelle à partir de celle-ci.

Gardez à l&#39;esprit qu&#39;il s&#39;agit d&#39;une différence par rapport à la [photo Make-It-Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), qui corrige principalement les contours.

Pour ce faire avec un matériau entier, voir [Mosaïque automatique intelligente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

## Paramètres

* **Taille du masque** :*0.0 - 1.0* Taille du masque rond utilisé lors de l’estampage du correctif.
* **Précision du masque** : *précision de retrait/smoothness du masque de 0,0 à 1,0*.
* **Déformation du masque** : *-100.0 - 100.0* Introduit la déformation aux bords du masque. Cette option permet d’éviter les transitions lisses et non définies entre les patchs.
* **Largeur de la taille du motif** : *0.0 - 1000.0* Modifie la largeur du correctif de manière non uniforme.
* **height de la taille du motif** : *0.0 - 1000.0* modifie l’height du correctif de manière non uniforme.
* **Trouble** : *0,0 - 1,0*\
  Introduit un effet aléatoire de translation, en déplaçant légèrement les correctifs.
* **Variation de taille** : *0.0 - 100.0* introduit la variation de taille pour le masque.
* **Octave** : *0 - 6* Il s’agit du contrôle principal qui détermine la taille globale.
* **Rotation** : *-360.0 - 360.0* Fait pivoter au préalable le correctif.
* **Variation de rotation** : *0.0 - 360.0* Introduit une rotation aléatoire pour chaque tampon de correctif.
* **Couleur d&#39;arrière-plan** : *(Valeur de couleur)*Définit la couleur d&#39;arrière-plan pour les zones où aucun correctif n&#39;apparaît.
* **Variation de couleur** : *0,0 - 1,0 (version couleur uniquement)*Introduit une variation de couleur par correctif.
* **Variation de luminosité** *(version en niveaux de gris uniquement)*Introduit une variation de luminosité par correctif.

## Exemples d’images

![](../../../../../../assets/patch-ex.gif)

</td>
</tr>
</table>
