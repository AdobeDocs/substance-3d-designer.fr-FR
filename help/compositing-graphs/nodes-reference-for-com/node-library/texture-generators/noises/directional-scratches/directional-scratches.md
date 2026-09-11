---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: Utilisez le nœud Scratches directionnels pour créer des motifs de rayures directionnels afin d’ajouter des effets d’usure et d’endommagement aux matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rayures directionnelles
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1241ebb4d1e67c9ed9d86285a6397ddc335e0f37
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Rayures directionnelles

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rayures directionnelles - Icône](directional-scratches.resources/directional_scratches.png "Rayures directionnelles - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Diffusion aléatoire de motifs de rayures avec un angle et une taille réglables.

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
| <b>Angle</b> <i>Flottant</i> | Angle utilisé pour définir la direction des rayures, en nombre de tours et en partant de l’horizontale vers la droite. |
| <b>Angle aléatoire</b> <i>Flottant</i> | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Quantité du motif</b> <i>Flottant</i> | Multiplicateur de la quantité de motifs de travail diffusés. |
| <b>Taille du motif</b> <i>Flottant 2</i> | Taille du cadre de sélection du motif de travail.    La valeur Y contrôle la longueur maximale des rayures. |
| <b>Taille aléatoire du motif</b> <i>Flottant 2</i> | Multiplicateur de la réduction aléatoire d’échelle appliquée aux rayures.    La valeur Y l’applique à la longueur des rayures. |
| <b>Décalage de mosaïque</b> <i>Flottant 2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 1](directional-scratches.resources/directional_scratches_1.png "Égratignures directionnelles - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 2](directional-scratches.resources/noise-directional-scratches-speed0.3-aniso0.gif "Égratignures directionnelles - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 3](directional-scratches.resources/noise-directional-scratches-speed0.3-aniso0.6.gif "Égratignures directionnelles - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 4](directional-scratches.resources/noise-directional-scrat-1.gif "Égratignures directionnelles - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 5](directional-scratches.resources/noise-directional-scrat-2.gif "Égratignures directionnelles - Exemple 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
