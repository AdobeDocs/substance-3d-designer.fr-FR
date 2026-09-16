---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ""
description: Utilisez le nœud Déformation pour appliquer des effets de distorsion à des textures afin de créer des effets de déformation et de displacement.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 9%
---

# Déformation

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Noeud atomique : Warp](warp.resources/comp_warp_1.png "Noeud atomique : Warp"){width="100%"}

<b>Entrée :</b> Noeuds atomiques

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Déplace les valeurs de pixels de l’image d’entrée en fonction des pentes calculées à partir d’une entrée de dégradé distincte, ce qui entraîne une déformation.

Contrairement à la Déformation directionnelle, ce nœud s’éloigne uniformément des zones blanches, dans une direction définie par la pente ou le dégradé de l’entrée de dégradé.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="warp.resources/warp-tooltip.gif" alt="info-bulle de déformation" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Le nœud peut être un peu difficile à manipuler, car le résultat de l’effet dépend très fortement de l’entrée de dégradé : de petits réglages du dégradé peuvent faire une énorme différence visuelle avec les mêmes valeurs d’intensité. Assurez-vous de jouer avec le contraste, la Luminance et l’échelle de l’entrée de dégradé, ainsi que le curseur Intensité sur ce nœud.

Si vous connaissez les Maps normal, vous pouvez imaginer le fonctionnement de ce nœud comme la conversion de l&#39;entrée de dégradé en une [Map normal](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), puis la distorsion de l&#39;entrée de base dans la direction définie par les vecteurs de Map normal. En fait, la [déformation vectorielle](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md) permet d’obtenir le même résultat. Des effets similaires sont également disponibles dans [Flou de Pente](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).



## Paramètres

|  |  |
| --- | --- |
| <b>Intensité</b> *Flottant* | Définit l’intensité de la déformation. |
| <b>mode de filtrage d&#39;entrée</b> *Booléen* | Détermine si le filtrage le plus proche ou bilinéaire est utilisé pour échantillonner l’entrée. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris/Couleur* PRINCIPAL | Couleur ou image en niveaux de gris. |
| <b>Entrée de dégradé</b> *Niveaux de gris* | La pente du dégradé de l’image d&#39;entrée en niveaux de gris détermine l’effet de déformation dans l’image de sortie. |


## Exemples

*Bientôt disponible.*
