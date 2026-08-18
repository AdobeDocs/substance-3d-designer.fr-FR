---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Utilisez le nœud de filtre Courbure pour générer des cartes de courbure à partir de cartes d'height afin de détecter des surfaces convexes et concaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure (nœud de filtre)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---


# Courbure (nœud de filtre)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## Courbure

**Entrée :** *Filtres/Effets*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Effectue une conversion de courbure simple et stricte en une passe pour entrer [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). La texture obtenue présente des teintes blanches pour les zones convexes et noires pour les zones concaves. La courbure produit toujours des lignes fines en pixels et des transitions nettes.

Ce nœud est utile pour mettre rapidement en évidence ou obscurcir certains bords. Il est limité par rapport à [Courbure lisse](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (qui produit des résultats de meilleure qualité) et à [Courbure Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (qui offre plus d&#39;options).

## Paramètres

* **Intensité** : *0,0 - 10,0* Intensité de l&#39;effet. Augmente le contraste du résultat.
* **Format normal** : *DirectX, OpenGL*\
  Bascule entre différents formats de mappage normal (inverse la couche verte).

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
