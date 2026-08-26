---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-4.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit directionnel 4 pour générer des motifs de bruit directionnel de quatre octaves afin de créer des textures anisotropes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BRUIT DIRECTIONNEL 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# BRUIT DIRECTIONNEL 4

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Bruit directionnel 4 - Icône](../../../../../../assets/directional_noise_4.png "Bruit directionnel 4 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits de <b>Bruit directionnel</b>.

Voir aussi : [Bruit directionnel 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Bruit directionnel 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Bruit directionnel 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md)

</td>
</tr>
</table>

## Sorties

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris* | Le bruit généré est une image bitmap en niveaux de gris. |

## Paramètres

|  |  |
| --- | --- |
| Entier <b>Échelle</b> | Subdivision de la grille utilisée pour générer les carreaux de bruit.    Plus la valeur est élevée, plus le nombre de carreaux dessinés est important et plus le bruit est dense. |
| <b>Désordre</b> Flottant | Déplace les ingrédients du bruit.    Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> Flotter | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Désordre anisotropie</b> Flottant | Contrôle l&#39;étendue des directions du displacement appliqué par le paramètre <b>Désordre</b>, où une valeur plus élevée entraîne une direction plus étroite et plus définie.    La direction est contrôlée par le paramètre <b>Désorganiser l&#39;angle d&#39;anisotropie</b>. |
| <b>Modification de l&#39;angle d&#39;anisotropie</b> Flottant | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre « Disorder anisotropie » n&#39;est pas nul. |
| <b>Angle</b> Flottant | Angle utilisé pour définir la direction du bruit, en nombre de tours et à partir de l’horizontale vers la droite. |
| <b>Angle aléatoire</b> Flottant | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Décalage de mosaïque</b> Float2 | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> booléenne | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit directionnel 4 - Exemple 1](../../../../../../assets/directional_noise_4_1.png "Bruit directionnel 4 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit directionnel 4 - Exemple 2](../../../../../../assets/noise_directional_noise_4_v2_speed0.6_aniso0.gif "Bruit directionnel 4 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit directionnel 4 - Exemple 3](../../../../../../assets/noise_directional_noise_4_v2_speed0.6_aniso1.gif "Bruit directionnel 4 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit directionnel 4 - Exemple 4](../../../../../../assets/noise_directional_noise_4_v2_speed0.3_aniso0.6.gif "Bruit directionnel 4 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
