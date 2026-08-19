---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Utilisez le nœud Détection des contours pour détecter les contours dans les textures afin de créer des contours et des effets de masque basés sur les contours.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Detect
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# Edge Detect

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## Edge Detect

**Entrée :** *Filtres/Effets*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Détecte le contraste d’une image en noir et blanc, puis crée un masque noir et blanc mettant en évidence le contraste.

Utile dans de nombreux cas où une sorte de masque pour les bords est nécessaire. N&#39;oubliez pas que cela fonctionne mieux avec une entrée à contraste élevé ; si nécessaire, ajustez le contraste avant de passer quelque chose dans ce nœud.

## Paramètres

* **Largeur des bords** : *1.0 - 16.0* Largeur des zones détectées autour des bords.
* **Arrondi des bords** :*0.0 - 16.0* arrondit, floute et lisse le masque généré ensemble.
* **Inverser** : *Faux/Vrai*\
  Inverse le résultat.
* **Tolérance** : *0,0 - 1,0* facteur de seuil de tolérance pour l&#39;emplacement où les contours doivent apparaître.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
