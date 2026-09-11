---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/create-color-palette-16.html"
breadcrumb-title: ''
description: Utilisez le nœud Créer une palette de couleurs pour extraire une palette de 16 couleurs des textures pour des effets stylisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Create Color Palette (16)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Créer une palette de couleurs (16)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Créer une palette de couleurs (16)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Quantifier la couleur](create-color-palette-16.resources/CreateColorPalette16.png "Quantifier la couleur"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Crée une liste ordonnée de couleurs et l’affiche sous forme de palette, avec un maximum de 16 couleurs.

Le nœud peut ajouter de nouvelles couleurs à une palette existante, à l’aide de l’ensemble d’entrées de palette.

Ce nœud peut être utilisé en combinaison avec les nœuds suivants : [Quantifier la couleur](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Appliquer la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Modifier la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Afficher la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Palette</b> <i>Couleur</i> PRINCIPALE | Liste triée de couleurs RGB codées sous la forme d’une ligne de pixels. La palette peut contenir jusqu’à 256 couleurs.   Cette entrée est facultative. Si elles sont utilisées, les couleurs définies par le nœud sont ajoutées à cette palette.   La palette peut être visualisée avec le nœud [Afficher la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md). |
| <b>Quantité de couleur de la palette</b> <i>Entier</i> | Quantité de couleurs stockées dans la palette.   Si ce nombre ne correspond pas à la quantité réelle de couleurs dans l&#39;entrée d&#39;image « Palette », la visualisation peut être incomplète ou avoir plus d&#39;emplacements vides que nécessaire. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Palette</b> <i>Couleur</i> | Palette mise à jour avec les couleurs spécifiées qui y sont ajoutées. |
| <b>Quantité de couleur de la palette</b> <i>Entier</i> | Quantité mise à jour de couleurs stockées dans la palette, avec la quantité spécifiée de couleurs ajoutées. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité de couleur</b> *Entier* | Quantité de couleurs à ajouter à la palette. |
| <b>Couleur #</b> *Flottant 3* *Autant de paramètres disponibles que la valeur « Quantité de couleur »* | Couleur à ajouter à la palette.   Les couleurs sont ajoutées à la palette dans le même ordre que cette liste numérotée. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Créer une palette de couleurs : Exemple 1](create-color-palette-16.resources/create_color_palette_example_1.png "Créer une palette de couleurs : Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Créer une palette de couleurs : Exemple 2](create-color-palette-16.resources/create_color_palette_example_2.png "Créer une palette de couleurs : Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

![Créer une palette de couleurs : Exemple 3](create-color-palette-16.resources/create_color_palette_example_3.png "Créer une palette de couleurs : Exemple 3"){zoomable="yes"}
