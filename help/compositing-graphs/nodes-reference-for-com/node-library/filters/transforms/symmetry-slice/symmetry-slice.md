---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Utilisez le nœud de tranche de symétrie pour découper des textures le long des axes de symétrie afin de créer des motifs et des effets en miroir.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tranche de symétrie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Tranche de symétrie

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## Tranche de symétrie

**Entrée :** *Filtres/Transformations*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud d&#39;opération complexe de symétrie/mise en miroir. Permet une grande variété d&#39;opérations géométriques avec un contrôle total, mais nécessite quelques essais.

Comparé à [Miroir](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) et [Symétrie](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md), ce nœud dispose de beaucoup plus d&#39;options.

## Paramètres

* **Mode de symétrie** : *0 - 6* Choisissez une géométrie de symétrie/une ligne miroir. Les options sont Horizontal, Vertical, Diagonale Gauche-Droite, Diagonale Droite-Gauche, Inversion verticale, Angle et Angle diagonal.
* **Mode de transfert** : *0 - 6\
  Mode de fusion. Les options sont les suivantes :*
* **Fusionner** :*0.0 - 1.0* Fusionne l&#39;image d&#39;origine avec le résultat.
* **Symétrie** :*Faux/Vrai* inverse l&#39;origine, ce qui signifie que le côté d&#39;origine de l&#39;opération est inversé. La symétrie de gauche à droite par exemple se transforme de droite à gauche.
* **Inverser le côté2** : *Faux/Vrai*&#x200B;À utiliser uniquement lorsque le mode de symétrie est 5 ou 6. Inverser l’origine des angles.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
