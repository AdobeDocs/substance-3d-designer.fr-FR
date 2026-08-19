---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: Utilisez le nœud Interpolation vectorielle pour interpoler des textures entre deux entrées à l’aide de champs vectoriels pour des transitions fluides.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interpolation vectorielle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# Interpolation vectorielle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

## Interpolation vectorielle (niveaux de gris)

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Déforme une image d’entrée à l’aide d’une carte vectorielle. L’effet est similaire à la distorsion UV avec une carte normale ou à l’utilisation d’une carte de flux dans les nuanceurs de jeux vidéo. Les pixels d’entrée sont déplacés par les vecteurs définis dans les valeurs Rouge et Vert de la carte vectorielle.

Ce nœud en lui-même n&#39;est pas le plus difficile à utiliser, mais la création d&#39;une carte vectorielle appropriée prend soin. Nous vous recommandons de travailler avec les profondeurs binaires les plus élevées pour assurer la précision lors du morphing.

La déformation vectorielle est très similaire à la [déformation vectorielle](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md) : la principale différence est que ce nœud de morphing ne « boucle » pas ou ne « mosaïque » le résultat lorsqu’il est poussé en dehors des limites de la zone de travail. Au lieu de cela, il serre et répète les bords.

## Paramètres

### Entrées

* **Entrée** :*Entrée couleur/niveaux de gris* Entrée source qui doit être la cible de la déformation.
* **Champ vectoriel** : *Entrée de couleur* La carte vectorielle utilisée pour générer la déformation.

### Paramètres

* **Quantité** : *0,0 - 1,0* définit l’intensité de l’effet de déformation, fonctionne comme un multiplicateur pour la texture vectorielle.

## Exemples d’images

</td>
</tr>
</table>
