---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Utilisez les nœuds vectoriels et de redimensionnement dans les graphes de fonction Substance 3D Designer pour manipuler les données et les composants vectoriels.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vecteur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# Nœuds vectoriels et de redimensionnement

Les nœuds vectoriels et de redimensionnement vous permettent respectivement de construire et de déconstruire des nœuds vectoriels à partir de et dans des composants distincts.Ils sont similaires à [Fusion RVBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) et [Fractionnement RVBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), mais pour les Graphes de fonction. Ils constituent également une méthode de conversion privilégiée entre les types de données vectorielles, car le [Converti](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)n’est pas une option dans la plupart des cas.

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
* Si vous souhaitez construire un vecteur à 3 ou 4 composants à partir d’un seul Entier ou d’un seul Flottant, vous devez d’abord effectuer au moins une combinaison Vecteur 2 avant de pouvoir les combiner en un vecteur à 3 composants.

Réfléchissez bien à l&#39;ordre des connexions. L’ordre de connexion des entrées est illustré ci-dessous.

![](../../../../assets/vector-int1.png){width="200px"}

Exemple à gauche Connecte d&#39;abord un Entier (1), puis un Entier (3). Le résultat est comme ci-dessous

| Sortie | X | Y | Z | l |
| --- | --- | --- | --- | --- |
| Entrée 1 | 0 |  |  |  |
| Entrée 2 |  | 1 | 2 | 4 |

![](../../../../assets/vector-int2.png){width="200px"}

Exemple à gauche : permute les entrées du premier exemple, le premier Entier 3, puis un Entier (1).

| Sortie | X | Y | Z | l |
| --- | --- | --- | --- | --- |
| Entrée 1 | 1 | 2 | 4 |  |
| Entrée 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-vectorint4.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-vectorint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-vectorint3.png"/></div> |
| --- | --- | --- |
| **Entier vectoriel2** | **Entier vectoriel3** | **Entier vectoriel4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-vectofloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-vectofloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-vectofloat4.png"/></div> |
| **Vecteur flottant 2** | **Vecteur flottant3** | **Vecteur flottant4** |

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

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-swizzleint1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-swizzleint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-swizzleint3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../assets/fn-vector-swizzleint4.png"/></div> |
| --- | --- | --- | --- |
| **Swizzle integer** | **Piquer** **Entier 2** | **Piquer** **Entier 3** | **Piquer** **Entier 4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-swizzlefloat1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-swizzlefloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-swizzlefloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="../../../../assets/fn-vector-swizzlefloat4.png"/></div> |
| **Piquer** **Flottant** | **Swizzle** **Flottant 2** | **Swizzle** **Flottant3** | **Swizzle** **Flottant4** |

</td>
</tr>
</table>
