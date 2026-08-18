---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Utilisez le nœud Normal à Height pour convertir les cartes de normales en cartes d'height afin d'extraire les informations de profondeur de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal à l’Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Normal à l’Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## Normal à l’Height

**Entrée :** *Filtres/Mappage de normales*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud de conversion inverse qui tente de reconvertir une carte normale d&#39;espace tangent en carte de hauteur. Il s&#39;agit de la version légèrement plus simple ; [Normal à l&#39;Height HQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) dispose de plus d&#39;options.

Utile lorsque vous n&#39;avez qu&#39;une source Normalmap, mais que vous souhaitez néanmoins effectuer des opérations la combinant avec une carte de hauteur. Gardez à l’esprit que cela ne permettra jamais d’obtenir un résultat correct à 100 %, car les informations sont perdues par nature lors de la conversion de l’Height en normalité. Si vous réglez les paramètres en conséquence, cette version hors siège réussit correctement à convertir les détails simples.

## Paramètres

* **Balance des Reliefs** :*0,0 - 1,0* ajustez la mesure dans laquelle les différentes fréquences influencent le résultat final. Cela dépend en grande partie du mappage d&#39;entrée et nécessite un peu de réglages.
* **Format normal** : *DirectX, OpenGL*\
  Bascule entre différents formats de mappage normal (inverse la couche verte).
* **Opacité globale** : *0.0 - 1.0* Ajuste l’opacité globale de l’effet.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
