---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Utilisez le nœud Noise Upscale 3 pour mettre à niveau les textures à l’aide d’algorithmes avancés basés sur le bruit afin de préserver les détails à des résolutions plus élevées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Amélioration du bruit 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---


# Amélioration du bruit 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Prend un bruit d’entrée procédural et le met à l’échelle jusqu’à une double résolution, en conservant les détails sans introduire trop de mosaïque. Utilise un masque défini par l’utilisateur pour fusionner le bruit au-dessus de son échelle d’origine.

Ce nœud est principalement destiné à l’optimisation des graphes lents qui utilisent des bruits intenses et importants. Cela vous permet d’utiliser des résolutions plus élevées sans ajouter trop de temps de calcul supplémentaire.

Voir également [Amélioration du bruit 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) et [Amélioration du bruit 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), qui, dans la plupart des cas, ont tendance à être légèrement meilleurs pour masquer les carreaux.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Niveaux de gris</b> <i>Entrée en niveaux de gris</i> | Image Bruit cible. |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/noise3ex.png" />
        </td>
    </tr>
</table>
