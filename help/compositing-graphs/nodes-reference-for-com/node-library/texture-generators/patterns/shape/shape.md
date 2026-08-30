---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Utilisez le nœud Forme pour générer des formes géométriques de base afin de créer des motifs et des textures dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# Forme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape.resources/shape-2.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère diverses formes procédurales, avec des options pour modifier les formes de base. Les formes sont toujours parfaitement interpolées et de haute précision.

Malgré sa simplicité, il s&#39;agit d&#39;un nœud très utile : c&#39;est la pierre angulaire de la plupart des générations de Heightmap procédurales ! En combinant des formes simples avec des nœuds de transformation, vous pouvez créer une forme Heightmap entièrement procédurale, beaucoup plus précise qu’une image bitmap.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mosaïque</b> <i>1 - 16</i> | Définit le nombre de fois où le résultat doit se produire. |
| <b>Motif</b> <i>Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Graduation, Ondes, Demi-cloche, Cloche striée, Croissant, Capsule, Cône, Hémisphère</i> | Sélectionne la forme de motif à utiliser. |
| <b>Spécifique Au Motif</b> <i>0.0 - 1.0</i> | Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné. |
| <b>Échelle</b> <i>0.0 - 1.0</i> | Met à l’échelle toute la forme. |
| <b>Taille</b> <i>0.0 - 1.0</i> | Permet une mise à l’échelle non uniforme sur l’axe X ou Y. |
| <b>Angle</b> <i>0.0 - 1.0</i> | Fait pivoter la forme entière. |
| <b>Rotation 45°</b> <i>Faux/Vrai</i> | Permet une rotation à 45 degrés prédéfinis. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Permet la compensation de la courbure et de l’étirement avec des proportions non carrées. |
| <b>Répétition Non Carrée</b> <i>Faux/Vrai</i> | Lorsque l’Extension non carrée est activée, la forme est mosaïque sans être écrasée. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape.resources/shape-ex.gif" />
        </td>
    </tr>
</table>
