---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: Utilisez le nœud Mappeur de formes pour mapper des formes sur des textures avec des transformations et un positionnement personnalisables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappeur de formes
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Mappeur de formes

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Mappeur de formes - Icône](shape-mapper.resources/shape_mapper.png "Mappeur de formes - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Projette une image d&#39;entrée le long d’un cercle ou d’un polygone.

La projection déforme l’image pour qu’elle suive le contour de la forme et l’ajuste exactement à un nombre spécifié de fois sans espaces.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Niveaux de gris</i> | Motif à placer le long de la forme. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Résultat de la projection du motif le long de la forme, sous forme d’image bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Forme</b> <i>Entier</i> | Définit le type de forme le long de laquelle les motifs doivent être placés :<ul data-preserve-html="true"> <li data-preserve-html="true">Cercle</li> <li data-preserve-html="true">Polygone</li> </ul> |
| <b>Quantité du motif</b> <i>Entier</i> | Quantité de motifs placés le long de la forme sélectionnée. |
| <b>Lier les segments avec la quantité de motif</b> <i>Booléen</i>   *Disponible lorsque « Forme » est défini sur « Polygone »* | Utilisez la <b>quantité de motif</b> comme nombre de <b>segments</b>.   Cela empêche les motifs de s’enrouler autour des coins, garantissant ainsi un aspect droit et cohérent. |
| <b>Segments</b> <i>Entier</i>   *Disponible lorsque &#39;Shape&#39; est défini sur &#39;Polygon&#39; et &#39;Link segments with pattern amount&#39; est défini sur &#39;False&#39;* | Nombre de segments du polygone le long desquels les motifs sont placés.   Les segments sont *de taille régulière* et tous les vertex sont *équidistants du centre*, de sorte que l&#39;augmentation de la quantité de segments fait converger le polygone vers un cercle. |
| <b>Rayon</b> <i>Flottant</i> | Multiplicateur du rayon de la forme, où 1,0 correspond à la moitié de la longueur du côté le plus court de l’image. |
| <b>Largeur</b> <i>Flottant</i> | Multiplicateur de la largeur des motifs le long de la forme, où 1,0 correspond à la moitié de la longueur du côté le plus court de l’image. |
| <b>Rotation</b> <i>Flottant</i> | Spécifie le degré de rotation appliqué à la forme, en nombre de tours dans le sens des aiguilles d’une montre à partir de la droite horizontale. |
| <b>Symétrie un sur deux</b> <i>Booléen</i> | Retournez une forme sur deux verticalement. |
| <b>Mode de filtrage</b> <i>Entier</i> | La méthode de filtrage appliquée aux motifs placés le long de la forme:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Au plus proche :</i> applique la valeur du pixel projeté le plus proche telle quelle, ce qui donne un aspect plus net mais crénelé.</li> <li data-preserve-html="true"><i>Bilinéaire :</i> applique un filtre bilinéaire pour interpoler le pixel projeté avec ses voisins, pour un aspect plus lisse mais plus flou.</li> </ul> |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la forme générée reste carrée et étend la génération d’image aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
