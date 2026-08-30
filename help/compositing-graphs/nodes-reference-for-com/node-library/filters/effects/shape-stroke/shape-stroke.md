---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: Utilisez le nœud Contour de forme pour ajouter des contours de contour aux formes afin de créer des bordures et des effets de contour.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Contour
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# Contour

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke.png){width="128px"}

![](shape-stroke.resources/shape-stroke-grayscale.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ajoute un contour autour d’un noir et d’un masque blanc (pour la version en niveaux de gris) ou d’une forme avec un canal Alpha (pour la version en couleurs), comme vous le savez peut-être déjà dans d’autres applications de retouche d’images 2D. Peut être considéré comme une version plus complète de [Edge Detect](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md).

Très utile pour une variété d’effets de retouche d’images.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Largeur</b> <i>-1.0 - 1.0</i> | Largeur de l’effet de contour. |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité globale de l’effet. |
| <b>(Contour) Couleur</b> <i>(valeur de couleur)</i> | Couleur utilisée pour l’effet de contour. |
| <b>Couleur du masque</b> <i>(valeur de couleur) (version en niveaux de gris uniquement)</i> | Couleur unie à utiliser pour la sortie du mappage de transparence. |
| <b>L&#39;Entrée Est Prémultipliée</b> <i>Faux/Vrai (Version Couleur Uniquement)</i> | Indique si l&#39;entrée doit être considérée comme prémultipliée. |
| <b>Prémultiplier La Sortie</b> <i>Faux/Vrai</i> | Indique si la sortie doit être prémultipliée. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shapestroke-ex.png" />
        </td>
    </tr>
</table>
