---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: Utilisez le nœud Dissociation normale pour séparer les données de mappage normales combinées en composants X, Y et Z individuels.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dissociation normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Dissociation normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de dissociation normale](normal-uncombine.resources/normal-uncombine-01.png "Icône de dissociation normale"){width="200px"}

<b>Entrée :</b> Filtres > Mappage normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Supprime d&#39;une carte de normales les détails de surface décrits par une carte d&#39;height.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Normal combiné</b> <i>Couleur</i> PRINCIPALE | Mappage normal dans lequel les détails doivent être supprimés. |
| <b>Height</b> <i>Niveaux de gris</i> | La carte d&#39;height représentant les détails de surface qui doivent être supprimés de la carte de normales. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Normal non combiné</b> <i>Couleur</i> | La carte de normales où les détails de surface décrits par la carte d&#39;height d&#39;entrée ont été supprimés. |
| <b>Intensité estimée</b> <i>Flotter</i> | Estimation de l&#39;intensité qui doit être définie sur un nœud [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) relié à la carte d&#39;height d&#39;entrée, pour correspondre à l&#39;intensité de la carte de normale d&#39;entrée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Format normal</b> *Nombre entier* | Format du mappage normal en entrée. Inverse efficacement la couche verte.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX :</b> l&#39;axe Y pointe vers le haut</li> <li data-preserve-html="true"><b>OpenGL :</b> l’axe Y pointe vers le bas</li> </ul> |

## Exemples

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-02.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-03.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 2](normal-uncombine.resources/normal-uncombine-04.png "Désassociation normale : Exemple 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-05.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-06.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 4](normal-uncombine.resources/normal-uncombine-07.png "Désassociation normale : Exemple 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-08.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-09.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 6](normal-uncombine.resources/normal-uncombine-10.png "Désassociation normale : Exemple 6"){zoomable="yes"}
