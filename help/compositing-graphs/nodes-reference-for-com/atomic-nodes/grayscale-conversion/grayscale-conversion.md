---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ''
description: Utilisez le nœud Conversion en niveaux de gris pour convertir les textures colorimétriques en niveaux de gris à l’aide de diverses méthodes de conversion.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conversion en niveaux de gris
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 7%

---


# Conversion en niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : conversion en niveaux de gris](grayscale-conversion.resources/comp_grayscaleconversion_1.png "Nœud atomique : conversion en niveaux de gris"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Convertit une image couleur en niveaux de gris en évaluant la luminance de chaque canal de couleur.

Ce nœud peut être utilisé comme méthode optimisée pour extraire une couche en niveaux de gris d’une image couleur, en définissant toutes les valeurs « Épaisseurs de couche » sur 0, à l’exception de la couche souhaitée, qui doit être définie sur 1.

</td>
</tr>
</table>

La plupart des nœuds peuvent être définis pour une sortie en niveaux de gris ou en couleurs, le premier étant préférable pour des raisons de simplicité et de performances.

En effet, il est recommandé de travailler en niveaux de gris dès le départ et de coloriser les images plus tard dans votre workflow, en utilisant par exemple un nœud [Courbe de transfert de dégradé](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md).

Cela signifie qu’un nœud de conversion en niveaux de gris est généralement réservé uniquement aux cas où vous souhaitez spécifiquement convertir une image couleur en niveaux de gris. Dans ces cas, examinez également la [conversion des niveaux de gris avancée](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md) et la [conversion des couleurs en masques](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Paramètres

</td>
<td style="border: 0;" valign="top">

### Connecteurs d’entrée

</td>
<td style="border: 0;" valign="top">

### Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Épaisseurs de canal</b> *Float4* | Définit le poids de chaque couche RVBA dans la conversion en niveaux de gris.   Par défaut, un fractionnement régulier est effectué sur les canaux du RGB. |
| <b>Aplatir alpha</b> *Booléen* | Définit le comportement de l’Alpha sur les niveaux de gris finaux, car les valeurs de niveaux de gris ne peuvent pas contenir d’informations sur l’Alpha.   Lorsque *True*, la conversion en niveaux de gris est multipliée par rapport à la couche Alpha de l&#39;image d&#39;entrée |
| <b>Valeur d&#39;arrière-plan</b> *Flotter* | Définit la valeur d’arrière-plan de base lorsque l’entrée comporte un masque alpha. C’est-à-dire qui détermine les pixels à traiter comme transparents.   *Disponible lorsque &#39;Flatten alpha&#39; est défini sur &#39;True&#39;.* |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Couleur* PRINCIPALE | Image couleur à traiter. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris* |  |

## Exemples

*Bientôt disponible.*
