---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Tons directs gaussiens 1 pour générer des motifs de tons directs gaussiens afin de créer des variations et des détails de texture organique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Taches gaussiennes 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# Taches gaussiennes 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Taches gaussiennes 1 - Icône](gaussian-spots-1.resources/gaussian_spots_1.png "Taches gaussiennes 1 - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variation des <b>taches gaussiennes</b> lisses des bruits.\
Basé sur le nœud [bruit gaussien](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), avec des dégradés plus étroits.

Voir aussi : [Taches gaussiennes 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-2/gaussian-spots-2.md)

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
| <b>Échelle</b> <i>Entier</i> | Subdivision de la grille utilisée pour générer les éléments de bruit.    Plus la valeur est élevée, plus le nombre de carreaux dessinés est élevé et plus le bruit est dense. |
| <b>Désordre</b> <i>Flottant</i> | Déplace les ingrédients du bruit.    Cela permet d’animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flottant</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Désorganiser l&#39;anisotropie</b> <i>Flottant</i> | Contrôle l&#39;étendue des directions du displacement appliqué par le paramètre <b>Désordre</b>, où une valeur plus élevée entraîne une direction plus étroite et plus définie.    La direction est contrôlée par le paramètre <b>anisotropy angle de désordre</b>. |
| <b>Désorganiser l&#39;anisotropy angle</b> <i>Flottant</i> | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre <b>Disorder anisotropie</b> n&#39;est pas nul. |
| <b>Décalage de mosaïque</b> <i>Flottant 2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Taches gaussiennes 1 - Exemple 1](gaussian-spots-1.resources/gaussian_spots_1_1.png "Taches gaussiennes 1 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Taches gaussiennes 1 - Exemple 2](gaussian-spots-1.resources/noise_gaussian_spots_1_v2_speed0.6_aniso0.gif "Taches gaussiennes 1 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Taches gaussiennes 1 - Exemple 3](gaussian-spots-1.resources/noise_gaussian_spots_1_v2_speed0.6_aniso1.gif "Taches gaussiennes 1 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Taches gaussiennes 1 - Exemple 4](gaussian-spots-1.resources/noise_gaussian_spots_1_v2_speed0.3_aniso0.6.gif "Taches gaussiennes 1 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
