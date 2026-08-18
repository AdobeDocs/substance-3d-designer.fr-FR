---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit Worley 3D pour générer un bruit Worley en fonction de la position 3D afin de créer des effets de texture volumique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Worley Noise
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# 3D Worley Noise

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## 3D Worley Noise

**Entrée :** *Générateurs De Texture**/Bruits*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Il s’agit de l’un des bruits les plus polyvalents et avancés de la bibliothèque. Il génère un bruit Worley dans l’espace 3D, à partir d’un mappage de position d’entrée. Propose de nombreuses options qui la rendent beaucoup plus puissante que les bruits standard basés sur les [Cellules](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)ou la [distance](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md).

## Paramètres

* **Échelle** : *1 - 64*\
  Définissez l’échelle globale de l’effet.
* **Taille** :*0.0 - 1.0* Effectuez une mise à l’échelle non uniforme sur les axes X, Y et Z séparément.
* **Mode** : *Euclidean, Manhattan, Chebyshev, Minkowski\
  Modifiez la mesure de distance. Permet certains types de bruit très différents.*
* **Nombre de Minkowski** : *0,0 - 20,0* uniquement avec la mesure de distance de Minkowski. Fusionne entre différents types de mesures.
* **Style** : *F1, F2, F2-F1, Bordure, Couleur aléatoire* définissez les mathématiques de la combinaison de mesure. Permet de nombreuses autres combinaisons.
* **Largeur de la bordure** : *0.0 - 1.0* Lorsque le calcul de la combinaison de bordures est actif, contrôle la largeur de la bordure.
* **Arrondi** : *0.0 - 1.0* Disponible uniquement avec les modes F1, F2 et F2-F1. Définit la position médiane du niveau.
* **Inverser** : *Faux/Vrai*\
  Inverse le résultat.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>
