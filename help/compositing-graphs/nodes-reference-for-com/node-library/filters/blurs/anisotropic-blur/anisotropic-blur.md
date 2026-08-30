---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou anisotrope pour appliquer des effets de flou directionnel afin de créer un flou directionnel et des traînées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou anisotrope
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# Flou anisotrope

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](anisotropic-blur.resources/anisotropic-blur-grayscale.png){width="128px"}

![](anisotropic-blur.resources/anisotropic-blur.png){width="128px"}

<b>Entrée :</b> Filtres > Flous

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue un [flou directionnel](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) de haute qualité, avec quelques paramètres pour personnaliser l&#39;apparence. Également appelé « flou de mouvement ».

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Flou anisotrope » pour les valeurs Couleur ou « Niveaux de gris anisotrope » pour les valeurs Niveaux de gris.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 16.0</i> | Force (rayon) du flou. Plus cette valeur est élevée, plus le flou sera important. |
| <b>Anisotropie</b> <i>0.0 - 1.0</i> | Directionnalité du flou. La définition de ce paramètre sur 0,0 revient à appliquer un flou normal. |
| <b>Angle</b> <i>0.0 - 1.0</i> | Définit l’angle de la direction du flou. |
| <b>Qualité</b> <i>0 - 1</i> | Bascule entre un flou [box](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) et un flou HQ en interne. La vitesse change pour la qualité. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="anisotropic-blur.resources/aniso-blur-example.gif" />
        </td>
    </tr>
</table>
