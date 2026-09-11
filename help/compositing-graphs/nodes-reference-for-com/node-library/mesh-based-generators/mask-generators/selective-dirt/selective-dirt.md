---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Utilisez le nœud Dirt sélectif pour générer des masques d'accumulation de dirt sélectif en fonction de la géométrie du maillage afin d'obtenir une altération réaliste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt sélectif
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 8%

---


# Dirt sélectif

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](selective-dirt.resources/selective-dirt.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une image en noir et masque blanc en fonction des maps bakées et des paramètres utilisateur. Similaire à [Masques adaptables](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) représente un effet de dirt simple sur les contours convexes.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Masque de variation</b> <i>Entrée en niveaux de gris</i> | Carte de variation facultative, qui peut être activée via des paramètres. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit le niveau total de l’effet, qui s’affiche progressivement. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Définit la quantité de variation/usure/salissures à fusionner avec l’effet. |
| <b>Remplacer le masque de variation</b> <i>Faux/Vrai</i> | Permet de remplacer la variante par un emplacement d’entrée personnalisé. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="selective-dirt.resources/selective-dirt-ex.gif" />
        </td>
    </tr>
</table>
