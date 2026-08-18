---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation non carrée pour appliquer des transformations à des textures non carrées avec une mise à l’échelle indépendante X et Y.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation non carrée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Transformation non carrée

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Transformation non carrée (niveaux de gris)

**Entrée :** *Filtres/Transformations*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Version sans carrés de [Transformation 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Détecte automatiquement les rapports non carrés et peut transformer les images carrées en zone de travail non carrée.

Assurez-vous de bien comprendre les [paramètres du graphique](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)pour tirer le meilleur parti de ce nœud, car vous devrez définir correctement certains paramètres :

* La taille de votre **graphique** doit être non carrée, sinon ce nœud n&#39;est pas nécessaire.
* Définissez la taille de sortie du **nœud** de transformation non carrée sur « *Relative au parent* ».
* Définissez le mode de mosaïque du **nœud** sur « *Aucun mosaïque* » si vous souhaitez uniquement transformer votre entrée en une seule position.

## Paramètres

* **Mode mosaïque** :*Automatique, manuel* Activez ou non les compensations automatiques non carrées.
* **Mosaïque** : *1 - 16* Uniquement accessible lorsque le mode Mosaïque est défini sur Manuel. Permet de modifier l’échelle de manière à éviter les mosaïques.
* **Décalage** : *0,0 - 1,0*\
  Déplace ou traduit le résultat. Double-cliquez sur le curseur pour entrer des valeurs négatives.
* **Rotation** : *0.0 - 1.0* Fait pivoter l’image d’entrée.
* **Rotation sécurisée (carré uniquement)** :*Faux/Vrai* s’accroche aux valeurs sécurisées pour conserver la netteté des pixels.
* **Couleur d&#39;arrière-plan** : *(Valeur de couleur)*Couleur d&#39;arrière-plan pour remplir l&#39;image. Visible uniquement lorsque le [mode Mosaïque dans les paramètres de base est défini sur « *Aucune mosaïque*« ](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md).

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
