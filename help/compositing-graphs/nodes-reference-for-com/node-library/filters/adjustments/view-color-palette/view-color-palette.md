---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: Utilisez le nœud Afficher la palette de couleurs pour visualiser les données de palette de couleurs extraites des textures à des fins d’analyse.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Afficher la palette de couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# Afficher la palette de couleurs

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Quantifier la couleur](view-color-palette.resources/ViewColorPalette.png "Quantifier la couleur"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Rassemble une palette de couleurs dans un carré ou un rectangle pour la visualiser plus facilement dans la vue Graphique ou 2D.\
Le packing vise à laisser le moins de créneaux vides possible.

</td>
</tr>
</table>

L’ordre des couleurs dans la palette est conservé, avec des couleurs qui s’écoulent de gauche à droite et de haut en bas de la même manière que pour l’habillage de texte.

Ce nœud peut être utilisé pour visualiser les palettes produites par les nœuds suivants : [Quantifier la couleur](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Créer une palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modifier la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Palette</b> <i>Couleur</i> PRINCIPALE | Liste triée de couleurs RGB codées sous la forme d’une ligne de pixels. La palette peut contenir jusqu’à 256 couleurs.   Il s’agit de la palette que le nœud compresse et restitue. |
| <b>Quantité de couleur de la palette</b> <i>Nombre entier</i> | Quantité de couleurs stockées dans la palette.   Si ce nombre ne correspond pas à la quantité réelle de couleurs dans l&#39;entrée d&#39;image « Palette », la visualisation peut être incomplète ou avoir plus d&#39;emplacements vides que nécessaire. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Visualisation de la palette compactée. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Afficher la palette de couleurs : Exemple 1](view-color-palette.resources/view_color_palette_example_1.png "Afficher la palette de couleurs : Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Afficher la palette de couleurs : Exemple 2](view-color-palette.resources/view_color_palette_example_2.png "Afficher la palette de couleurs : Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Afficher la palette de couleurs : Exemple 3](view-color-palette.resources/view_color_palette_example_3.png "Afficher la palette de couleurs : Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Afficher la palette de couleurs : Exemple 4](view-color-palette.resources/view_color_palette_example_4.png "Afficher la palette de couleurs : Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
