---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ''
description: Utilisez le nœud Liquide pour générer des motifs liquides et fluides afin de créer des effets de surface d'eau, d'huile et d'autres fluides.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Liquide
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# Liquide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](liquid.resources/liquid.png){width="128px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s&#39;agit d&#39;une variante simple du [bruit gaussien](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), qui [se déforme](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) avec lui-même pour créer un effet de type liquide.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle</b> <i>1 - 128</i> | Définit l’échelle globale de l’effet. |
| <b>Désordre</b> <i>0.0 - 1.0</i> | Déphasage du bruit pour introduire une faible variation |
| <b>Intensité de déformation</b> <i>0.0 - 1.0</i> | Définit l’intensité de l’effet de déformation. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Permet la compensation de la courbure et de l’étirement avec des proportions non carrées. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="liquid.resources/liquid-ex.gif" />
        </td>
    </tr>
</table>
