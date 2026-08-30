---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure du cuir pour générer des masques d'usure sur les surfaces en cuir en fonction de la courbure du maillage et des points de contact.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usure du cuir
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# Usure du cuir

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-wear.resources/leather-wear.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente l&#39;usure avec un motif en cuir, avec plus d&#39;usure sur les bords en fonction de la Courbure. Son fonctionnement est similaire à celui de l&#39;[Edge Wear fibre de verre](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) et ses paramètres sont généralement identiques.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour le placement des contours. Obligatoire ! |
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour occlure certaines zones. Recommandé, mais pas obligatoire. |
| <b>Entrée Usure/salissures</b> <i>Entrée en niveaux de gris</i> | Emplacement d&#39;entrée de mappage Usure/salissures facultatif qui peut être basculé via le paramètre « Utiliser l&#39;Usure/salissures personnalisée ». |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau d&#39;usure</b> <i>0.0 - 1.0</i> | Définit le niveau d’usure global, progressivement révélateur. |
| <b>Contraste d&#39;usure</b> <i>0.0 - 1.0</i> | Définit le contraste de l’effet. |
| <b>Quantité Usure/salissures</b> <i>0.0 - 1.0</i> | Définit la quantité d’usure/salissures (motif de cuir par défaut) à mélanger entre les contours. |
| <b>Masquage d&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Définit la mesure dans laquelle l’OA masque les effets d’usure. |
| <b>Épaisseur de la Courbure</b> <i>0.0 - 1.0</i> | Définit la mesure dans laquelle les contours de la courbure affectent le résultat final. Même si la valeur est définie sur 0, vous avez toujours besoin d&#39;une courbe de courbure. |
| <b>Utiliser l&#39;Usure/salissures personnalisée</b> <i>Faux/Vrai</i> | Permet de remplacer le motif en cuir par défaut intégré. Utilisez plutôt un emplacement d’entrée personnalisé. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-wear.resources/leather-wear-ex.gif" />
        </td>
    </tr>
</table>
