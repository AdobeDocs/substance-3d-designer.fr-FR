---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Edge Wear de métal pour générer des masques d'usure sur les bords métalliques en fonction de la courbure et de la position du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de métal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# Edge Wear de métal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente l&#39;usure des bords d&#39;un objet métallique, avec des rayures et des copeaux apparaissant sur les bords relevés convexes, potentiellement masqués par les zones sombres de l&#39;AO cuites.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Entrée Usure/salissures</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Espace universel normal</b> <i>Entrée couleur</i> |  |
| <b>Position</b> <i>Entrée couleur</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau d&#39;usure</b> <i>0.0 - 1.0</i> | Définit la quantité totale d’usure, révèle progressivement. |
| <b>Contraste d&#39;usure</b> <i>0.0 - 1.0</i> | Définit le contraste du résultat final. |
| <b>Smoothness des contours</b> <i>0.0 - 16.0</i> | Définit le smoothness de la atténuation par rapport aux arêtes de la Courbure. |
| <b>Quantité Usure/salissures</b> <i>0.0 - 1.0</i> | Définit la quantité d’usure/salissures à intégrer entre les contours. |
| <b>Échelle Usure/salissures</b> <i>1 - 16</i> | Définit l’échelle de l’Usure/salissures. |
| <b>Masquage d&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Définit la quantité d’effet de l’IA sur l’effet final, les zones sombres étant masquées. |
| <b>Épaisseur de la Courbure</b> <i>0.0 - 1.0</i> | Définit la quantité d’effet que les contours convexes de la Courbure ont sur l’effet final. |
| <b>Utiliser l&#39;Usure/salissures personnalisée</b> <i>Faux/Vrai</i> | Active un emplacement d&#39;entrée de mappage Usure/salissures personnalisé. |
| <b>Utiliser le mode triplanaire</b> <i>Faux/Vrai</i> | Activez la projection [Tri Planaire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) pour masquer les seams. |
| <b>Contraste de fusion triplanaire</b> <i>0.0 - 1.0</i> | Définit le contraste de fusion pour la Projection triplanaire. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-ex.gif" />
        </td>
    </tr>
</table>
