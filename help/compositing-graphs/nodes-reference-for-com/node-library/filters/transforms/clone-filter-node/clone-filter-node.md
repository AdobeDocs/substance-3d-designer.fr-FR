---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Utilisez le nœud de filtre Dupliquer pour dupliquer et décaler des zones de texture afin de créer des motifs et des effets de mosaïque continus.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cloner (nœud de filtre)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Cloner (nœud de filtre)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

## Cloner

**Entrée :** *Filtres/Transformations*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Clone l’image d’entrée une fois à un emplacement spécifié. Peut fonctionner comme un outil de « tampon de duplication » brut.

Nécessite un certain soin pour obtenir les résultats escomptés :

* Idéalement, l’image d’entrée doit avoir une couche alpha (comme une décalcomanie), puisque la fusion est une copie directe.
* Le masque étant défini par défaut sur le noir, une valeur de niveaux de gris blanc uniforme doit au moins être utilisée pour visualiser les résultats.
* Le décalage se découpe facilement en dehors de l’image. Utilisez donc des valeurs faibles.

## Paramètres

### Entrées

* **Source** : *Entrée couleur*\
  Image à dupliquer. Important : idéalement, l’image doit avoir une couche alpha !
* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud. Par défaut, c’est le noir !

### Paramètres

* **Décalage** : *-*\
  Déplace ou traduit le résultat. Positif correspond à Gauche et Haut, Négatif à Droite et Bas. Utilisez de petites valeurs, 1,0 et plus le déplace en dehors de l’image !
* **Masque de flou** : *0.0 - 10.0\
  Appliquez un filtre de flou au masque pour adoucir les contours.*

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/clone-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
