---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation pour appliquer des effets de distorsion aux textures afin de créer des effets de déformation et de displacement.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---


# Déformation

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : Warp](warp.resources/warp-01.png "Nœud atomique : Warp"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Déplace les valeurs de pixels de l’image d’entrée en fonction des pentes calculées à partir d’une entrée de dégradé distincte, ce qui entraîne une déformation.

Contrairement à la déformation directionnelle, ce nœud s’éloigne uniformément des zones blanches, dans une direction définie par la pente ou le dégradé de l’entrée de dégradé.

</td>
</tr>
</table>

Le nœud peut être un peu difficile à manipuler, car le résultat de l’effet dépend très fortement de l’entrée de dégradé : de petits réglages du dégradé peuvent faire une énorme différence visuelle avec les mêmes valeurs d’intensité. Assurez-vous de jouer avec les commandes Contraste, Luminance et Échelle de l’Entrée de dégradé, ainsi qu’avec le curseur Intensité sur ce nœud.

Si vous connaissez les cartes de normales, vous pouvez imaginer le fonctionnement de ce nœud comme la conversion de l&#39;entrée de dégradé en une [carte de normales](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), puis la distorsion de l&#39;entrée de base dans la direction définie par les vecteurs de carte de normales. En fait, la [déformation vectorielle](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md) permet d’obtenir le même résultat. Des effets similaires sont également disponibles dans [Flou de Pente](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

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

## Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Intensité</b> *Flotter* | Définit l’intensité de la déformation. |
| <b>Mode de filtrage d&#39;entrée</b> *Booléen* | Détermine si le filtrage le plus proche ou bilinéaire est utilisé pour échantillonner l’entrée. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris/Couleur* PRINCIPAL | Image en couleurs ou en niveaux de gris. |
| <b>Entrée de dégradé</b> *Niveaux de gris* | La pente du dégradé de l’image d’entrée en niveaux de gris détermine l’effet de déformation dans l’image de sortie. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
