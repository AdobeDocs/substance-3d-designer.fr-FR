---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Utilisez le nœud Sélecteur de matière pour sélectionner des matières en fonction des données de maillage afin de créer des effets de texture multi-matières.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sélecteur de matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# Sélecteur de matière

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## Sélecteur de matière

**Entrée :** *Générateurs Basés Sur Le Maillage**/Utilitaires*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Convertit un mappage d’ID en couleur en un masque binaire noir et blanc. Permet de fusionner et de combiner différentes couleurs dans un seul masque.

C&#39;est pratique si vous ne souhaitez pas utiliser [Fusion de plusieurs matériaux](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) et préférez utiliser le masque manuellement, ou si vous souhaitez utiliser manuellement ces mêmes masques à d&#39;autres endroits.

## Paramètres

* **Matières** : 1 - 16\
  Définit le nombre de matériaux pour lesquels la combinaison est activée.
* **Activer les #1-16 de matière** : faux/vrai\
  Active/désactive la fusion et la combinaison de couleurs dans le masque de sortie final. Peut être activé pour autant de couleurs que vous souhaitez combiner.
* **#1-16 de matière** : (valeur chromatique)\
  Sélecteur de couleurs pour la couleur des matériaux qui sera convertie en noir et blanc.
* **Paramètres du sélecteur de couleurs**\
  Modifie la fusion et la conversion de la couleur en noir et blanc.
  * **Tolérance** : 0,01 - 1,0\
    Degré de fusion avec les couleurs voisines.
  * **Remplissage** : 0,0 - 1,0\
    Netteté de la transition, comme Contraste.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
