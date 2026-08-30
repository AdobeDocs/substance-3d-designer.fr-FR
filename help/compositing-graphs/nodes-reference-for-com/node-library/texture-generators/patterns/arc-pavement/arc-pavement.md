---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Utilisez le nœud Chaussée en arc pour générer des motifs de chaussée en forme d'arc afin de créer des textures de route et de tracé courbes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Chaussée Arc
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 11%

---


# Chaussée Arc

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](arc-pavement.resources/arcpavement-ex.png)

<b>Entrée :</b> Générateurs de textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un motif de pavage en arc de Paris. Cet effet ne peut pas être obtenu avec le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)standard ou le [Mosaïque Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md), d&#39;où ce nœud dédié.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle</b> <i>1 - 8</i> | Définit l’échelle/la répétition globale. |
| <b>Quantité du motif</b> <i>1 - 32</i> | Définit la quantité de briques utilisées dans chaque arc. |
| <b>Quantité aléatoire du motif</b> <i>0.0 - 1.0</i> | Rend aléatoire la quantité de briques dans chaque arc. A pour effet supplémentaire de donner aux briques différentes échelles. |
| <b>Quantité minimale du motif</b> <i>1 - 10</i> | Contrôle le nombre minimal de briques lors de la sélection aléatoire des arcs. |
| <b>Quantité D&#39;Arcs</b> <i>0 - 20</i> | Définit la quantité d’arcs empilés verticalement. Modifie l’height de la brique. |
| <b>Motif</b> <i>Image d&#39;entrée, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Graduations, Ondes, Demi-cloche, Cloche striée, Croissant, Capsule, Cône, </i> | Sélectionne la forme de motif à utiliser. |
| <b>Filtrage d&#39;Image d&#39;entrée</b> <i>Bilinéaire + Mipmaps, Bilinéaire, Nearest</i> |  |
| <b>Échelle du motif</b> <i>0.0 - 1.0</i> | Définit l’échelle de chaque mosaïque. |
| <b>Largeur du motif</b> <i>0.0 - 1.0</i> | Définit la largeur de chaque carreau. |
| <b>Height du motif</b> <i>0.0 - 1.0</i> | Définit l’height de chaque mosaïque. |
| <b>Largeur aléatoire du motif</b> <i>0.0 - 1.0</i> | Aléatoire la largeur des carreaux. |
| <b>Aléatoire de l&#39;Height du motif</b> <i>0.0 - 1.0</i> | Aléatoire de l’height de la vignette. |
| <b>Largeur aléatoire globale du motif</b> <i>0.0 - 1.0</i> | Aléatoire la largeur des carreaux, sans créer d’espaces plus grands entre eux. |
| <b>Diminution de l&#39;Height du motif</b> <i>0.0 - 1.0</i> | Contrôle l’écrasement de l’height des carreaux aux extrémités de chaque arc. |
| <b>Color Random</b> <i>0.0 - 1.0</i> | Aléatoire des couleurs des carreaux. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Permet la compensation de la courbure et de l’étirement avec des proportions non carrées. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="arc-pavement.resources/arcpavement-ex.png" />
        </td>
    </tr>
</table>
