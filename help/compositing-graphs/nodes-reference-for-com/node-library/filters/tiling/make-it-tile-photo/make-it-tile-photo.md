---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Utilisez le nœud Créer une vignette de photo pour convertir des photos en textures de répétition homogènes pour la création de matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Créer une photo en mosaïque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# Créer une photo en mosaïque

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-photo.resources/make-it-tile-photo.png)

![](make-it-tile-photo.resources/make-it-tile-photo-grayscale.png)

<b>Entrée :</b> Filtres > Répétition

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud fournit une fonctionnalité de correction des contours pour toute image dont les contours non continus peuvent empêcher la formation de mosaïques. Elle n&#39;affecte que les contours de l&#39;image d&#39;entrée. Si vous souhaitez ajuster l&#39;échelle ou la mosaïque de différentes manières, consultez la section [Réaliser un correctif de mosaïque](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Déformation du masque H</b> <i>-100.0 - 100.0</i> | Introduit la déformation sur l’axe horizontal, pour éviter les transitions non définies. |
| <b>Déformation du masque V</b> <i>-100.0 - 100.0</i> | Introduit la déformation sur l’axe vertical, pour éviter les transitions non définies. |
| <b>Taille du masque H</b> <i>0.0 - 1.0</i> | Définit la distance horizontale du bord de transition. |
| <b>Taille du masque V</b> <i>0.0 - 1.0</i> | Définit la distance verticale du bord de transition. |
| <b>Précision du masque H</b> <i>0.0 - 1.0</i> | Définit le lissage horizontal de la transition. |
| <b>Précision du masque V</b> <i>0.0 - 1.0</i> | Définit le lissage vertical de la transition. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-photo.resources/mit-photo-ex.png" />
        </td>
    </tr>
</table>
