---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: Utilisez le filtre Flou de couleur MLV pour appliquer des effets de flou directionnel aux textures de couleurs afin d’obtenir un aspect visuel dynamique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---


# Couleur MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Couleur MLV : icon](mlv-color.resources/MLV_Color_Icon.png "Couleur MLV : icon")

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
> Voir aussi [Niveaux de gris MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Couleur</i> | Image couleur à traiter. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Image couleur filtrée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> *Flottant* | Force du filtrage appliqué à l’image.<br><br>Des valeurs plus élevées lissent les détails et accentuent le bruit des zones plus plates. |
| <b>Smoothness</b> *Flottant* | Intensité du lissage appliqué aux zones de structuration, ce qui produit des zones plus arrondies et réduit l’effet de pas qui peut se produire à des intensités de filtrage plus élevées. |
| <b>Critère</b> *Entier* | Critère utilisé pour sélectionner les valeurs qui définiront les zones de structuration de l’image.<br><br>En d&#39;autres termes, comment les pixels doivent être *regroupés* en zones qui doivent être lissées.<br><br>*- Variance :* Sélectionnez les valeurs avec la plus faible dispersion autour de la moyenne, ce qui entraîne des clusters de pixels similaires les uns aux autres <br>*- Coefficient de variation :* Sélectionnez des valeurs tout en tenant compte de la moyenne, ce qui entraîne inversement une moindre variation dans les zones plus lumineuses |
| <b>Gaussien</b> *Booléen* | Utilisez une distribution gaussienne pour regrouper les pixels dans des zones de structuration.<br><br>Lorsque la valeur est True, les zones sont plus lisses et l&#39;effet d&#39;aplatissement est réduit. |
| <b>Affecter alpha</b> *Booléen* | Lorsque la valeur est True, le filtrage est également appliqué sur le canal Alpha de l’image.<br><br>Lorsque la valeur est False, le canal Alpha est entièrement ignoré et laissé tel quel dans la sortie. |
| <b>Itérations</b> *Entier* | Nombre d’exécutions du filtre, chaque itération s’appliquant au résultat de la précédente.<br><br>Plus d&#39;itérations entraînent des zones de structuration plus plates et plus nettes. |

## Exemples

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>Après</i>
    </td>
  </tr>
</table>
