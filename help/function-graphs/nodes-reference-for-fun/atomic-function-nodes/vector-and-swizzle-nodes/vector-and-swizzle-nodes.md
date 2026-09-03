---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Utilisez les nœuds vectoriels et de redimensionnement dans les graphiques fonctionnels Substance 3D Designer pour manipuler les données et les composants vectoriels.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vecteur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# Nœuds vectoriels et de redimensionnement

Les nœuds vectoriels et de redimensionnement vous permettent respectivement de construire et de déconstruire des nœuds vectoriels à partir de et dans des composants distincts.Ils sont similaires à [Fusion RVBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) et [Fractionnement RVBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), mais également pour les graphiques de fonctions. Ils constituent également une méthode de conversion privilégiée entre les types de données vectorielles, car la [diffusion](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)n’est pas une option dans la plupart des cas.

## Nœuds vectoriels

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Les nœuds vectoriels vous permettent de combiner des vecteurs ou des éléments ayant moins de composants, en vecteurs ayant plus de composants. Il existe quelques règles ou limitations spécifiques pour les nœuds vectoriels :

* Les nœuds vectoriels ont **seulement deux entrées**, même si le vecteur résultant a plus de 2 composants.
* Les entrées vectorielles ne sont **pas limitées à un type** : elles peuvent prendre n&#39;importe quel composant inférieur comme entrée.
* L&#39;ordre de la sortie du résultat est déterminé par l&#39;**ordre des entrées**.

Cela signifie que les méthodes suivantes sont les mieux utilisées :

* Construisez un vecteur 4 de deux façons : connectez deux vecteurs à 2 composants ou connectez un vecteur à 1 composant et un vecteur à 3 composants.
* Si vous souhaitez construire un vecteur à 3 ou 4 composants à partir d’entiers simples ou de valeurs flottantes, vous devez d’abord effectuer au moins une combinaison de vecteurs 2 avant de pouvoir les combiner en un vecteur à 3 composants.

Réfléchissez bien à l&#39;ordre des connexions. L’ordre de connexion des entrées est illustré ci-dessous.

![](vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-01.png){width="200px"}

Exemple à gauche Connecte d&#39;abord un nombre entier(1), puis un nombre entier 3. Le résultat est comme ci-dessous

| Sortie | X | Y | Z | l |
| --- | --- | --- | --- | --- |
| Entrée 1 | 0 |  |  |  |
| Entrée 2 |  | 1 | 2 | 4 |

![](vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-02.png){width="200px"}

Exemple à gauche : permute les entrées du premier exemple, d’abord Entier 3, puis Entier(1).

| Sortie | X | Y | Z | l |
| --- | --- | --- | --- | --- |
| Entrée 1 | 1 | 2 | 4 |  |
| Entrée 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-03.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-04.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-05.png"/></div> |
| --- | --- | --- |
| **Vector Integer2** | **Vector Integer3** | **Vector Integer4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-06.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-07.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-08.png"/></div> |
| **Vector Float2** | **Vector Float3** | **Vector Float4** |

</td>
</tr>
</table>

## Nœuds de redimensionnement

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Les nœuds de swizzle déconstruisent ou fractionnent les composants des vecteurs à plusieurs composants, ce qui vous permet d’utiliser les composants X, Y, Z et W individuellement et de les permuter. Les règles et limitations suivantes s’appliquent :

* Les nœuds de redimensionnement n&#39;ont **qu&#39;une seule sortie**.
* Les nœuds de swizzle **prennent n&#39;importe quelle entrée** du type approprié (Int ou Flottant).

### Diviser les composants

L&#39;utilisation la plus courante de Swizzle est de l&#39;utiliser pour diviser des composants, tels que le freinage d&#39;un Entier 4 en 4 Entiers individuels. Les limitations signifient que vous aurez besoin de quatre nœuds de Swizzle integer distincts pour cela.

Tout autre type de séparation est également possible pour un Entier 4, tel que deux Entiers 2, ou un Entier et un Entier 3, toujours en gardant à l&#39;esprit que chaque résultat a besoin de son propre nœud.

### Permuter/Pivoter les composants

Comme son nom l’indique, Swizzle peut être utilisé pour modifier l’ordre des valeurs, voire les remplacer. Vous pouvez modifier l’ordre de X,Y,Z,W à W,Y,X,Z et vous pouvez modifier les valeurs de X,Y,Z,W à X,X,X,W, par exemple.

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-09.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-10.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-11.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-12.png"/></div> |
| --- | --- | --- | --- |
| **Swizzle integer** | **Piquer** **Entier 2** | **Piquer** **Entier 3** | **Piquer** **Entier 4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-13.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-14.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-15.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="vector-and-swizzle-nodes.resources/vector-and-swizzle-nodes-16.png"/></div> |
| **Piquer** **Flottant** | **Swizzle** **Flottant 2** | **Swizzle** **Flottant3** | **Swizzle** **Flottant4** |

</td>
</tr>
</table>
