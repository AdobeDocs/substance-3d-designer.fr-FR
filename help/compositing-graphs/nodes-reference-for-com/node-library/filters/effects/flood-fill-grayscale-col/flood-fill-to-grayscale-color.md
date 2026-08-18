---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Flood Fill vers Couleurs en niveaux de gris pour remplir les régions connectées avec des couleurs en niveaux de gris afin de créer des motifs monochromes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill à GrayscaleColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# Flood Fill à Niveaux de gris/Couleur

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-grayscale.png){width="128px"}

![](../../../../../../assets/floodfill-to-color.png){width="128px"}

## Flood Fill à des niveaux de gris/couleurs aléatoires

**Entrée :** *Filtres/Effets*

**&#x200B;**&#x200B;Simple&#x200B;**&#x200B;**

</td>
<td style="border: 0;" valign="top">

## Description

Utilise les données du Flood Fill pour générer des nuances de niveaux de gris ou de valeurs chromatiques. Contrairement à [Flood Fill à Random Grayscale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), ces deux nœuds permettent un meilleur contrôle pour définir la variation et les tons exacts, avec un mappage d&#39;entrée supplémentaire pour déterminer la valeur de base à randomiser sur une base par cellule.

Il s&#39;agit d&#39;un système puissant qui donne à chaque cellule une valeur ou une couleur unique, tout en gardant le contrôle et en la basant sur une entrée prédéterminée.

## Paramètres

### Entrées

* **Flood Fill** : *Entrée de couleur*
* **Entrée Niveaux De Gris/Couleur** :*Entrée Niveaux De Gris/Couleur*

### Paramètres

* **Réglage de la luminance/couleur** : *-1.0 - 1.0* Définissez le biais ou la valeur de base pour le nœud. Lorsqu’une entrée Niveaux de gris ou Couleur est utilisée, elle est utilisée pour modifier cette valeur initiale comme point de départ.
* **Luminance/Couleur aléatoire** : *-1.0 - 1.0* Définissez le degré de variation.

</td>
</tr>
</table>
