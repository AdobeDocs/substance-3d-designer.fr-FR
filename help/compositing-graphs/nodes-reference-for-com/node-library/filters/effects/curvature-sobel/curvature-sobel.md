---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Utilisez le nœud Sobel de courbure pour détecter les arêtes de courbure à l’aide des opérateurs Sobel pour créer des masques de contour.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel courbé
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# Sobel courbé

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## Sobel courbé

**Entrée :** *Filtres/Effets*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Effectue une conversion de courbure simple et stricte en une passe pour entrer [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). La texture obtenue présente des teintes blanches pour les zones convexes et noires pour les zones concaves. La courbure produit toujours des lignes plus épaisses et des transitions nettes.

Ce nœud est utile pour mettre rapidement en évidence ou obscurcir certains bords. Elle est légèrement différente de la [courbure](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), car elle produit des résultats de meilleure qualité, mais reste nette et dure.

## Paramètres

* **Intensité** : *0,0 - 1,0* L&#39;intensité de l&#39;effet ajuste le contraste.
* **Type normal** : *DirectX, OpenGL*

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
