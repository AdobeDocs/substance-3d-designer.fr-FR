---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Utilisez le nœud Créer une photo en mosaïque pour convertir les photos en textures de mosaïque homogènes pour la création de matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Créer une photo en mosaïque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Créer une photo en mosaïque

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

## Créer une photo en mosaïque (niveaux de gris)

**Entrée :** *Filtres/Limites*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud fournit une fonctionnalité de correction des contours pour toute image dont les contours non continus peuvent empêcher la formation de mosaïques. Elle n’affecte rien d’autre que les bords de l’image d’entrée. Si vous souhaitez ajuster l&#39;échelle ou la mosaïque de différentes manières, consultez la section [Réaliser un correctif de mosaïque](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

## Paramètres

* **Déformation du masque H** : *-100.0 - 100.0* Introduit la déformation sur l’axe horizontal, pour éviter les transitions non définies.
* **Déformation du masque V** : *-100.0 - 100.0* Introduit la déformation sur l’axe vertical, pour éviter les transitions non définies.
* **Taille du masque H** : *0.0 - 1.0* Définit la distance jusqu&#39;à laquelle le bord de transition atteint horizontalement.
* **Taille du masque V** : *0.0 - 1.0* Définit la distance à laquelle le bord de transition atteint verticalement.
* **Précision du masque H** : *0.0 - 1.0* Définit le lissage horizontal de la transition.
* **Précision du masque V** : *0.0 - 1.0* Définit la fluidité de la transition verticale.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mit-photo-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
