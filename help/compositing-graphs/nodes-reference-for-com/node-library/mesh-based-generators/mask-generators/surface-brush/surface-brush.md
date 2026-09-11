---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Utilisez le nœud Pinceau de surface pour générer des masques en fonction de l'orientation de la surface afin de créer des effets d'altération et d'usure directionnels.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pinceau de surface
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 7%

---


# Pinceau de surface

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](surface-brush.resources/surface-brush.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une image en noir et masque blanc en fonction des maps bakées et des paramètres utilisateur. Similaire à [Masques adaptables](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente un effet intéressant de brossage du métal sur une surface de l&#39;objet, occulté par la géométrie de l&#39;objet et l&#39;AO.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Normale de l&#39;espace monde</b> <i>Entrée couleur</i> |  |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Ambient occlusion</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Position</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit le niveau d’effet global, progressivement révélateur. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Longueur Scratches</b> <i>0.0 - 8.0</i> | Définit la longueur des rayures. Les valeurs plus faibles sont plus semblables à des points, les valeurs plus élevées sont des traits longs. |
| <b>Axe d&#39;occlusion</b> <i>X, Y, Z, none</i> | Axe de l’objet qui doit recevoir les rayures. Ne modifie pas le sens des rayures. |
| <b>Intensité de l&#39;Axe d&#39;occlusion</b> <i>0.0 - 1.0</i> | Force de l’effet occlusion axe. |
| <b>Occlusion</b> <i>0.0 - 1.0</i> | Force de l&#39;AO sur les rayures occlusives. |
| <b>Netteté</b> <i>0.0 - 1.0</i> | Définissez la quantité de post-netteté à appliquer aux rayures. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="surface-brush.resources/surface-brush-ex.gif" />
        </td>
    </tr>
</table>
