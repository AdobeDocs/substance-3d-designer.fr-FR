---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Utilisez le nœud de filtrage Biseau pour créer des biseaux sur les formes et les motifs afin d’ajouter de la profondeur et des dimensions.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Biseau (nœud de filtre)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# Biseau (nœud de filtre)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## Biseau

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Applique un effet de biseautage des bords à une image en hauteur en niveaux de gris en entrée. Renvoie la valeur Heightmap biseautée et la valeur Normalmap en fonction de cette valeur Heightmap.

Il s’agit d’un nœud utile pour appliquer des profils de courbe exacts sur une carte de hauteur de base binaire (noir/blanc à fort contraste).

## Paramètres

### Entrées

* **entrée** : *entrée en niveaux de gris*\
  Mappage de hauteur à convertir.
* **Courbe Personnalisée** : *Entrée En Niveaux De Gris*\
  Dégradé qui détermine la courbe/pente exacte. Idéalement, il s&#39;agit d&#39;un nœud linéaire en dégradé, sur lequel vous pouvez effectuer tout type de réglage tel que les [niveaux](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) ou les [courbes](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md). Cette option est uniquement active lorsque l’option « Utiliser la courbe personnalisée » a la valeur True.

### Paramètres

* **Distance** : *-1,0 - 1,0* Jusqu’à quelle distance l’effet de biseau doit atteindre.
* **Type d&#39;angle** :*arrondi, Angular* l&#39;arrondi ou la droite du profil de biseautage.
* **Lissage** :*0.0 - 5.0* Le lissage supplémentaire (flou) à effectuer après le biseau.
* **Utiliser un flou non uniforme** : *Faux/Vrai* Indiquer si le lissage doit être effectué de manière non uniforme.
* **Utiliser la courbe personnalisée** : *Faux/Vrai* Active/désactive l&#39;utilisation de votre propre courbe d&#39;height personnalisée. Voir ci-dessus pour plus d’informations.
* **Intensité normale** : *0.0 - 50.0* Intensité de la carte des normales générée.
* **Format normal** : *DirectX, OpenGL*\
  Basculer entre différents formats de mappage normal (inverse la couche verte).

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
