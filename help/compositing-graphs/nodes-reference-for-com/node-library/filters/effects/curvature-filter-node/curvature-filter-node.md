---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Utilisez le noeud de filtrage Courbure pour générer des maps curvatures à partir de maps height de détection des surfaces convexes et concaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Courbure (Noeud de filtrage)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Courbure (Noeud de filtrage)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-filter-node.resources/curvature-filter-node-01.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue une conversion de courbure simple et stricte en une seule passe pour entrer [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). La texture obtenue présente des teintes blanches pour les zones convexes et noires pour les zones concaves. La courbure produit toujours des lignes fines en pixels et des transitions nettes.

Ce nœud est utile pour mettre rapidement en évidence ou obscurcir certains bords. Il est limité par rapport à [Courbure lisse](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (qui produit des résultats de meilleure qualité) et à [Courbure Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (qui offre plus d&#39;options).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 10.0</i> | Intensité de l’effet. Augmente le contraste du résultat. |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-filter-node.resources/curvature-filter-node-02.png" />
        </td>
    </tr>
</table>
