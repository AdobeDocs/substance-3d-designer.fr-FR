---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: Utilisez le nœud Encoche du contour pour générer des motifs d’entaille sur les bords du filet afin de créer des effets réalistes d’endommagement et de retrait des bords.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Encoche de bord
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---


# Encoche de bord

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-notch.resources/edge-notch.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente un simple masque pour bords relevés, rompu par un bruit haute fréquence. Voir [Dirt du contour](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md) ou [Dommages au contour](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md) pour plus d&#39;options.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour mettre en surbrillance les contours. Obligatoire ! |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit le niveau de l’effet Encoche des contours. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-notch.resources/edge-notch-ex.gif" />
        </td>
    </tr>
</table>
