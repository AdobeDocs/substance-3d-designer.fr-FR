---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou pour appliquer des effets de flou aux textures afin de lisser les détails et de créer des effets de flou.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 6%

---


# Flou

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icône de nœud de flou](blur.resources/blur-9.png){width="200px"}

**Entrée :** Noeuds atomiques

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud de flou effectue une opération « box-blur » : calcul de la moyenne des valeurs des pixels sur une distance définie, ce qui donne un aspect flou et flou. Il fournit l&#39;opération de flou la plus simple, la plus rapide et la plus basique disponible dans [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html).

Bien que le flou fonctionne bien pour les opérations rapides et simples, comme adoucir légèrement certains bords, dans tout scénario plus exigeant, [Blur HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) est un meilleur choix, sacrifiant les performances à la qualité.

</td>
</tr>
</table>

## Paramètres

* **Intensité** : 0-illimité\
  Définit l’intensité ou la distance du flou. Le nombre n’est pas limité, mais pour des valeurs élevées, l’image entière adopte une couleur moyennée.

L&#39;exemple ci-dessous montre le flou de ce nœud à gauche, par rapport à [Blur HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) à droite, lors de l&#39;utilisation de valeurs élevées (50 dans ce cas). Avec des valeurs d’environ 1-2, la différence n’est pas perceptible.

| Flou (atomique) | Flou HQ |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-hq.png"/></div> |
