---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-smooth.html"
breadcrumb-title: ''
description: Utilisez le nœud Bevel smooth pour lisser les bords biseautés des formes et des motifs de surfaces réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bevel smooth
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---


# Bevel smooth

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Nuances de gris anisotrope de Kuwahara](bevel-smooth.resources/bevel_smooth.png "Icône Nuances de gris anisotrope de Kuwahara"){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Trace un dégradé ou une couleur plate à partir des bordures d’un masque vers l’extérieur, l’intérieur ou les deux.

Les dégradés qui se chevauchent sont triés par distance normalisée inversée afin de tracer la distance par rapport à la bordure la plus proche.

La distance du dégradé peut être ajustée dynamiquement le long de la bordure à l’aide d’une map distance.

</td>
</tr>
</table>

>[!TIP]
>
> Le nœud [Directional distance](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/directional-distance/directional-distance.md) offre des fonctionnalités similaires, où la dilatation est effectuée dans une direction spécifique.

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée de masque</b> <i>Niveaux de gris</i> PRINCIPAUX | Image à partir de laquelle extraire le masque.   Toutes les valeurs supérieures à la valeur « Seuil du masque » sont blanches dans ce masque. |
| <b>Entrée source</b> <i>Niveaux de gris</i> | Entrée facultative utilisée uniquement lorsque le paramètre « Mode de sortie » est défini sur « Dilatation ».   Dans ce cas, l’image est incrustée sur les zones blanches du masque et les valeurs de niveaux de gris des bordures sont dilatées. |
| <b>Map distance</b> <i>Niveaux de gris</i> | Entrée facultative utilisée lorsque la valeur du paramètre Multiplicateur de Map distance est supérieure à 0.   Il est utilisé pour ajuster la distance de biseautage/dilatation le long des bordures du masque, où une valeur plus sombre réduit la distance. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Image du résultat, en fonction du « Mode de sortie » sélectionné. |
| <b>UV</b> <i>Couleur</i> | Carte UV dans laquelle les UV sont dilatés le long des bordures du masque.   Vous pouvez le connecter à un nœud [mappeur UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md) pour mapper n&#39;importe quelle autre image à l&#39;aide de ces UV dilatés. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode de sortie</b> *Nombre entier* | Méthode de dilatation des bordures du masque :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Biseau :</b> dessinez un dégradé de 1 à 0, où 0 est atteint à la &#39;distance&#39; maximale</li> <li data-preserve-html="true"><b>Dilatation :</b> dessinez une couleur unie jusqu&#39;à la distance maximale. Cette couleur est le blanc de l’image de couleur « Entrée source » à la bordure du masque, si elle est connectée</li> <li data-preserve-html="true"><b>Distance :</b> distance brute à partir de la bordure de masque la plus proche, dans l&#39;espace d&#39;image normalisé où 1 est la longueur du côté le plus court de l&#39;image</li> </ul> |
| <b>Direction</b> *Nombre entier* *Disponible lorsque le « mode de sortie » est défini sur « Biseau » ou « Dilation »* | Le côté de la bordure du masque qui doit être dilaté :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Entrée :</b> dessinez vers l&#39;intérieur du masque</li> <li data-preserve-html="true"><b>Sortie :</b> dessinez vers l&#39;extérieur du masque</li> <li data-preserve-html="true"><b>Entrée/Sortie :</b> dessinez vers l&#39;intérieur et l&#39;extérieur du masque</li> </ul> |
| <b>Distance maximale</b> *Flotter* | Distance de dilatation, dans l&#39;espace image normalisé où 1 est la longueur du côté le plus court de l&#39;image d&#39;entrée. |
| <b>Masquer le smoothness</b> *Flotter* | Intensité du lissage appliqué au masque.   La valeur correspond au rayon du flou et 1 unité correspond à 1/256e de l’image. |
| <b>Décalage du masque</b> *Flotter* | Déplace les bordures du masque vers l’intérieur ou vers l’extérieur. |
| <b>Seuil de masque</b> *Flotter* | Valeur utilisée pour détecter les bordures du masque dans l’image « Entrée de masque ».   Les valeurs supérieures à ce seuil correspondent à l&#39;*intérieur* des formes de masque, tandis que les valeurs inférieures correspondent à l&#39;*extérieur*. |
| <b>Échelle</b> *Float2* | Règle les distances horizontale (X) et verticale (Y) de la dilatation.   Ces valeurs sont des multiplicateurs pour la valeur du paramètre Distance maximale. |
| <b>Multiplicateur de Map distance</b> *Nombre entier* | Ajuste l&#39;impact de la « Map distance » sur la « Distance maximale ». |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bevel smooth : Exemple 1](bevel-smooth.resources/bevel_smooth_example_1.gif "Bevel smooth : Exemple 1"){width="1024px" zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bevel smooth : Exemple 8](bevel-smooth.resources/bevel_smooth_example_8.jpg "Bevel smooth : Exemple 8"){width="1024px" zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_4_before.jpg" alt="biseau_lisse_exemple_4_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_4_after.jpg" alt="biseau_lisse_exemple_4_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_2_before.jpg" alt="biseau_lisse_exemple_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_2_after.jpg" alt="bevel_sleigh_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_3_before.jpg" alt="biseau_lisse_exemple_3_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_3_after.jpg" alt="bevel_sleigh_example_3_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_5_before.jpg" alt="biseau_lisse_exemple_5_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_5_after.jpg" alt="bevel_sleigh_example_5_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_7_before.jpg" alt="biseau_lisse_exemple_7_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_7_after.jpg" alt="biseau_lisse_exemple_7_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>
