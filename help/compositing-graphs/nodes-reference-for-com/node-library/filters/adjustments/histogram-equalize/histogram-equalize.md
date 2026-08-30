---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: Utilisez le nœud Égaliser de l’histogramme pour redistribuer les intensités des pixels afin d’améliorer le contraste et la luminosité.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Histogramme égaliser
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# Histogramme égaliser

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Histogramme égaliser : icône](histogram-equalize.resources/histogram_equalize.png "Histogramme égaliser : icône"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Égalise l’histogramme d’une image en niveaux de gris, en ajustant efficacement les valeurs de niveaux de gris pour obtenir une distribution égale.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Niveaux de gris</i> PRINCIPAUX | Image pour laquelle l’histogramme doit être égalisé. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Image finale avec égalisation de l’histogramme appliquée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Résolution de l&#39;histogramme</b> *Nombre entier* | La largeur de l’histogramme. Une valeur élevée permet une distribution plus fine des valeurs.   Les résolutions disponibles sont, en pixels : 256, 512, 1024, 2048, 4096 |
| <b>Lissage de l&#39;histogramme</b> *Flotter* | L&#39;histogramme peut être lissé en redistribuant les valeurs de niveaux de gris dans l&#39;image pour égaliser la *différence* entre chaque valeur.   Ce paramètre ajuste l’intensité de ce lissage. |

## Exemples

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Histogramme égaliser : exemple 1](histogram-equalize.resources/histogram_equalize_example_3.png "Histogramme égaliser : exemple 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Histogramme égaliser : exemple 2](histogram-equalize.resources/histogram_equalize_example_5.png "Histogramme égaliser : exemple 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Histogramme égaliser : exemple 3](histogram-equalize.resources/histogram_equalize_example_6.png "Histogramme égaliser : exemple 3"){zoomable="yes"}
