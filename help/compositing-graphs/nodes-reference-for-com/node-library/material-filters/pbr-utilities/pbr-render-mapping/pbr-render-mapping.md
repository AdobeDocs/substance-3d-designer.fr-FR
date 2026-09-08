---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: Utilisez le nœud Correspondance de Rendu PBR pour convertir les sorties de matériau en différents formats de correspondance de Rendu PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappage de rendu PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# Mappage de rendu PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

<b>Entrée :</b> Filtres de matériau > Utilitaires PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s&#39;agit d&#39;un nœud d&#39;extension pour le [nœud Rendu PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), qui vous permet de mapper une texture distincte sur la forme à partir d&#39;un [nœud Rendu PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) précédent. Son objectif principal est de vous permettre de remapper chaque canal séparé de votre [Rendu PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), de nouveau sur la forme, pour créer des ventilations de canal de mappage composite, comme dans les exemples ci-dessous. Vous êtes libre de créer votre propre méthode composite et vos propres masques en utilisant les nœuds de mappage de Rendu PBR comme composant.

Il existe une version en couleurs et en niveaux de gris pour les deux types de données : utiliser la couleur pour les cartes de diffusion, utiliser les niveaux de gris pour les cartes de rugosité, de métal et autres cartes en niveaux de gris.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Texture</b> <i>Entrée Couleur/Niveaux De Gris</i> | Texture à mapper sur la forme. |
| <b>UV</b> <i>Entrée couleur</i> | Entrée de données d&#39;UV obligatoire à partir d&#39;un [nœud de Rendu PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md). |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Définissez une valeur de couleur unie à utiliser en arrière-plan. |

## Exemples

Exemple : composition de quatre nœuds de mappage de Rendu PBR différents utilisant un [histogramme sélectionné](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md) sur un [dégradé linéaire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) comme masques.

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/pbr-render-mapping-ex.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/pbr-render-mapping-ex-2.png" />
        </td>
    </tr>
</table>
