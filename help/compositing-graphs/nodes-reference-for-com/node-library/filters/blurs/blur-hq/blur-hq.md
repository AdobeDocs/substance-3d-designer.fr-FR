---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Utilisez le nœud Blur HQ pour appliquer des effets de flou de haute qualité aux textures afin de créer des effets de flou lisses et de qualité professionnelle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# Flou HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/blur-hq-1.png){width="128px"}

![](../../../../../../assets/blur-hq-grayscale.png){width="128px"}

<b>Entrée :</b> Filtres > Flous

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique un flou gaussien de haute qualité au résultat. Bien meilleure qualité que le [flou de boîte atomique standard](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)[.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Blur HQ » pour les entrées Color ou « Blur HQ Grayscale » pour les entrées Grayscale.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 16.0</i> | Force (rayon) du flou. Plus cette valeur est élevée, plus le flou sera important. |
| <b>Qualité</b> <i>0 - 1</i> | Augmente la quantité d’échantillonnage interne pour une qualité encore plus élevée, à une vitesse de calcul réduite. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/hqblur-example.gif" />
        </td>
    </tr>
</table>
