---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: Utilisez le nœud de filtre Ombres pour générer des effets d’ombre à partir des textures d’entrée afin d’ajouter de la profondeur et du réalisme aux matières.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tons foncés (nœud de filtre)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 2%

---


# Tons foncés (nœud de filtre)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shadows-1.png){width="128px"}

## Ombres

**Entrée :** *Filtres/Effets*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Version brute en niveaux de gris uniquement du nœud [Shape Drop Shadow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md). Il prend uniquement une forme binaire en noir et blanc comme entrée et renvoie uniquement l’ombre.

Peut être utile si vous êtes juste après l&#39;ombre et que vous ne souhaitez pas travailler avec un nœud plus complet, par exemple lors de la construction de votre propre matériau ou éclairage cuit.

## Paramètres

* **Distance de l&#39;ombre** : *0,0 - 1,0* contrôle la distance à laquelle l&#39;ombre doit tomber.
* **Angle de la lumière** : *0,0 - 1,0* contrôle l&#39;angle d&#39;incidence de la lumière.
* **Lissage des contours** :*0.0 - 1.0* détermine la dureté ou le flou des contours des ombres.
* **Échantillons** : *1 - 16* définit la qualité du paramètre Lissage des contours.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shadow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
