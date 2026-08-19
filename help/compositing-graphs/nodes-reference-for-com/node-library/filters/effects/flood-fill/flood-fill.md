---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: Utilisez le nœud Flood Fill pour remplir des régions connectées de couleur similaire afin de créer des masques et des effets de traitement de texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill.png){width="128px"}

## Flood Fill

**Entrée :** *Filtres/Effets*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Flood Fill fait partie d’un ensemble avancé d’effets qui vous permettent d’ajouter beaucoup plus de variation à une texture de mosaïque binaire de base. Il n’est pas destiné à être utilisé seul : il s’agit plutôt d’un point de départ pour d’autres effets Flood Fill. Cette division des données permet un flux de production plus dynamique, plus optimisé et moins destructeur.

Les autres effets Flood Fill sont [Flood Fill au dégradé](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), [Flood Fill à la couleur/aux niveaux de gris](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md), [Flood Fill à la nuance de gris aléatoire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), [Flood Fill à la couleur aléatoire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md), [Flood Fill à la taille de la BBox](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md), [Flood Fill à la position](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md), [Mappeur Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md) et [Flood Fill à l’index](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)

>[!WARNING]
>
> Le mappage d’entrée doit être adapté au Flood Fill pour fonctionner. Idéalement, il s’agit d’une carte binaire (noir/blanc uniquement, pas de niveaux de gris) où chaque carreau est séparé des autres lignes par une bordure entièrement noire (0,0,0) pour chaque pixel. Le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) est un exemple parfait pour cela.
> 
> Des problèmes surviennent si les carreaux ne sont pas séparés par des pixels noirs entiers, généralement lorsque des valeurs d’inclinaison en niveaux de gris sont utilisées. Vous pouvez identifier cela par un manque global de valeurs rouges dans le résultat, et peut-être par des lignes d&#39;artefact étranges. Dans ce cas, ajustez le contraste sur la carte d’entrée ou éteignez la carte d’entrée. Assurez-vous de modifier le paramètre de compromis Sécurité/Vitesse pour voir si quelque chose s’améliore.

## Paramètres

* **Compromis sécurité/vitesse** : *formes simples ou petites, formes complexes ou grandes, pas de mode d&#39;échec.*Réglez le mode de calcul pour qu&#39;il corresponde le mieux aux formes d&#39;entrée. Permet d’obtenir des résultats beaucoup plus précis si le mode correct est choisi.
* **Options avancées** : *Afficher les paramètres avancés et Sortie/Masquer les paramètres avancés et la sortie*
* **Remplacer le compromis sécurité/vitesse** : *-1 - 100* visible uniquement avec les options avancées activées. Permet de remplacer les fonctions internes. Très avancé, permet de créer ses propres effets ou de déboguer.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/flood-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/flood-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

Bons et mauvais exemples de résultats de Flood Fill.

</td>
</tr>
</table>
