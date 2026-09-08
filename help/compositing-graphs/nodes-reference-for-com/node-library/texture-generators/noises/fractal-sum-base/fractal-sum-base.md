---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: Utilisez le nœud Base de Somme fractale pour générer des motifs de bruit fractal de base afin de créer des textures organiques complexes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: base de somme fractale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# base de somme fractale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Base de Sommes fractale - Icône](../../../../../../assets/fractal_sum_base.png "Base de Sommes fractale - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Un bruit fractal personnalisable avec une plage et un équilibre d&#39;octaves réglables.

Les bruits de la famille <b>Somme fractale</b> sont tous basés sur ce nœud.

Voir aussi : [Somme fractale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Somme fractale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Somme fractale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Somme fractale 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est une image bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Rugosité</b> <i>Flotter</i> | L&#39;équilibre des octaves de bruit.    Une valeur élevée rend les octaves de fréquence plus visibles. |
| <b>Min. niveau</b> <i>Nombre entier</i> | Octave minimale utilisée dans le bruit.    Plus la valeur est élevée, plus la fréquence du bruit est élevée. |
| <b>Max. niveau</b> <i>Nombre entier</i> | Octave maximale utilisée dans le bruit.    Plus la valeur est élevée, plus la fréquence du bruit est élevée. |
| <b>Désordre</b> <i>Flotter</i> | Déplace les ingrédients du bruit.    Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flotter</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Contraste</b> <i>Flotter</i> | Contraste du résultat final. |
| <b>Opacité globale</b> <i>Flotter</i> | Opacité des octaves de bruit ajoutées ensemble dans le résultat final.    Une valeur élevée peut entraîner la gravure de zones en blanc. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Base de Sommes fractale - Exemple 1](../../../../../../assets/fractal_sum_base_1.png "Base de Sommes fractale - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Base de Sommes fractale - Exemple 2](../../../../../../assets/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "Base de Sommes fractale - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>
