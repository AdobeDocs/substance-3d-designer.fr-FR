---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Edge Wear pour générer des masques d'usure sur les maillages afin de créer des effets réalistes d'endommagement et d'altération des bords.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 7%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-wear.resources/edge-wear.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une image en noir et masque blanc en fonction des maps bakées et des paramètres utilisateur. Similaire à [Masques adaptables](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce nœud représente l&#39;usure des bords des objets. Il a pas mal de paramètres, mais n&#39;est pas le plus facile à utiliser : nous vous recommandons de jouer et de se faire une idée des choses. Le nœud est assez puissant, bien qu&#39;aucun masque de remplacement personnalisé ne puisse être effectué.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit l’étendue totale de l’effet. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Seuil</b> <i>0.0 - 1.0</i> | Similaire à Niveau, définit l’étendue totale de l’effet. |
| <b>Largeur des contours</b> <i>0.0 - 1.0</i> | Définit l’intensité de l’effet de mise en surbrillance. Réduisez pour les rendre plus clairsemés. |
| <b>Désordre</b> <i>0.0 - 1.0</i> | Définit la quantité de bruit à intégrer pour fractionner le smoothness. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-wear.resources/edge-wear-ex.gif" />
        </td>
    </tr>
</table>
