---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Utilisez le nœud Lueur pour ajouter des effets de lueur aux textures afin de créer des états de matériau lumineux et émissifs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lueur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# Lueur

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## Lueur

**Entrée :** *Filtres/Effets*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Applique un effet de type « Lueur externe », comme dans d’autres logiciels de retouche d’images courants. Ajoute essentiellement un contour en dégradé de fondu autour de l’entrée.

Gardez à l’esprit qu’il ne s’agit pas d’une fonctionnalité prévue pour les images avec des couches Alpha, comme vous pourriez vous y attendre. Même la version en couleurs ne prévoit que des masques binaires, noir et blanc en entrée ; elle ne permet d’utiliser qu’une lueur colorée. Si vous recherchez une version qui fonctionne sur les images avec transparence, consultez [Shape Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez Lueur pour les entrées Couleur ou Lueur en niveaux de gris pour les entrées Niveaux de gris.

## Paramètres

* **Quantité de lueur** : *0.0 - 1.0* Opacité globale pour l’effet de lueur.
* **Quantité de suppression** : *seuil de 0 à 1,0* seuil pour savoir quand couper l&#39;effet de lueur. Utile pour les zones semi-transparentes.
* **Taille de la lueur** :*0.0 - 20.0* contrôle l’étendue de l’effet de lueur.
* **Couleur de rayonnement** : *(Valeur de couleur) (Version de couleur uniquement)*Définit la couleur de l’effet de rayonnement.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
