---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud de Transforme Trapézoïde pour appliquer une distorsion trapézoïdale aux textures afin de créer des effets de correction de perspective.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transforme trapézoïdale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# Transforme trapézoïdale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](trapezoid-transform.resources/trapeze-transform.png){width="128px"}

![](trapezoid-transform.resources/trapeze-transform-grayscale.png){width="128px"}

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud de transforme spécial qui modifie l’entrée de manière perspective/déformation trapézoïdale. Contrôle les étires Haut et Bas. Les valeurs peuvent être poussées au-delà des limites pour des effets plus forts.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Étire supérieure</b> <i>0.0 - 1.0</i> | Définissez la quantité de étire ou de courge en haut. |
| <b>Étire inférieure</b> <i>0.0 - 1.0</i> | Définissez la quantité de étire ou la courbure au bas de l’écran. |
| <b>Couleur d&#39;arrière-plan</b> <i>(Niveaux de gris/Valeur de couleur)</i> | Définissez une couleur d’arrière-plan unie si la répétition est désactivée. |
| <b>Échantillonnage</b> <i>Bilinéaire, le plus proche</i> | Définissez la qualité d’échantillonnage. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="trapezoid-transform.resources/trapeze-example.gif" />
        </td>
    </tr>
</table>
