---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur du filtre médian pour réduire le bruit et conserver les contours dans les textures de couleur.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur de filtre médiane
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Couleur de filtre médiane

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Couleur médiane du filtre : icon](../../../../../../assets/MedianFilter_Icon_Color.png "Couleur médiane du filtre : icon")

<b>Entrée :</b> Filtres > Flous

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce filtre lisse le bruit d’une image tout en préservant les contours.

Pour chaque pixel, le nœud calcule une valeur de couleur en fonction de la valeur médiane des voisins du pixel.

</td>
</tr>
</table>

>[!NOTE]
>
> Voir aussi [Filtre médian en niveaux de gris](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Couleur</i> | Image couleur à laquelle le filtre doit être appliqué. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Image couleur calculée en appliquant le filtre à l’image couleur d’entrée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Taille du noyau</b> *Entier* | Un noyau est un groupe spécifique de valeurs utilisées dans les calculs d’un filtre. Dans ce contexte, ce sont les valeurs des pixels voisins.<br><br>Pour chaque pixel, le filtre prend tous les voisins autour de ce pixel dans un noyau carré et calcule la valeur médiane de tous les voisins.<br><br>Ce paramètre contrôle la taille de ce noyau carré, en pixels. Un noyau plus grand produit un effet de lissage plus fort et d&#39;une plus grande portée au prix d&#39;un certain niveau de détail.<br><br>*- 3x3:* un noyau de 3 pixels de large et 3 pixels de haut, totalisant 8 pixels voisins.<br>*- 5x5:* un noyau de 5 pixels de large et 5 pixels de haut, totalisant 24 pixels voisins. |
| <b>Type de filtre</b> *Entier* | Calcul appliqué aux voisins échantillonnés dans le noyau.<br><br>*- Médiane :* Utilisez directement la valeur médiane de tous les voisins.<br>*- MLMAD :* signifie &#39;Médiane de l&#39;écart absolu le moins médian&#39;. L&#39;écart tient compte de la différence d&#39;une valeur par rapport à la médiane. Au lieu d&#39;utiliser directement la valeur médiane qui peut être inclinée par un pixel aberrant avec un écart élevé, la méthode MLMAD utilise la médiane de tous les écarts. Cette méthode produit un effet de lissage plus intense qui peut aplatir les zones en fonction de la taille du noyau. |
| <b>Affecter alpha</b> *Booléen* | Détermine si le filtre doit être appliqué au canal Alpha de l’image. Lorsque *True*, le canal Alpha est inchangé. |

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
      <img src="../../../../../../assets/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>Après</i>
    </td>
  </tr>
</table>
