---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Utilisez le nœud de 3D linear gradient pour créer des dégradés linéaires basés sur la position universelle 3D pour les effets spatiaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-linear-gradient.resources/3d-linear-gradient.png){width="128px"}

<b>Entrée :</b> Générateurs de textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Crée un dégradé volumique basé sur le mappage de position d’entrée. Génère efficacement une transition du noir au blanc entre 2 points dans l’espace 3D. Destiné à être utilisé uniquement avec le moteur GPU.

Voir également [Masque de volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) pour obtenir un effet similaire.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode De Position Des Points</b> <i>Positions UV, Positions Espaces monde</i> | Choisissez si les points de dégradé fonctionnent dans l’espace UV (cela fonctionne mieux lorsque vous les définissez en Vue 2D) ou dans les coordonnées 3D, si vous souhaitez saisir manuellement une position exacte. |
| <b>Point 1</b> | Point de départ du dégradé. Il peut s’agir de coordonnées 2D ou 3D basées sur le mode Position. |
| <b>Point 2</b> | Point de fin du dégradé. Il peut s’agir de coordonnées 2D ou 3D basées sur le mode Position. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-linear-gradient.resources/3d-gradient.gif" />
        </td>
    </tr>
</table>
