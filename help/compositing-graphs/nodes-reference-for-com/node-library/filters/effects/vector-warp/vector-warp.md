---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation vectorielle pour déformer des textures à l’aide de champs vectoriels afin de créer des effets de distorsion fluides et organiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation vectorielle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# Déformation vectorielle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-warp.resources/vector-warp.png){width="128px"}

![](vector-warp.resources/vector-warp-grayscale.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

La déformation vectorielle est un effet de distorsion avancé, similaire à la [déformation](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) et à la [déformation directionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), avec la principale différence qu’il est piloté par un bitmap vectoriel (couleur) plutôt que par une texture en niveaux de gris. Cela signifie qu&#39;il est plus puissant et polyvalent que ses cousins de nœuds atomiques.

La texture vectorielle est similaire à une texture normale, mais elle n’a pas besoin d’être normalisée et seuls les canaux R et Vert (X et Y) sont utilisés. Les couches bleue et Alpha peuvent être laissées en noir si vous le souhaitez. La construction d&#39;une bonne carte vectorielle peut constituer le plus grand défi lors de l&#39;utilisation de ce nœud. Vous pouvez [convertir les cartes en niveaux de gris en cartes normales](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) ou construire la carte en combinant des canaux avec[Fusion RVBA](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md). Vous pouvez également utiliser un élément de type [« Flow Map »](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting).

Ce nœud peut être utile lorsque vous voulez effectuer des distorsions très spécifiques avec des directions variables, où les nœuds de déformation standard ne le coupent pas.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Entrée couleur</i> | Mappez pour déformer. |
| <b>Carte vectorielle</b> <i>Entrée couleur</i> | Mappage du pilote de distorsion. Les couches de couleur Rouge et Bleu sont utilisées. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 1.0</i> | Multiplicateur d’intensité pour la carte vectorielle. |
| <b>Format vectoriel</b> <i>DirectX, OpenGL</i> | Permute la couche verte entre les interprétations Haut et Bas. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="vector-warp.resources/vector-warp-ex.png" />
        </td>
    </tr>
</table>
