---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Utilisez le nœud Courbure Sobel pour détecter les contours de courbure à l’aide d’opérateurs Sobel pour créer des masques de contour.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure Sobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# Courbure Sobel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-sobel.resources/curvature-sobel.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue une conversion de courbure simple et stricte en une seule passe pour entrer [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). La texture obtenue présente des teintes blanches pour les zones convexes et noires pour les zones concaves. La courbure produit toujours des lignes plus épaisses et des transitions nettes.

Ce nœud est utile pour mettre rapidement en évidence ou obscurcir certains bords. Elle est légèrement différente de la [Courbure](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), car elle produit de meilleurs résultats de qualité, tout en étant nette et dure.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 1.0</i> | Intensité de l’effet : ajuste le contraste. |
| <b>Type normal</b> <i>DirectX, OpenGL</i> |  |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-sobel.resources/curv-sobel-ex.png" />
        </td>
    </tr>
</table>
