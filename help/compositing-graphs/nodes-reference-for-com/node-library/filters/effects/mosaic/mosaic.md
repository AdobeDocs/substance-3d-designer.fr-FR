---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: Utilisez le nœud Mosaïque pour créer des effets de mosaïque en divisant les textures en blocs et motifs pixellisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# Mosaïque

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-1.png){width="128px"}

![](mosaic.resources/mosaic-grayscale.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

« Facétise » une courbe de transfert de dégradé existante, lisse et en pente en effectuant un effet [Déformation](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) multi-passes. Lorsqu&#39;une même texture est utilisée pour les deux entrées, elle grossit et accentue essentiellement les zones les plus claires.

Cette option est utile pour ajouter plus de définition aux cartes en niveaux de gris telles que Heightmap, car elle peut donner plus de définition aux formes.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Couleur</b> <i>Entrée Couleur/Niveaux De Gris</i> |  |
| <b>Mosaic Map</b> <i>Entrée en niveaux de gris</i> | Déformation de la carte de pilote. Peut être identique à la première entrée. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Exemples</b> <i>0 - 16</i> | Détermine la qualité multi-échantillon. |
| <b>Intensité</b> <i>0.0 - 1.0</i> | Force de l’effet. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaci-ex.png" />
        </td>
    </tr>
</table>
