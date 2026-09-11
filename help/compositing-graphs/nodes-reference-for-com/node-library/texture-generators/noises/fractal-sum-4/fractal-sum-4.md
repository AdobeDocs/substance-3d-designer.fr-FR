---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-4.html"
breadcrumb-title: ''
description: Utilisez le nœud Somme fractale 4 pour générer un bruit fractal de quatre octaves afin de créer des textures organiques détaillées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SOMME FRACTALE 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# SOMME FRACTALE 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Somme fractale 4 - Icône](fractal-sum-4.resources/fractal_sum_4.png "Somme fractale 4 - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits de <b>Somme fractale</b>.

Voir aussi : [Somme fractale de base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md), [Somme fractale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Somme fractale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Somme fractale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est un bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Désordre</b> <i>Flottant</i> | Déplace les ingrédients du bruit.    Cela permet d’animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flottant</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Somme fractale 4 - Exemple 1](fractal-sum-4.resources/fractal_sum_4_1.png "Somme fractale 4 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Somme fractale 4 - Exemple 2](fractal-sum-4.resources/noise_fractal_sum_4_v2_speed0.6_aniso0.gif "Somme fractale 4 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>
