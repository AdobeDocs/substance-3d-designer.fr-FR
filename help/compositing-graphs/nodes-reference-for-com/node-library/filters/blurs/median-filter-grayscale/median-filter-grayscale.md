---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-grayscale.html"
breadcrumb-title: ''
description: Utilisez le nœud Niveaux de gris du filtre médian pour réduire le bruit et préserver les contours des textures en niveaux de gris.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtre médian en niveaux de gris
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---


# Filtre médian en niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Filtre médian en niveaux de gris : icône](../../../../../../assets/MedianFilter_Icon_Grayscale.png "Filtre médian en niveaux de gris : icône")

<b>Entrée :</b> Filtres > Flous

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce filtre lisse le bruit dans une image tout en préservant les contours.

Pour chaque pixel, le nœud calcule une valeur de niveaux de gris en fonction de la valeur médiane des voisins du pixel.

</td>
</tr>
</table>

>[!NOTE]
>
> Voir aussi [Couleur de filtre médiane](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-color/median-filter-color.md).

## Connecteurs d’entrée

<b>Saisir </b>*en niveaux de gris* l&#39;image en niveaux de gris à laquelle le filtre doit être appliqué.

## Connecteurs de sortie

<b>Sortie </b>*en niveaux de gris* Image en niveaux de gris calculée en appliquant le filtre à l’image en niveaux de gris d’entrée.

## Paramètres

<b>Taille du noyau</b> *Entier* Un noyau est un groupe spécifique de valeurs utilisées dans les calculs d&#39;un filtre. Dans ce contexte, ce sont les valeurs des pixels voisins.\
Pour chaque pixel, le filtre prend tous les voisins autour de ce pixel dans un noyau carré et calcule la valeur médiane de tous les voisins.\
Ce paramètre contrôle la taille de ce noyau carré, en pixels. Un noyau plus grand produit un effet de lissage plus intense et d’une plus grande portée au détriment d’un certain niveau de détail.\
*- 3x3:* un noyau de 3 pixels de large et 3 pixels de haut, totalisant 8 pixels voisins.\
*- 5x5:* un noyau de 5 pixels de large et 5 pixels de haut, totalisant 24 pixels voisins.

<b>Type de filtre</b> *Entier* Le calcul appliqué aux voisins échantillonnés dans le noyau.\
*- Médiane :* Utilisez directement la valeur médiane de tous les voisins.\
*- MLMAD:* Signifie « Médiane De L’Écart Absolu Le Moins Médian ». L&#39;écart tient compte de la différence d&#39;une valeur par rapport à la médiane. Au lieu d&#39;utiliser directement la valeur médiane qui peut être inclinée par un pixel aberrant avec un écart élevé, la méthode MLMAD utilise la médiane de tous les écarts. Cette méthode produit un effet de lissage plus intense qui peut aplatir les zones en fonction de la taille du noyau.

## Exemples

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant4A.png" alt="MedianFilter_Variant4A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant4B.png" alt="MedianFilter_Variant4B">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant1A.png" alt="MedianFilter_Variant1A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant1B.png" alt="MedianFilter_Variant1B">
      <br><i>Après</i>
    </td>
  </tr>
</table>
