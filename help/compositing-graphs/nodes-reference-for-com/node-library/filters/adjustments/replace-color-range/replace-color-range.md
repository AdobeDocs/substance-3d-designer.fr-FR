---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Utilisez le nœud Remplacer la gamme de couleurs pour remplacer les couleurs d’une gamme spécifiée par de nouvelles couleurs pour la correction colorimétrique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Remplacer la gamme de couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# Remplacer la gamme de couleurs

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## Remplacer la gamme de couleurs

**Entrée :** *Filtres/Réglages*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Remplace la couleur source par la couleur cible, à l’aide de commandes supplémentaires. Peut, par exemple, être utilisé pour recolorer des parties d&#39;une carte d&#39;ID de matériau (bake).

Pour une version plus avancée, voir [Correspondance des couleurs.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

## Paramètres

* **Couleur source** : *(Valeur de couleur)*Couleur à remplacer.
* **Couleur cible** : *(Valeur de couleur)*Couleur à remplacer.
* **Plage source** : *0,0 -* 1,0\
  Plage ou tolérance de la source sélectionnée. Peut être augmenté pour que les couleurs voisines aient également une teinte décalée.
* **Seuil** : *0,0 - 1,0* Atténuation/contraste pour la plage. Réglez l’option Basse pour remplacer uniquement la couleur source, l’option Haute pour remplacer également les couleurs fusionnées dans la source.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
