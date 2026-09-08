---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: Utilisez le filtre Flou en niveaux de gris MLV pour appliquer des effets de flou directionnel aux textures en niveaux de gris afin de créer des aspects dynamiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Niveaux de gris MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# Niveaux de gris MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Niveaux de gris MLV : icon](../../../../../../assets/MLV_Grayscale_Icon.png "Niveaux de gris MLV : icon")

<b>Entrée :</b> Filtres > Flous

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

MLV signifie <b>&#39;Moyenne de moindre écart&#39;</b>. Ce filtre améliore les contours et lisse le bruit d’une image.

Le filtre recherche les zones structurantes d’une image et les utilise pour la rendre plus nette et l’aplatir. Dans certains cas, cela peut entraîner des marches le long de dégradés plus larges que les zones de structuration.

</td>
</tr>
</table>

>[!NOTE]
>
> Voir aussi [Couleur MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Niveaux de gris</i> | Image en niveaux de gris à traiter. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Image en niveaux de gris filtrée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> *Flottant* | Force du filtrage appliqué à l’image.<br><br>Des valeurs plus élevées lissent les détails et accentuent le bruit des zones plus plates. |
| <b>Smoothness</b> *Flottant* | Intensité du lissage appliqué aux zones de structuration, ce qui produit des zones plus arrondies et réduit l’effet de pas qui peut se produire à des intensités de filtrage plus élevées. |
| <b>Critère</b> *Entier* | Critère utilisé pour sélectionner les valeurs qui définiront les zones de structuration de l’image.<br><br>En d&#39;autres termes, comment les pixels doivent être *regroupés* en zones qui doivent être lissées.<br><br>*- Variance :* Sélectionnez les valeurs avec la plus faible dispersion autour de la moyenne, ce qui entraîne des clusters de pixels similaires les uns aux autres <br>*- Coefficient de variation :* Sélectionnez des valeurs tout en tenant compte de la moyenne, ce qui entraîne inversement une moindre variation dans les zones plus lumineuses |
| <b>Gaussien</b> *Booléen* | Utilisez une distribution gaussienne pour regrouper les pixels dans des zones de structuration.<br><br>Lorsque la valeur est True, les zones sont plus lisses et l&#39;effet d&#39;aplatissement est réduit. |
| <b>Itérations</b> *Nombre entier* | Nombre d’exécutions du filtre, chaque itération s’appliquant au résultat de la précédente.<br><br>Plus d&#39;itérations entraînent des zones de structuration plus plates et plus nettes. |

## Exemples

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>Après</i>
    </td>
  </tr>
</table>
