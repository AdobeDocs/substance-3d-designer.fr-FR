---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: Utilisez le filtre Flou de couleur MLV pour appliquer des effets de flou de mouvement aux textures de couleur afin de créer des aspects visuels dynamiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# Couleur MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Couleur MLV : icon](../../../../../../assets/MLV_Color_Icon.png "Couleur MLV : icon")

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
> Voir aussi [Niveaux de gris MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md).

## Connecteurs d’entrée

<b>Entrez </b>*Couleur* l&#39;image couleur qui doit être traitée.

## Connecteurs de sortie

<b>Sortie</b> *Couleur* L’image couleur filtrée.

## Paramètres

<b>Intensité</b> *Flottant* L’intensité du filtrage appliqué à l’image.\
Plus la valeur est élevée, plus les détails et le bruit sont lissés dans les zones plus plates.

<b>Smoothness</b> *Flotter* L&#39;intensité du lissage appliqué aux zones de structuration, ce qui donne des zones plus arrondies et réduit l&#39;effet de pas qui peut se produire à des intensités de filtrage plus élevées.

<b>Critère</b> *Entier* Critère utilisé pour sélectionner les valeurs qui définiront les zones de structuration de l&#39;image.\
En d&#39;autres termes, comment les pixels doivent être *regroupés* en zones qui doivent être lissées.\
*- Variance :* sélectionnez les valeurs avec la dispersion la plus faible autour de la moyenne, ce qui donne des groupes de pixels similaires les uns aux autres\
*- Coefficient de variation :* sélectionnez les valeurs en tenant compte de la moyenne, ce qui entraîne inversement une variation moindre dans les zones plus lumineuses

<b>Gaussien</b> *Booléen* Utilisez une distribution gaussienne pour regrouper les pixels dans des zones de structuration.\
Lorsque la valeur est True, les zones sont plus lisses et l&#39;effet d&#39;aplatissement est réduit.

<b>Affecter alpha</b> *Booléen* Lorsque la valeur est True, le filtrage est également appliqué sur la couche alpha de l’image.\
Lorsque la valeur est False, la couche alpha est entièrement ignorée et laissée telle quelle dans la sortie.

<b>Itérations</b> *Entier* Nombre d&#39;exécutions du filtre, où chaque itération est appliquée au résultat de la précédente.\
Plus il y a d’itérations, plus les zones de structuration sont plates et nettes.

## Exemples

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>Après</i>
    </td>
  </tr>
</table>
