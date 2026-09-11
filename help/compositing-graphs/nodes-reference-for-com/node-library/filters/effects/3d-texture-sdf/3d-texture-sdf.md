---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Utilisez le nœud SDF Texture 3D pour générer des textures de champs de distance signées à partir de données 3D afin de créer des formes et des effets lisses.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Texture SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# 3D Texture SDF

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3dtexturesdf.png){width="200px"}

<b>Entrée :</b> Filtre > Effet

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud SDF **de** Texture 3D génère le *champ de distance signé* d&#39;une forme à partir du masque *texture 3D* de **Entrée** représentant les tranches du *volume* de la forme.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée de masque</b> <i>Niveaux de gris</i> | Le masque de <i>texture 3D</i> représentant les tranches du <i>volume</i> d&#39;une forme. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Seuil</b> <i>Flottant</i> | Lorsque le volume de forme est décrit par un <i>dégradé de fondu</i>, définit la valeur de dégradé à laquelle la <i>surface</i> de la forme est <i>détectée</i>. |
| <b>Sortie</b> <i>Entier</i> | Type de champ de distance à générer :<br>- <i>Champ de distance</i> : génère un champ de distance décrivant les distances <i>à l&#39;extérieur</i> de la forme.<br>- <i>Champ de distance signée</i> : génère un champ de distance décrivant les distances <i>à l&#39;extérieur</i> (positives) et <i>à l&#39;intérieur</i> (négatives) de la forme. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-node.png" />
        </td>
    </tr>
</table>
