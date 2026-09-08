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
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Flood Fill à Niveaux de gris/Couleur

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-grayscale.png){width="128px"}

![](../../../../../../assets/floodfill-to-color.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Utilise les données du Flood Fill pour générer des nuances de niveaux de gris ou de valeurs chromatiques. Contrairement à [Flood Fill à Random Grayscale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), ces deux nœuds permettent un meilleur contrôle pour définir la variation et les tons exacts, avec un mappage d&#39;entrée supplémentaire pour déterminer la valeur de base à randomiser sur une base par cellule.

Il s&#39;agit d&#39;un système puissant qui donne à chaque cellule une valeur ou une couleur unique, tout en gardant le contrôle et en la basant sur une entrée prédéterminée.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Entrée couleur</i> |  |
| <b>Entrée Niveaux de gris/Couleur</b> <i>Entrée Niveaux de gris/Couleur</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Réglage de la Luminance/couleur</b> <i>-1.0 - 1.0</i> | Définissez le biais ou la valeur de base pour le nœud. Lorsqu’une entrée Niveaux de gris ou Couleur est utilisée, elle est utilisée pour modifier cette valeur initiale comme point de départ. |
| <b>Luminance/Couleur aléatoire</b> <i>-1.0 - 1.0</i> | Définissez le degré de variation. |
