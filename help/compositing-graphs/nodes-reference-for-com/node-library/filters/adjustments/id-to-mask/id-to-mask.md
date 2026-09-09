---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: Utilisez le nœud ID vers masque en niveaux de gris pour convertir les valeurs de mappage ID en masques en niveaux de gris pour la sélection de matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ID pour masquer les niveaux de gris
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# ID pour masquer les niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Identifier pour masquer l’icône en niveaux de gris](id-to-mask.resources/IDToMask.png "Identifier pour masquer l’icône en niveaux de gris"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Crée un masque à partir d’un mappage d’ID où les pixels avec les valeurs de pixels sélectionnées sont blancs.

Un mappage d’ID est une image où les pixels qui font partie d’un ensemble (par exemple, une forme) contiennent tous la même valeur d’identification unique. Dans ce cas, la valeur est un nombre entier.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>ID</b> <i>Niveaux de gris</i> PRINCIPAUX | Mappage d’ID d’entrée à partir duquel un masque doit être extrait. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Masque binaire extrait du mappage d&#39;ID d&#39;entrée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode de sélection</b> *Nombre entier* | Méthode de sélection des valeurs de pixels dans la carte d’ID, qui doivent être blanches dans le masque :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Solo :</b> sélectionnez une seule valeur de pixel</li> <li data-preserve-html="true"><b>Plage :</b> sélectionnez une plage de valeurs de pixels</li> </ul> |
| <b>Nombre entier d&#39;ID</b> *Nombre entier* *Disponible lorsque le « mode Sélection » est défini sur « Solo »* | Valeur de pixel dans le mappage d’ID qui doit être blanche dans le masque de sortie. |
| <b>Plage d’ID</b> *Entier2* *Disponible lorsque &#39;Mode de sélection&#39; est défini sur &#39;Plage&#39;* | Plage de valeurs de pixels dans le mappage ID, du début à la fin, qui doit être blanche dans le masque de sortie. |

## Exemples

<table>
  <tr>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ID à masquer : Exemple 2](id-to-mask.resources/id_to_mask_example_2.gif "ID à masquer : Exemple 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ID à masquer : Exemple 3](id-to-mask.resources/id_to_mask_example_3.png "ID à masquer : Exemple 3"){zoomable="yes"}

</td>
</tr>
</table>
