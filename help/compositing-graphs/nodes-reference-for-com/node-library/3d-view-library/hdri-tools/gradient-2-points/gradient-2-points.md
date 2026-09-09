---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-2-points.html"
breadcrumb-title: ''
description: Utilisez le nœud Dégradé 2 points pour créer des dégradés à deux points dans des environnements HDRI pour les transitions de couleurs du ciel et du sol.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient 2 Points
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé de 2 points
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---


# Dégradé de 2 points

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-2-points.resources/gradient-2-points.png){width="250px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Crée un dégradé de 2 couleurs entre deux points sélectionnés par l’utilisateur. Le résultat est ajusté en fonction de la projection sphérique. Similaire à [Dégradé linéaire (HDRI)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/gradient-linear-hdri/gradient-linear-hdri.md), mais avec deux points au lieu d&#39;un.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Position Du Point 1</b> | Position du premier point sélectionnée par l’utilisateur. Possède un handle en vue 2D. |
| <b>Couleur Point 1</b> <i>(valeur de couleur)</i> | Couleur au début du dégradé. |
| <b>Contraste Du Point 1</b> <i>0.0 - 1.0</i> | Contraste du premier masque de point. |
| <b>Position Du Point 2</b> | Position du deuxième point sélectionnée par l’utilisateur. Possède un handle en vue 2D. |
| <b>Couleur Point 2</b> <i>(valeur de couleur)</i> | Couleur à la fin du dégradé. |
| <b>Contraste du point 2</b> <i>0.0 - 1.0</i> | Contraste du second masque de point. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-2-points.resources/gradient-ex2.gif" />
        </td>
    </tr>
</table>
