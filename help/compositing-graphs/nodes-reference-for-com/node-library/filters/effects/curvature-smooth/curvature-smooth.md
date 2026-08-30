---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Utilisez le nœud Lissage de Courbure pour générer des maps curvatures lisses à partir de maps height pour l'extraction des détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lissage de courbure
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---


# Lissage de courbure

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud Arrondi de Courbure](curvature-smooth.resources/CurvatureSmooth.png "Icône de nœud Arrondi de Courbure"){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Calcule la courbure d&#39;une surface décrite par une map normal.

Une map curvature représente les zones concaves et convexes d&#39;une surface.\
Les zones plates sont grises à 50 %. Les zones convexes sont plus claires, tandis que les zones concaves sont plus sombres.

</td>
</tr>
</table>

Les zones concaves et convexes sont également divisées en leurs propres sorties, pour faciliter la sélection ou le masquage des zones en fonction de ces caractéristiques.

>[!TIP]
>
> Examinez la [Courbure](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) pour une version plus nette ou la[Courbure Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) si vous avez besoin d&#39;autres options.

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Normal</b> <i>Couleur</i> <b>PRINCIPAL</b> | Map normal décrivant la surface dont la courbure doit être calculée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Niveaux de gris</i> | Map curvature calculée à partir de la map normal d&#39;entrée.   Les zones plates sont grises à 50 %. Les zones convexes sont plus claires, tandis que les zones concaves sont plus sombres. |
| <b>Convexité</b> <i>Niveaux de gris</i> | La carte de convexité calculée à partir de la map normal d&#39;entrée.   Plus une zone est convexe, plus elle est lumineuse sur la carte.  Les zones plates ou concaves sont noires. |
| <b>Concavité</b> <i>Niveaux de gris</i> | Carte de concavité calculée à partir de la carte normale d&#39;entrée.   Plus une zone est concave, plus elle est lumineuse sur la carte.  Les zones plates ou convexes sont noires. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Format normal</b> *Nombre entier* | Format du mappage normal en entrée. Inverse efficacement la couche verte.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX :</b> l&#39;axe Y pointe vers le haut</li> <li data-preserve-html="true"><b style="">OpenGL :</b> l’axe Y pointe vers le bas</li> </ul> |

## Exemples

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_before.jpg" alt="curvature_blend_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_after.jpg" alt="curvature_blend_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 2](curvature-smooth.resources/curvature_smooth_example_2.jpg "Lissage de courbure : Exemple 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 3](curvature-smooth.resources/curvature_smooth_example_3.jpg "Lissage de courbure : Exemple 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_before.jpg" alt="curvature_blend_example_4_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_after.jpg" alt="curvature_blend_example_4_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 4](curvature-smooth.resources/curvature_smooth_example_5.jpg "Lissage de courbure : Exemple 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 5](curvature-smooth.resources/curvature_smooth_example_6.jpg "Lissage de courbure : Exemple 5"){zoomable="yes"}

</td>
</tr>
</table>
