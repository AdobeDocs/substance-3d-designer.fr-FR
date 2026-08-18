---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Utilisez le nœud Shape Glow pour ajouter des effets de lueur aux formes et aux textures afin de créer des effets visuels lumineux et atmosphériques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Glow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Shape Glow

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## Lueur de forme (niveaux de gris)

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Crée une lueur diffuse autour d’un masque d’entrée (pour la version en niveaux de gris) ou d’une forme avec une couche alpha (pour la version en couleurs). Comparé à [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), ce réglage est plus proche de celui d&#39;autres logiciels de retouche d&#39;images 2D, car il s&#39;agit d&#39;un effet plus complet avec plus de commandes.

## Paramètres

* **Mode** : *Souple, précis* Bascule entre deux modes de précision.
* **Largeur** : *-1.0 - 1.0* Contrôle l’étendue de la lueur.
* **Répartition** :*0,0 - 1,0* La coupure/le seuil de l’effet de flou donne l’impression que la lueur est solide près de la forme.
* **Opacité** : *0.0 - 1.0*\
  Opacité de fusion pour l’effet Rayonnement.
* **(Ombre) Couleur** : *(Valeur de couleur)*Teinte de couleur à appliquer à la lueur.
* **Couleur de masque** : *(Valeur de couleur) *(Version en niveaux de gris uniquement)**Couleur unie à utiliser pour la sortie mappée de transparence.
* **L&#39;entrée est prémultipliée** : *Faux/Vrai *(Version couleur uniquement)**Indique si l&#39;entrée doit être considérée comme prémultipliée.
* **Prémultiplier la sortie** : *Faux/Vrai* Indique si la sortie doit être prémultipliée.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
