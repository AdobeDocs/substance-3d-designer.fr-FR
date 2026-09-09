---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: Utilisez le nœud Eclairage Annuler Hautes fréquences pour supprimer les détails d'éclairage haute fréquence des textures pour l'analyse des matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclairage Annuler Hautes Fréquences
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---


# Éclairage Annuler Hautes Fréquences

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](lighting-cancel-high-frequencies.resources/lighting-cancel-high-frequencies.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Similaire à [Passe-haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), mais plus adapté aux images couleur (cela ne désature pas autant le résultat), ce nœud tente d&#39;annuler les détails d&#39;éclairage de petite taille et haute fréquence.

Voir également [Éclairage Annuler les basses fréquences](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md) et, plus avancé, [Passe-haut de Luminance](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md) recommandé.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 1.0</i> | Force de l’effet d’annulation d’éclairage. |
| <b>Rayon</b> <i>0.0 - 10.0</i> | Rayon ou taille des détails d’éclairage à annuler. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="lighting-cancel-high-frequencies.resources/lighting-cancel-highfrequencies-example.png" />
        </td>
    </tr>
</table>
