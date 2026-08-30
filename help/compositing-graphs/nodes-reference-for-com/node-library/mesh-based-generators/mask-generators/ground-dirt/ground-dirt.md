---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: Utilisez le nœud Dirt au sol pour générer des masques d’accumulation de dirt en fonction de la position et de l’orientation du maillage par rapport au sol.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt au sol
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 6%

---


# Dirt au sol

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ground-dirt.resources/ground-dirt.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente le dirt qui s&#39;est accumulé de bas en haut, à l&#39;opposé de [Bas en haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) ou [Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md). Il n’a pas de mappage personnalisé personnalisé personnalisé personnalisé personnalisé.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Position</b> <i>Entrée en niveaux de gris</i> | Positionnement ancré sur lequel baser l’effet. Obligatoire ! |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit le niveau d’aspect total du dirt. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Height du Dirt</b> <i>0.0 - 1.0</i> | Définit l’height (proportionnel) d’affichage du dirt. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ground-dirt.resources/ground-dirt-ex.gif" />
        </td>
    </tr>
</table>
