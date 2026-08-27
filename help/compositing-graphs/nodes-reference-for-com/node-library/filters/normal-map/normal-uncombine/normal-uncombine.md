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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# Dissociation normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de dissociation normale](../../../../../../assets/NormalUncombine.png "Icône de dissociation normale"){width="200px"}

<b>Entrée :</b> Filtres > Mappage normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Supprime d&#39;une carte de normales les détails de surface décrits par une carte d&#39;height.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Paramètres

</td>
</tr>
</table>

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Normal combiné</b> *Couleur* PRINCIPALE | Mappage normal dans lequel les détails doivent être supprimés. |
| <b>Height</b> *Niveaux de gris* | La carte d&#39;height représentant les détails de surface qui doivent être supprimés de la carte de normales. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Normal non combiné</b> *Couleur* | La carte de normales où les détails de surface décrits par la carte d&#39;height d&#39;entrée ont été supprimés. |
| <b>Intensité estimée</b> *Flotter* | Estimation de l&#39;intensité qui doit être définie sur un nœud [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) relié à la carte d&#39;height d&#39;entrée, pour correspondre à l&#39;intensité de la carte de normale d&#39;entrée. |

## Paramètres

|  |  |
| --- | --- |
| <b>Format normal</b> *Nombre entier* | Format du mappage normal en entrée. Inverse efficacement la couche verte.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX :</b> l&#39;axe Y pointe vers le haut</li> <li data-preserve-html="true"><b>OpenGL :</b> l’axe Y pointe vers le bas</li> </ul> |

## Exemples

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 2](../../../../../../assets/normal_uncombine_example_4.png "Désassociation normale : Exemple 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 4](../../../../../../assets/normal_uncombine_example_6.png "Désassociation normale : Exemple 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

![Désassociation normale : Exemple 6](../../../../../../assets/normal_uncombine_example_5.png "Désassociation normale : Exemple 6"){zoomable="yes"}
