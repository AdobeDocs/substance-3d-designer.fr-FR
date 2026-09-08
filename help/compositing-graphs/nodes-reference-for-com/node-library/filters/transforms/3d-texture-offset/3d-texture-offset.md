---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/3d-texture-offset.html"
breadcrumb-title: ''
description: Utilisez le nœud Décalage de la Texture 3D pour décaler les textures dans l’espace 3D afin de créer des effets de parallaxe et des variations de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > 3D Texture Offset
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Décalage de la Texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Décalage de la Texture 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtextureoffsetgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtextureoffsetcolor.png){width="200px"}

</td>
</tr>
</table>

Filtre <b>Entrée :</b> > Transformation

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud **Décalage de Texture 3D** applique une *transformation de décalage* dans les axes **X**, **Y** et **Z** sur un objet décrit par la *texture 3D* connectée à l&#39;**entrée**.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Niveaux de gris/Couleur</i> | La <i>texture 3D</i> décrivant un objet 3D.<br>L&#39;objet est généralement décrit dans un <i>cube unitaire</i>. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Décalage</b> <i>Float3</i> | Quantité de décalage en <i>espace monde</i> appliquée à l&#39;objet décrit par la <i>texture 3D</i> connectée à l&#39;<b>entrée</b>. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtextureoffset-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtextureoffset-node.png" />
        </td>
    </tr>
</table>
