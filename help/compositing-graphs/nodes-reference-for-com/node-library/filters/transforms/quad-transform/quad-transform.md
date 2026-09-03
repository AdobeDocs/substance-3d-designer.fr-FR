---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transforme quadrilatère pour appliquer des transformations quadrilatérales aux textures afin de corriger les perspectives et la déformation.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transforme Quad
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# Transforme Quad

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](quad-transform.resources/quad-transform-01.png){width="128px"}

![](quad-transform.resources/quad-transform-02.png){width="128px"}

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud de transforme spécial qui permet la transformation d’une forme en quad par interaction avec ses points d’angle. Permet d’effectuer des transformes très spécifiques de manière pratique.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>p00</b> | Point supérieur gauche. |
| <b>p01</b> | Point inférieur gauche |
| <b>p10</b> | En haut à droite. |
| <b>p11</b> | En bas à droite. |
| <b>Abattage</b> <i>Avant uniquement, Arrière uniquement, Avant sur arrière, Arrière sur avant</i> | Définir l&#39;abattage/le masquage de la forme lorsque les points se croisent. |
| <b>Activer la Répétition</b> <i>Faux/Vrai</i> |  |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur Niveaux de gris)</i> | Couleur d’arrière-plan unie si la répétition est désactivée. |
| <b>Échantillonnage</b> <i>Bilinéaire, le plus proche</i> | Définissez la qualité d’échantillonnage. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="quad-transform.resources/quad-transform-03.gif" />
        </td>
    </tr>
</table>
