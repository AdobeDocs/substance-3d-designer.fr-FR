---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Edge Wear Fibre Glass pour générer des masques d'usure sur les bords en fibre de verre en fonction de la courbure du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear en fibre de verre
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 6%

---


# Edge Wear en fibre de verre

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fiber-glass-edge-wear.resources/fiber-glass-edge-wear-01.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Représente un masque spécifiquement destiné à une usure de type fibre de verre, qui pourrait éventuellement être utilisé pour un tissu. En raison de la nature très mosaïque et répétitive des fibres, le mélange triplanaire peut éventuellement être activé.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour la mise en surbrillance des contours. Obligatoire ! |
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour masquer les zones occultées. Non requis, mais certainement recommandé. |
| <b>Entrée Usure/salissures</b> <i>Entrée en niveaux de gris</i> | Emplacement personnalisé en option pour remplacer le motif de fibre. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Espace universel normal</b> <i>Entrée couleur</i> | Utilisé uniquement pour le format triplanaire. |
| <b>Position</b> <i>Entrée couleur</i> | Utilisé uniquement pour le format triplanaire. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau d&#39;usure</b> <i>0.0 - 1.0</i> | Comme un [histogramme de balayage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), révèle progressivement l&#39;usure. |
| <b>Contraste d&#39;usure</b> <i>0.0 - 1.0</i> | Définit le contraste total de l’effet. |
| <b>Smoothness des contours</b> <i>0.0 - 16.0</i> | Définit le fond perdu/le flou des bords mis en surbrillance. |
| <b>Quantité Usure/salissures</b> <i>0.0 - 1.0</i> | Définit la proportion de l&#39;effet de fibre à fusionner entre les bords. Réglez-le avec le niveau d’usure pour obtenir un contrôle maximal. |
| <b>Masquage d&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Définit le degré d’influence de l’AO sur le masquage de l’effet. |
| <b>Épaisseur de la Courbure</b> <i>0.0 - 1.0</i> | Définit le degré d’influence des arêtes convexes de la Courbure. |
| <b>Utiliser l&#39;Usure/salissures personnalisée</b> <i>Faux/Vrai</i> | Remplace les fibres intégrées par un mappage personnalisé. |
| <b>Utiliser le mode triplanaire</b> <i>Faux/Vrai</i> | Permet à [Tri Planaire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) de masquer les seams. |
| <b>Contraste de fusion triplanaire</b> <i>0.0 - 1.0</i> | Contrôle le contraste de l’effet triplanaire. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fiber-glass-edge-wear.resources/fiber-glass-edge-wear-02.gif" />
        </td>
    </tr>
</table>
