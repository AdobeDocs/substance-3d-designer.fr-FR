---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure de Peinture pour générer des masques d'usure de peinture en fonction de la géométrie du maillage afin de créer des effets d'écaillage de peinture réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usure De La peinture
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# Usure De La peinture

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une image en noir et masque blanc en fonction des maps bakées et des paramètres utilisateur. Similaire à [Masques adaptables](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente l&#39;écaillage de la peinture et l&#39;usure des bords.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Ambient occlusion</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Masque de variation</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit la quantité totale d’usure de la peinture, en la révélant progressivement. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Occlusion</b> <i>0.0 - 1.0</i> | Définit l&#39;effet de l&#39;AO baké sur la prévention de l&#39;usure dans les zones plus sombres. |
| <b>Rayon</b> <i>0.0 - 2.0</i> | Définit la distance sur laquelle l’effet d’écaillage s’étend à partir des contours convexes. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Définissez la quantité de variation (usure/salissures) à fusionner avec l’effet. |
| <b>Remplacer le masque de variation</b> <i>Faux/Vrai</i> | Active l&#39;emplacement d&#39;entrée de mappage de variation personnalisée (usure/salissures). |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/paint-wear-ex.gif" />
        </td>
    </tr>
</table>
