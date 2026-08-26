---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: Utilisez le filtre Flou en niveaux de gris MLV pour appliquer des effets de flou directionnel à des textures en niveaux de gris afin de créer des aspects dynamiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Niveaux de gris MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

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

MLV signifie <b>&#39;Moyenne de moindre écart&#39;</b>. Ce filtre améliore les contours et lisse le bruit dans une image.

Le filtre recherche les zones structurantes d’une image et les utilise pour la rendre plus nette et l’aplatir. Dans certains cas, cela peut entraîner des marches le long de dégradés plus larges que les zones de structuration.

</td>
</tr>
</table>

>[!NOTE]
>
> Voir aussi [Couleur MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md).

## Connecteurs d’entrée

<b>Entrez </b>*L&#39;image en niveaux de gris*&#x200B;à traiter.

## Connecteurs de sortie

<b>Sortie </b>*En niveaux de gris* L’image en niveaux de gris filtrée.

## Paramètres

<b>Intensité</b> *Flottant* L’intensité du filtrage appliqué à l’image.\
Plus la valeur est élevée, plus les détails et le bruit sont lissés dans les zones plus plates.

<b>Smoothness</b> *Variable* L’intensité du lissage appliqué aux zones de structuration, ce qui donne des zones plus arrondies et réduit l’effet de pas qui peut se produire à des intensités de filtrage plus élevées.

<b>Critère</b> *Entier* Critère utilisé pour sélectionner les valeurs qui définiront les zones de structuration de l&#39;image.\
En d&#39;autres termes, comment les pixels doivent être *regroupés* en zones qui doivent être lissées.\
*- Variance :* sélectionnez les valeurs avec la dispersion la plus faible autour de la moyenne, ce qui donne des groupes de pixels similaires les uns aux autres\
*- Coefficient de variation :* sélectionnez les valeurs en tenant compte de la moyenne, ce qui entraîne inversement une variation moindre dans les zones plus lumineuses

<b>Gaussien</b> *Booléen* Utilisez une distribution gaussienne pour regrouper les pixels dans des zones de structuration.\
Lorsque la valeur est True, les zones sont plus lisses et l&#39;effet d&#39;aplatissement est réduit.

<b>Itérations</b> *Entier* Nombre d&#39;exécutions du filtre, où chaque itération est appliquée au résultat de la précédente.\
Plus il y a d’itérations, plus les zones de structuration sont plates et nettes.

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
