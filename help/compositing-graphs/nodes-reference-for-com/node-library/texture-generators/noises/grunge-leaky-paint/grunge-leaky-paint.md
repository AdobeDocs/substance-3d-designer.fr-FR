---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-leaky-paint.html"
breadcrumb-title: ''
description: Utilisez le nœud Peinture avec fuite d’Usure/salissures pour générer des motifs de fuite de peinture afin de créer des effets de surface vieillis et altérés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Grunge Leaky Paint
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Peinture avec fuite d’Usure/salissures
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Peinture avec fuite d’Usure/salissures

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grunge-leaky-paint.resources/grungeleakypaint.jpg){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud **Usure/salissures Leaky Paint** génère une carte usure/salissures semblable à celle de la peinture qui s&#39;écoule à travers les fuites.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Balance</b> <i>Flotter</i> | Règle la balance entre les valeurs sombres et claires. |
| <b>Contraste</b> <i>Flotter</i> | Règle le contraste de l’image. |
| <b>Inverser</b> <i>Booléen</i> | Inverse la sortie de l&#39;image, à l&#39;aide d&#39;une opération `1-x`. |
| <b>Extension non carrée</b> <i>Booléen</i> | Permet la compensation de la courbure et de l’étirement avec des proportions non carrées. |
| <b>Avancé</b> |  |
| <b>Intensité de la fuite</b> <i>Flotter</i> | Règle la densité et l’intensité des gouttes. |
| <b>Échelle de fuite</b> <i>Nombre entier</i> | Règle l’échelle de la séparation des gouttes. |
| <b>Angle de fuite aléatoire</b> <i>Flotter</i> | Ajuste l&#39;*angle maximal* auquel les gouttes peuvent être tournées de manière aléatoire, en *nombre de tours*. |
| <b>Netteté de la fuite</b> <i>Flotter</i> | Règle la netteté et la netteté des gouttes. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grunge-leaky-paint.resources/grungeleakypaint-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="grunge-leaky-paint.resources/grungeleakypaint-variant2.jpg" />
        </td>
    </tr>
</table>
