---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit directionnel 1 pour générer des motifs de bruit directionnel afin de créer des variations de texture anisotropes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BRUIT DIRECTIONNEL 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 93824555c1b2d3de289eaf470e6f929ebf90dd71
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 1%

---


# BRUIT DIRECTIONNEL 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Bruit directionnel 1 - Icône](directional-noise-1.resources/directional_noise_1.png "Bruit directionnel 1 - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits de <b>Bruit directionnel</b>.

Voir aussi : [Bruit directionnel 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Bruit directionnel 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md), [Bruit directionnel 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| <b>Désorganiser l&#39;anisotropy angle</b> <i>Flottant</i> | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre « Disorder anisotropie » n&#39;est pas nul. |
| <b>Angle</b> <i>Flottant</i> | Angle utilisé pour définir la direction du bruit, en nombre de tours et à partir de l’horizontale vers la droite. |
| <b>Angle aléatoire</b> <i>Flottant</i> | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Décalage de mosaïque</b> <i>Flottant 2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 1](directional-noise-1.resources/directional_noise_1_1.png "Bruit directionnel 1 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 2](directional-noise-1.resources/noise_directional_noise_1_v2_speed0.6_aniso0.gif "Bruit directionnel 1 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 3](directional-noise-1.resources/noise_directional_noise_1_v2_speed0.6_aniso1.gif "Bruit directionnel 1 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 4](directional-noise-1.resources/noise_directional_noise_1_v2_speed0.3_aniso0.6.gif "Bruit directionnel 1 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
