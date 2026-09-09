---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Utilisez le nœud Make It Tile Patch pour appliquer des correctifs et créer des textures de répétition homogènes à partir d'images d'entrée.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Créer un correctif de mosaïque
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# Créer un correctif de mosaïque

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch.png)

![](make-it-tile-patch.resources/make-it-tile-patch-grayscale.png)

<b>Entrée :</b> Filtres > Répétition

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud est un carreau semi-aléatoire basé sur une grille. Il prend un correctif d’entrée et le tamponne, en essayant de le transformer en image de répétition sans trop de répétitions, en fonction de vos paramètres.

Utile lorsque vous avez une petite zone de texture et que vous souhaitez en créer une plus grande échelle, la texture de répétition.

Gardez à l&#39;esprit qu&#39;il s&#39;agit d&#39;une différence par rapport à la [photo Make-It-Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), qui corrige principalement les contours.

Pour ce faire avec un matériau entier, voir [Mosaïque automatique intelligente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Taille du masque</b> <i>0.0 - 1.0</i> | Taille du masque rond utilisé lors de l’estampage du patch. |
| <b>Précision du masque</b> <i>0.0 - 1.0</i> | Précision de retrait/smoothness du masque. |
| <b>Déformation du masque</b> <i>-100.0 - 100.0</i> | Introduit la déformation sur les bords du masque. Cette option permet d’éviter les transitions lisses et non définies entre les patchs. |
| <b>Largeur de la taille du motif</b> <i>0.0 - 1000.0</i> | Modifie la largeur du correctif de manière non uniforme. |
| <b>height de la taille du motif</b> <i>0.0 - 1000.0</i> | Modifie l’height du correctif de manière non uniforme. |
| <b>Désordre</b> <i>0.0 - 1.0</i> | Introduit un effet aléatoire de translation, en déplaçant légèrement les correctifs. |
| <b>Variation de taille</b> <i>0.0 - 100.0</i> | Introduit une variation de taille pour le masque. |
| <b>Octave</b> <i>0 - 6</i> | Il s’agit du contrôle principal qui détermine la taille globale. |
| <b>Rotation</b> <i>-360.0 - 360.0</i> | Fait pivoter au préalable le patch. |
| <b>Variation de rotation</b> <i>0.0 - 360.0</i> | Introduit une rotation aléatoire pour chaque tampon de correctif. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Définit la couleur d’arrière-plan des zones où aucune pièce n’apparaît. |
| <b>Variation de couleur</b> <i>0.0 - 1.0 (Version En Couleur Uniquement)</i> | Introduit une variation de couleur par correctif. |
| <b>Variation de luminosité</b> <i>(version en niveaux de gris uniquement)</i> | Introduit une variation de luminosité par correctif. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/patch-ex.gif" />
        </td>
    </tr>
</table>
