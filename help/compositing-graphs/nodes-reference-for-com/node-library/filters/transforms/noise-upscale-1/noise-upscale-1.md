---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit Upscale 1 pour mettre à niveau les textures à l’aide d’algorithmes basés sur le bruit afin de préserver les détails lors de l’augmentation de la résolution des textures.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Amélioration du bruit 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---


# Amélioration du bruit 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-1.resources/noise-upscale.png){width="128px"}

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Prend un bruit d’entrée procédural et le met à l’échelle jusqu’à une double résolution, en conservant les détails sans introduire trop de répétition. Utilise un masque de type « X » et fusionne avec un contraste similaire à l’entrée d’origine (le mode de fusion interne est Copier).

Ce nœud est principalement destiné à optimiser les graphes lents qui utilisent des bruits lourds et volumineux. Cela vous permet d’utiliser des résolutions plus élevées sans ajouter trop de temps de calcul supplémentaire.

Voir également [Amélioration de Bruit 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md) et [Amélioration de Bruit 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) pour différentes variantes de ce processus.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Décalage1X</b> <i>0.0 - 1.0</i> | Fait glisser les parties supérieure et inférieure sur l’axe X. |
| <b>Décalage1Y</b> <i>0.0 - 1.0</i> | Fait glisser les parties supérieure et inférieure sur l’axe Y. |
| <b>Offset2X</b> <i>0.0 - 1.0</i> | Fait glisser les parties gauche et droite sur l’axe X. |
| <b>Offset2Y</b> <i>0.0 - 1.0</i> | Fait glisser les parties gauche et droite sur l’axe Y. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-1.resources/noise1ex.png" />
        </td>
    </tr>
</table>
