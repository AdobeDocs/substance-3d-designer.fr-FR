---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: Utilisez le nœud Dissociation normale pour séparer les données de map normal en composants X, Y et Z individuels.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dissociation normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Dissociation normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de dissociation normale](normal-uncombine.resources/NormalUncombine.png "Icône de dissociation normale"){width="200px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Supprime d&#39;une map normal les détails de surface décrits par une map height.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Normal combiné</b> <i>Couleur</i> PRINCIPALE | Map normal dont les détails doivent être supprimés. |
| <b>Height</b> <i>Niveaux de gris</i> | Map height représentant les détails de la surface à supprimer de la map normal combinée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Normal non combiné</b> <i>Couleur</i> | Map normal dans laquelle les détails de surface décrits par la map height d&#39;entrée ont été supprimés. |
| <b>Intensité estimée</b> <i>Flottant</i> | Estimation de l&#39;intensité qui doit être définie sur un nœud [normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) relié à la map height d&#39;entrée, pour correspondre à l&#39;intensité de la map normal d&#39;entrée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Format normal</b> *Entier* | Format de la map normal d&#39;entrée. Inverse efficacement la couche verte.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX :</b> L&#39;axe Y pointe vers le haut</li> <li data-preserve-html="true"><b>OpenGL :</b> l&#39;axe Y pointe vers le bas</li> </ul> |

## Exemples

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 2](normal-uncombine.resources/normal_uncombine_example_4.png "Désassociation normale : Exemple 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 4](normal-uncombine.resources/normal_uncombine_example_6.png "Désassociation normale : Exemple 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 6](normal-uncombine.resources/normal_uncombine_example_5.png "Désassociation normale : Exemple 6"){zoomable="yes"}
