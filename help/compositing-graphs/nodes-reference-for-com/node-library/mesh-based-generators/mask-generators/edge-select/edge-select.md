---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Utilisez le nœud de sélection des contours pour générer des masques en sélectionnant des contours de maillage afin de créer des effets d'altération et d'usure basés sur les contours.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Select
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---


# Edge Select

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-select.resources/edge-select-01.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une image en noir et masque blanc en fonction des maps bakées et des paramètres utilisateur. Similaire à [Masques adaptables](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque est le meilleur moyen de sélectionner n’importe quel type de contour en fonction de la courbure. Convexe, Concave à n&#39;importe quel niveau ou contraste peut être isolé, fournissant un excellent raccourci pour éviter de le faire manuellement via un [nœud Levels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour mettre en surbrillance les contours. Obligatoire ! |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit la quantité totale de mise en surbrillance des contours pour les modes Convexe et Concave. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste de la mise en surbrillance pour les modes Convexe et Concave. |
| <b>Convexe</b> |  |
| <b>Largeur des bords convexes</b> <i>0.0 - 1.0</i> | Définit la largeur de la mise en surbrillance des contours convexes. Gardez à l’esprit qu’une légère augmentation de la valeur Lissage peut entraîner un amincissement des bords. |
| <b>Lissage convexe</b> <i>0.0 - 1.0</i> | Définissez l’adoucissement de la transition pour les contours convexes. |
| <b>Intensité convexe</b> <i>0.0 - 1.0</i> | Définit l’intensité maximale de la mise en surbrillance des contours pour les contours convexes. Définissez la valeur sur 0 pour ne pas mettre en surbrillance. |
| <b>Concave</b> |  |
| <b>Largeur des contours concaves</b> <i>0.0 - 1.0</i> | Définissez la largeur de la mise en surbrillance pour les contours concaves. Gardez à l’esprit qu’une légère augmentation de la valeur Lissage peut entraîner un amincissement des bords. |
| <b>Lissage concave</b> <i>0.0 - 1.0</i> | Définissez l’adoucissement de la transition pour les bords concaves. |
| <b>Intensité concave</b> <i>0.0 - 1.0</i> | Définissez l’intensité maximale de la mise en surbrillance des contours pour les contours concaves. Définissez la valeur sur 0 pour ne pas mettre en surbrillance. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-select.resources/edge-select-02.gif" />
        </td>
    </tr>
</table>
