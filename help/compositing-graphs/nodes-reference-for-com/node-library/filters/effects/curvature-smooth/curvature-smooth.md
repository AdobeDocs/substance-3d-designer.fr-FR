---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Utilisez le nœud Lissage de courbure pour générer des cartes de courbure lisses à partir de cartes d'height pour l'extraction des détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lissage de courbure
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Lissage de courbure

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud Arrondi de courbure](../../../../../../assets/CurvatureSmooth.png "Icône de nœud Arrondi de courbure"){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Calcule la courbure d&#39;une surface décrite par une texture normale.

Une courbe map représente les zones concaves et convexes d&#39;une surface.\
Les zones plates sont grises à 50 %. Les zones convexes sont plus claires, tandis que les zones concaves sont plus sombres.

</td>
</tr>
</table>

Les zones concaves et convexes sont également divisées en leurs propres sorties, pour faciliter la sélection ou le masquage des zones en fonction de ces caractéristiques.

>[!TIP]
>
> Pour une version plus nette, consultez la section [Courbure](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) ou[Courbure Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) si vous avez besoin d&#39;autres options.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Paramètres

</td>
</tr>
</table>

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Normal</b> *Couleur* <b>PRIMAIRE</b> | Carte de normales décrivant la surface dont la courbure doit être calculée. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Courbure</b> *Niveaux de gris* | Courbure map calculée à partir de la courbe normale map d&#39;entrée.   Les zones plates sont grises à 50 %. Les zones convexes sont plus claires, tandis que les zones concaves sont plus sombres. |
| <b>Convexité</b> *Niveaux de gris* | La carte de convexité est calculée à partir de la carte normale d&#39;entrée.   Plus une zone est convexe, plus elle est lumineuse sur la carte.  Les zones plates ou concaves sont noires. |
| <b>Concavité</b> *Niveaux de gris* | Carte de concavité calculée à partir de la carte normale d&#39;entrée.   Plus une zone est concave, plus elle est lumineuse sur la carte.  Les zones plates ou convexes sont noires. |

## Paramètres

|  |  |
| --- | --- |
| <b>Format normal</b> *Nombre entier* | Format du mappage normal en entrée. Inverse efficacement la couche verte.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX :</b> l&#39;axe Y pointe vers le haut</li> <li data-preserve-html="true"><b style="">OpenGL :</b> l’axe Y pointe vers le bas</li> </ul> |

## Exemples

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_before.jpg" alt="curvature_blend_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_after.jpg" alt="curvature_blend_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 2](../../../../../../assets/curvature_smooth_example_2.jpg "Lissage de courbure : Exemple 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 3](../../../../../../assets/curvature_smooth_example_3.jpg "Lissage de courbure : Exemple 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_before.jpg" alt="curvature_blend_example_4_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_after.jpg" alt="curvature_blend_example_4_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 4](../../../../../../assets/curvature_smooth_example_5.jpg "Lissage de courbure : Exemple 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Lissage de courbure : Exemple 5](../../../../../../assets/curvature_smooth_example_6.jpg "Lissage de courbure : Exemple 5"){zoomable="yes"}

</td>
</tr>
</table>
