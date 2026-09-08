---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Itération et variable $number

![](../../../../assets/iterate-1.jpg)

Le nœud Itérer restituera aux nœuds connectés à la sortie de droite la durée spécifiée par la valeur Itérations.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1 itération : le motif gaussien est rendu une fois |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10 itérations : le motif gaussien est rendu 10 fois au même endroit |

Lors de l&#39;utilisation d&#39;un nœud Iterate, vous pouvez utiliser la variable $number pour obtenir la valeur d&#39;itération courante. $number est une valeur flottante commençant à 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Cette fonction, définie dans le paramètre Décalage du motif, sera exécutée 10 fois, une fois pour chaque motif.

Le premier motif a une valeur $number égale à 0 et est ensuite rendu à la coordonnée (0, 0). Le deuxième motif a une valeur $number égale à 1 et est ensuite rendu à la coordonnée (0,1, 0) (1 x 0,1 = 0,1) et ainsi de suite pour les motifs suivants.

Exemple de téléchargement : [itérer\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)
