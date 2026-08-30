---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-linear-hdri.html"
breadcrumb-title: ''
description: Utilisez le nœud HDRI Dégradé linéaire pour créer des dégradés linéaires dans des environnements HDRI pour des configurations d’éclairage personnalisées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient Linear (HDRI)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé linéaire (HDRI)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# Dégradé linéaire (HDRI)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-linear-hdri.resources/gradient-linear.png){width="200px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Crée un dégradé linéaire à travers le centre et avec un point placé par l’utilisateur. Le résultat final est ajusté en fonction de la projection sphérique, contrairement au [dégradé linéaire normal de 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Position du point</b> | Position du point utilisée pour déterminer la direction du dégradé. |
| <b>Couleur supérieure</b> <i>(valeur de couleur)</i> | Couleur de la partie supérieure du dégradé (au point) |
| <b>Couleur du bas</b> <i>(valeur de couleur)</i> | Couleur de la partie inférieure du dégradé (à partir du point). |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-linear-hdri.resources/gradient-ex1.gif" />
        </td>
    </tr>
</table>
