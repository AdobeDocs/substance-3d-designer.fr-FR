---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Utilisez le nœud Passe-haut de Luminance pour extraire les détails de luminance haute fréquence des textures afin d'améliorer les détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luminance passe-haut
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Luminance passe-haut

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](luminance-highpass.resources/luminance-highpass.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Annule les informations d&#39;éclairage en effectuant un [passe-haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) sur la valeur de Luminance d&#39;entrée. Utile pour fixer les textures photographiées avec des informations d’éclairage. Peut être combiné dans [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) avec plusieurs passes pour supprimer différentes fréquences des détails d&#39;éclairage.

Préserve mieux les couleurs que l&#39;[éclairage et annule les basses fréquences](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Rayon</b> <i>0.0 - 64.0</i> | Rayon de l’effet passe-haut. Un rayon inférieur annule un éclairage plus petit et s’ajuste en fonction des images d&#39;entrée. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="luminance-highpass.resources/luminance-highpass-example.png" />
        </td>
    </tr>
</table>
