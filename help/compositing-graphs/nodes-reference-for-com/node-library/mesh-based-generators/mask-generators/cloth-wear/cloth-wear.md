---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure du tissu pour générer des masques d'usure sur les surfaces du tissu en fonction de la courbure du maillage et des zones de contact.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usure du tissu
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Usure du tissu

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cloth-wear.resources/cloth-wear-01.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Le masque représente les bords effilochés sur les matériaux en tissu. Il utilise une carte de hauteur de détail de tissu qui détermine la plupart de l&#39;aspect ; sans une carte appropriée, l&#39;effet semble très basique.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Height de tissu</b> <i>Entrée en niveaux de gris</i> | Height pour le motif de tissu uniquement. Il ne s’agit pas de l’height de votre objet (cuit), mais plutôt d’un motif de détail en mosaïque. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Courbure cuite/générée pour déterminer les bords relevés. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité de bords nets</b> <i>0.0 - 1.0</i> |  |
| <b>Lissage</b> <i>0.0 - 5.0</i> | Détermine le niveau de flou/adoucissement des bords usés. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cloth-wear.resources/cloth-wear-02.gif" />
        </td>
    </tr>
</table>
