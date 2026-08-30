---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: Utilisez le nœud Interpolation vectorielle pour interpoler les textures entre deux entrées à l’aide de champs vectoriels pour des transitions fluides.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interpolation vectorielle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# Interpolation vectorielle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-morph.resources/vector-morph-grayscale.png)![](vector-morph.resources/vector-morph.png)

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Déforme une image d&#39;entrée à l’aide d’une carte vectorielle. L’effet est similaire à l’distorsion avec une carte normale ou à l’utilisation d’une « carte de flux » dans les nuanceurs de jeux vidéo. Les pixels d’entrée sont déplacés par les vecteurs définis dans les valeurs Rouge et Vert de la carte vectorielle.

Ce nœud en lui-même n&#39;est pas le plus difficile à utiliser, mais la création d&#39;une carte vectorielle appropriée prend soin. Nous vous recommandons de travailler avec les profondeurs binaires les plus élevées pour assurer la précision lors du morphing.

La déformation vectorielle est très similaire à la [déformation vectorielle](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md) : la principale différence est que ce nœud de morphing ne « boucle » pas ou ne « mosaïque » le résultat lorsqu’il est poussé en dehors des limites de la zone de travail. Au lieu de cela, il serre et répète les bords.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Entrée Couleur/Niveaux De Gris</i> | Entrée source qui doit être la cible de la déformation. |
| <b>Champ vectoriel</b> <i>Entrée couleur</i> | La carte vectorielle utilisée pour gérer la déformation. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité</b> <i>0.0 - 1.0</i> | Définit l’intensité de l’effet de déformation et fonctionne comme un multiplicateur pour la texture vectorielle. |
