---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/apply-color-palette.html"
breadcrumb-title: ''
description: Utilisez le nœud Appliquer la palette de couleurs pour remapper des textures à l'aide d'une palette de couleurs pour des effets de couleur stylisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Apply Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Appliquer la palette de couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# Appliquer la palette de couleurs

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Quantifier la couleur](../../../../../../assets/ApplyColorPalette.png "Quantifier la couleur"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique les couleurs d’une palette ordonnée à une image à l’aide d’un mappage d’ID.

La distribution des couleurs s’effectue en faisant correspondre les index du mappage d’ID aux index des couleurs de la palette.

Par exemple, les #2 de couleur de la palette seront appliquées à tous les pixels de la carte d’identité avec une valeur d’ID de 2.

Ce nœud peut être utilisé en combinaison avec les nœuds suivants : [Quantifier la couleur](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Créer une palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modifier la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Afficher la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>ID</b> *Niveaux de gris* PRINCIPAUX | Mappage d’ID d’entrée utilisé pour répartir les couleurs dans la palette d’entrée.   Un mappage d’ID est une image où les pixels qui font partie d’un ensemble (par exemple, une forme) contiennent tous la même valeur d’identification unique. Dans ce cas, la valeur est un nombre entier.   Un mappage ID peut être produit à l&#39;aide d&#39;un nœud [Quantize Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md). |
| <b>Palette</b> *Couleur* | Liste triée de couleurs RGB codées sous la forme d’une ligne de pixels. La palette peut contenir jusqu’à 256 couleurs. Il s&#39;agit de la palette que le nœud mappe aux index du mappage d&#39;ID.   Les palettes peuvent être produites avec un nœud [Quantifier la couleur](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) et modifiées avec un nœud [Modifier la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md). |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Couleur* | Résultat du mappage des couleurs de la palette aux index du mappage d’ID. |

## Exemples

![Appliquer la palette de couleurs : Exemple 1](../../../../../../assets/apply_color_palette_example_2.png "Appliquer la palette de couleurs : Exemple 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_before.jpg" alt="apply_color_palette_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_1_after.jpg" alt="apply_color_palette_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Appliquer la palette de couleurs : exemple 3](../../../../../../assets/apply_color_palette_example_4.png "Appliquer la palette de couleurs : exemple 3"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_before.jpg" alt="apply_color_palette_example_3_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/apply_color_palette_example_3_after.jpg" alt="apply_color_palette_example_3_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>
