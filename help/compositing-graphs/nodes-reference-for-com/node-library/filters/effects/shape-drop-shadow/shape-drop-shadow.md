---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Utilisez le nœud Ombre portée de forme pour ajouter des effets d’ombre portée aux formes afin de créer une profondeur et une dimension dans les textures.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ombre portée de la forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Ombre portée de la forme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## Ombre portée de la forme (niveaux de gris)

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Applique l’effet bien connu « Ombre portée » d’un autre logiciel de traitement d’image 2D, sur un masque noir et blanc d’entrée (pour la version en niveaux de gris) ou sur une image avec transparence (pour la version en couleurs).

Il diffère de l&#39;effet [Ombres](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) en ce sens qu&#39;il renvoie des images avec une transparence totale appliquée, ce qui donne un effet plus complet similaire à ce que vous attendriez dans d&#39;autres logiciels.

## Paramètres

* **Angle** : *0,0 - 1,0* Angle d’incidence de la (fausse) lumière.
* **Distance** : *-0.5 - 0.5* Distance à laquelle l&#39;ombre doit s&#39;abaisser/s&#39;éloigne de la forme.
* **Taille** :*0,0 - 1,0* contrôle le flou/les zones floues de l’ombre.
* **Répartition** :*0,0 - 1,0* La coupure/le seuil de l’effet de flou éloigne davantage l’ombre.
* **Opacité** : *0.0 - 1.0*\
  Opacité de fusion pour l’effet d’ombre.
* **(Ombre) Couleur** : *(Valeur de couleur)*Teinte de couleur à appliquer à l&#39;ombre.
* **Couleur de masque** : *(Valeur de couleur) *(Version en niveaux de gris uniquement)**Couleur unie à utiliser pour la sortie mappée de transparence.
* **L&#39;entrée est prémultipliée** : *Faux/Vrai *(Version couleur uniquement)**Indique si l&#39;entrée doit être considérée comme prémultipliée.
* **Prémultiplier la sortie** : *Faux/Vrai* Indique si la sortie doit être prémultipliée.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
