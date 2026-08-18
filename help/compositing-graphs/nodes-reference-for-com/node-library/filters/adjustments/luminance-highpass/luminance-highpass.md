---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Utilisez le nœud Passe-haut de luminance pour extraire les détails de luminance haute fréquence des textures afin d'améliorer les détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Passe-haut de luminance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# Passe-haut de luminance

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

## Passe-haut de luminance

**Entrée :** *Filtres/Réglages*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Annule les informations d&#39;éclairage en effectuant un [passe-haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) sur la valeur de luminance de l&#39;entrée. Utile pour corriger les textures photographiées avec des informations d’éclairage. Peut être combiné dans [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) avec plusieurs passes pour supprimer différentes fréquences des détails d&#39;éclairage.

Préserve mieux les couleurs que l&#39;[éclairage et annule les basses fréquences](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md).

## Paramètres

* **Rayon** : *0,0 - 64,0* Rayon de l’effet passe-haut. Un rayon plus petit annule un éclairage plus petit et s’ajuste aux images en entrée.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/luminance-highpass-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
