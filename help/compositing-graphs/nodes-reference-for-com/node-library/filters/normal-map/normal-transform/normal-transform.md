---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation normale pour appliquer des transformations aux cartes de normales tout en conservant correctement les directions des vecteurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Transformation normale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## Transformation normale

**Entrée :** *Filtres/Mappage de normales*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Comme le nœud 2D de transformation atomique, cela permet la transformation de cartes normales sans rupture de l&#39;espace tangent. Au lieu de cela, il est recalculé à la volée, ce qui permet de toujours corriger les cartes normales.

## Paramètres

* **Matrix2x2** : *(Matrice de transformation) :*\
  Faites pivoter ou mettez à l’échelle l’entrée.
* **Décalage** : *-0.5 - 0.5*\
  Déplace ou traduit le résultat. Lorsque la commande Transformation est présente, le résultat peut être modifié en interagissant directement avec la zone de travail.
* **Format normal** : *DirectX, OpenGL*\
  Basculer entre différents Formats de map normaux (inverse la couche verte)

</td>
</tr>
</table>
