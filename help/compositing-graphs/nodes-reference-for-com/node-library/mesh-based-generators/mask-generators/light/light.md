---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Utilisez le nœud Lumière pour générer des masques en fonction des conditions d’éclairage du maillage afin de créer des variations de matériau réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lumière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# Lumière

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](light.resources/light-01.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque est un peu différent des autres générateurs : il ne fait que de faux éclairages, basés sur la carte normale de l&#39;espace mondial, renvoyant un masque « lightmap » en noir et blanc.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Angle Horizontal</b> <i>0.0 - 1.0</i> | Définit l’angle horizontal de la fausse lumière. |
| <b>Angle vertical</b> <i>0.0 - 1.0</i> | Définit l’angle vertical de la fausse lumière. |
| <b>Mettre en surbrillance la Brillance</b> <i>0.0 - 0.999</i> | Définit la planche de retrait de la zone mise en surbrillance. |
| <b>Niveau de surbrillance</b> <i>0.0 - 1.0</i> | Définit le niveau de luminosité de la zone mise en surbrillance. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="light.resources/light-02.gif" />
        </td>
    </tr>
</table>
