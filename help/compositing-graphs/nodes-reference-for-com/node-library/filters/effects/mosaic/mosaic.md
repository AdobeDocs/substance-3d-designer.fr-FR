---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: Utilisez le nœud Mosaïque pour créer des effets de mosaïque en divisant les textures en blocs et motifs pixellisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# Mosaïque

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mosaic-1.png){width="128px"}

![](../../../../../../assets/mosaic-grayscale.png){width="128px"}

## Mosaïque (Niveaux de gris)

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

« Facétise » une courbe de transfert de dégradé existante, lisse et en pente en effectuant un effet [Déformation](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) multi-passes. Lorsqu&#39;une même texture est utilisée pour les deux entrées, elle grossit et accentue essentiellement les zones les plus claires.

Cette option est utile pour ajouter plus de définition aux cartes en niveaux de gris telles que Heightmap, car elle peut donner plus de définition aux formes.

## Paramètres

### Entrées

* **Couleur** :*Entrée Couleur/Niveaux De Gris*
* **Carte Mosaïque** : *Entrée En Niveaux De Gris*\
  Déformation de la carte de pilote. Peut être identique à la première entrée.

### Paramètres

* **Échantillons** : *0 - 16* Détermine la qualité multi-échantillon.
* **Intensité** : *0,0 - 1,0* Intensité de l&#39;effet.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mosaci-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
