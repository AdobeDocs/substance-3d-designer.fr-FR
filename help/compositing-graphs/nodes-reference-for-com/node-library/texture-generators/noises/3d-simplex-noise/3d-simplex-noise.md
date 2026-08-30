---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: Utilisez le nœud de Bruit 3D Simplex pour générer des motifs de bruit 3D simplex afin de créer des textures volumiques lisses et naturelles.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bruit simplifié 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 5%

---


# Bruit simplifié 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-simplex-noise.resources/3d-simplex-noise.png){width="128px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un bruit procédural lorsqu&#39;un mappage de position baké est connecté à l&#39;emplacement d&#39;entrée. Il est destiné à être utilisé avec le moteur GPU uniquement.\
Similaire au [Bruit Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), mais plus rapide et plus simple, pour les cas où les performances et la vitesse sont importantes.

Ce bruit peut être testé avec [Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) en entrée au lieu d&#39;une map bakée réelle (comme dans l&#39;exemple d&#39;image ci-dessous).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle</b> <i>0.0 - 64.0</i> | Définissez l’échelle globale de l’effet. |
| <b>Taille</b> <i>0.0 - 2.0</i> | Effectuez une mise à l’échelle non uniforme sur les axes X, Y et Z séparément. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-simplex-noise.resources/3d-simplex.gif" />
        </td>
    </tr>
</table>
