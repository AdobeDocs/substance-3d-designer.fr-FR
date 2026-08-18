---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Utilisez le nœud Noise Upscale 3 pour mettre à niveau les textures à l’aide d’algorithmes avancés basés sur le bruit afin de préserver les détails à des résolutions plus élevées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Amélioration du bruit 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Amélioration du bruit 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Amélioration du bruit 3

**Entrée :** *Filtres/Transformations*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Prend un bruit d’entrée procédural et le met à l’échelle jusqu’à une double résolution, en conservant les détails sans introduire trop de mosaïque. Utilise un masque défini par l’utilisateur pour fusionner le bruit au-dessus de son échelle d’origine.

Ce nœud est principalement destiné à l’optimisation des graphes lents qui utilisent des bruits intenses et importants. Cela vous permet d’utiliser des résolutions plus élevées sans ajouter trop de temps de calcul supplémentaire.

Voir également [Amélioration du bruit 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) et [Amélioration du bruit 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), qui, dans la plupart des cas, ont tendance à être légèrement meilleurs pour masquer les carreaux.

## Paramètres

### Entrées

* **Niveaux De Gris** : *Entrée En Niveaux De Gris*\
  Image Bruit cible.
* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

*Aucun paramètre.*

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise3ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
