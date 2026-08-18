---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: Utilisez le nœud Rotation des vecteurs normaux pour faire pivoter les vecteurs de texture normaux afin de régler l'éclairage de la surface et l'orientation des détails.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotation vectorielle normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Rotation vectorielle normale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## Rotation vectorielle normale

**Entrée :** *Filtres/Mappage de normales*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud utilitaire normal qui fait pivoter tous les vecteurs d&#39;une carte normale d&#39;entrée dans l&#39;espace tangent. Ne transforme pas réellement les pixels, mais modifie les valeurs qu’ils représentent. Il peut utiliser un mappage facultatif pour ajouter des rotations aléatoires à des facettes en niveaux de gris.

## Entrées

* **Normal** : *Entrée Couleur*\
  Mappage de base sur lequel effectuer la rotation. Obligatoire.
* **Map rotation (facultatif)** : *Entrée en niveaux de gris*\
  Courbe de transfert en niveaux de gris qui module l’intensité de rotation.

## Paramètres

* **Angle De Rotation** : *0,0 - 1,0*\
  Définit l&#39;angle de rotation de la texture normale
* **Format normal** : *DirectX, OpenGL*\
  Basculer entre différents Formats de map normaux (inverse la couche verte)

## Exemples

</td>
</tr>
</table>
