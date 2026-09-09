---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: Utilisez le nœud de calcul d'histogramme pour calculer les données d'histogramme à partir de textures pour analyse et traitement.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Histogramme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# Histogramme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Calcul de l&#39;histogramme : icône](histogram-compute.resources/histogram_compute.png "Calcul de l&#39;histogramme : icône"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Calcule l’histogramme d’une image en niveaux de gris.

L&#39;histogramme est codé sous la forme d&#39;une ligne de pixels dans une image, où chaque valeur de pixel correspond à la *population* de la valeur de couleur correspondant à la position de pixel sur l&#39;axe X.\
Par exemple, une valeur de pixel de 75 at (0,25, 0) signifie que 75 pixels ont la valeur de couleur 0,25 dans l’image.

</td>
</tr>
</table>

Le nœud génère également la *fonction de distribution cumulative* (CDF) calculée pour l&#39;image.

Les outils personnalisés peuvent être créés à l&#39;aide des données calculées par le nœud, telles que les masques personnalisés, comme indiqué ci-dessous dans la section « Exemples ».

>[!IMPORTANT]
>
> Toutes les valeurs comprises dans la plage [0,1] sont verrouillées. Par conséquent, l’histogramme peut ne pas être précis pour les images HDR.

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Niveaux de gris</i> PRINCIPAUX | Image pour laquelle l’histogramme doit être calculé. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Histogramme</b> <i>Niveaux de gris</i> | Histogramme calculé pour l&#39;image d&#39;entrée, codé sous la forme d&#39;une ligne de pixels où chaque valeur de pixel correspond à la *population* de la valeur de couleur correspondant à la position de pixel sur l&#39;axe X.   Par exemple, une valeur de pixel de 75 at (0,25, 0) signifie que 75 pixels ont la valeur de couleur 0,25 dans l’image. |
| <b>CDF</b> <i>Niveaux de gris</i> | Résultat de la *fonction de distribution cumulative* (CDF) calculée pour l&#39;image, codée en une ligne de pixels où chaque pixel est la somme de toutes les valeurs de pixels à sa gauche.   Cette somme est ensuite *normalisée* par rapport au nombre total de pixels dans l&#39;image. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Résolution de l&#39;histogramme</b> *Entier* | La largeur de l’histogramme. Une valeur élevée permet une distribution plus fine des valeurs.   Les résolutions disponibles sont, en pixels : 256, 512, 1024, 2048, 4096 |

## Exemples

![Calcul de l&#39;histogramme : Exemple 1](histogram-compute.resources/histogram_compute_example_1.jpg "Calcul de l&#39;histogramme : Exemple 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>
