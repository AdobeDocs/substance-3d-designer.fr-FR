---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Utilisez le nœud Flood Fill sur taille de boîte pour remplir des zones avec des valeurs de taille de cadre de sélection pour des effets de mise à l’échelle procédurale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill à la taille de la boîte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Flood Fill à la taille de la boîte

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-bbox-size.png){width="128px"}

## Flood Fill à la taille de la boîte

**Entrée :** *Filtres/Effets*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un mappage en niveaux de gris à partir d&#39;un [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md), avec des valeurs liées à la taille individuelle de chaque vignette.

Les valeurs sont calculées par rapport à la taille totale de la zone de travail (un carreau blanc intégral étire toute la zone de travail). Le contraste est donc souvent faible.

## Paramètres

* **Sortie** : *max(X, Y), X, Y* Définit la mesure sur laquelle la valeur est basée : la largeur, la longueur ou les deux.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodbbox-ex1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
