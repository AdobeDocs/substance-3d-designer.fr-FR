---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Utilisez le nœud Moucheture des arêtes pour générer des motifs d'usure mouchetés sur les arêtes de maillage afin de créer des effets d'endommagement des arêtes réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 6%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-speckle.resources/edge-speckle.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente les contours avec une légère moucheté ajoutée pour les séparer. Voir également [Dirt Edge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour la mise en surbrillance des contours. Obligatoire ! |
| <b>Masque de variation</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque facultatif utilisé pour masquer les effets du nœud. Activez avec « Remplacer le masque de variation ». |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit la quantité totale de mise en surbrillance des contours. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Sélection des contours</b> <i>0.0 - 1.0</i> | Définit l’influence des contours convexes. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Définit la mesure dans laquelle le masque de variation décompose l’effet. |
| <b>Remplacer le masque de variation</b> <i>Faux/Vrai</i> | Remplace le masque intégré par un emplacement d’entrée personnalisé. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-speckle.resources/edge-speckle-ex.gif" />
        </td>
    </tr>
</table>
