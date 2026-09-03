---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: Apprenez à utiliser les variables itération et nombre dans les mappages FXM pour créer des modèles en boucle et des variations de procédure.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Itération et variable numérique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Itération et variable `$number`

![](iterate-and-number-variable.resources/iterate-and-number-variable-01.jpg)

Le nœud Itérer restituera aux nœuds connectés à la sortie de droite la durée spécifiée par la valeur Itérations.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="iterate-and-number-variable.resources/iterate-and-number-variable-02.png"/></div> | 1 itération : le motif gaussien est rendu une fois |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="iterate-and-number-variable.resources/iterate-and-number-variable-03.png"/></div> | 10 itérations : le motif gaussien est rendu 10 fois au même endroit |

Lors de l&#39;utilisation d&#39;un nœud Iterate, vous pouvez utiliser la variable `$number` pour obtenir la valeur d&#39;itération actuelle. `$number` est une valeur flottante et commence à 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/iterate-and-number-variable-04.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/iterate-and-number-variable-05.png){width="300px"}

</td>
</tr>
</table>

Cette fonction, définie dans le paramètre Décalage du motif, sera exécutée 10 fois, une fois pour chaque motif.

Le premier motif a une valeur `$number` égale à 0 et est ensuite rendu à la coordonnée (0, 0). Le deuxième motif a une valeur `$number` égale à 1 et est ensuite rendu à la coordonnée (0,1, 0) (1 x 0,1 = 0,1) et ainsi de suite pour les motifs suivants.
