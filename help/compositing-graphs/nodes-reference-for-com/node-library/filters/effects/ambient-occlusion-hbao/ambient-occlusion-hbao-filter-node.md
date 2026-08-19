---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Utilisez le nœud de filtrage HBAO d'Occlusion ambiante pour générer des cartes d'occlusion ambiante à l'aide d'algorithmes d'horizon pour un ombrage réaliste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusion ambiante (HBAO) (Nœud de filtre)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Occlusion ambiante (HBAO) (Nœud de filtre)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## Occlusion ambiante (HBAO)

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Prend une carte de hauteur comme entrée et génère une carte d&#39;Occlusion ambiante à partir de celle-ci. Il utilise l&#39;Occlusion ambiante basée sur l&#39;horizon, un algorithme initialement destiné à la génération d&#39;AO en temps réel dans l&#39;espace de l&#39;écran. Très utile pour créer des mappages AO procéduraux à partir des mappages de hauteur procéduraux.

Pour une autre version plus avancée mais plus lente d&#39;AO, voir [Occlusion ambiante (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

## Paramètres

* **Utiliser les unités universelles** : *Faux/Vrai* Active/désactive l’utilisation des unités universelles ou d’espace d’écran. Active des paramètres supplémentaires qui permettent un contrôle plus précis.
* **Profondeur d&#39;Height** : *0.0 - 1.0*&#x200B;à utiliser uniquement lorsque Unités universelles est défini sur Faux. Contrôle la mise à l’échelle globale.
* **Taille de la surface** : **0.0 - 1000.0**&#x200B;à utiliser uniquement lorsque Unités universelles est défini sur Vrai. Contrôle la mise à l’échelle globale.
* **Échelle d&#39;Height (cm)** : *0.0 - 1000.0*&#x200B;à utiliser uniquement lorsque Unités universelles est défini sur Vrai. Contrôle la mise à l’échelle globale.
* **Rayon** : *0,0 - 1,0* Contrôle la propagation de l&#39;AO.
* **Qualité** : *4 échantillons, 8 échantillons, 16 échantillons*\
  Définit le niveau de qualité en déterminant la quantité d&#39;échantillons utilisée pour le calcul.
* **Optimisation GPU** : *Faux/Vrai* Active l’optimisation GPU interne et accélère le traitement.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
