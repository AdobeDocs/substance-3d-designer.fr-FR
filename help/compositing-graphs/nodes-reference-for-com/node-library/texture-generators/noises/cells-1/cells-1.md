---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Cellules 1 pour générer des motifs cellulaires de base afin de créer des effets de texture organique et biologique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELLULES 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# CELLULES 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cellules 1 - Icône](cells-1.resources/cells_1.png "Cellules 1 - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une variante des bruits murés de <b>Cellules</b>.

Les motifs sélectionnés par l’utilisateur sont dispersés et incrustés à l’aide d’un mode de fusion Max.

Voir aussi : [Cellules 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Cellules 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md), [Cellules 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Motif</b> <i>Entier</i> | Forme de base dispersée dans l’image générée. |
| <b>Taille du motif</b> <i>Flottant 2</i> | Multiplicateur de la taille d’un motif diffusé dans sa cellule, où 1,0 correspond à l’étendue complète de la cellule. |
| <b>Échelle du motif</b> <i>Flottant</i> | Multiplicateur pour la <b>taille du motif</b>, où 1,0 correspond à la taille réelle. |
| <b>Luminance aléatoire</b> <i>Flottant</i> | Plage de luminances soustraite aléatoirement des cellules, où 1 représente la plage complète. |
| <b>Angle</b> <i>Flottant</i> | Angle utilisé pour définir la direction des cellules, en nombre de tours et en partant de l’horizontale vers la droite. |
| <b>Angle aléatoire</b> <i>Flottant</i> | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Décalage de mosaïque</b> <i>Flottant 2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cellules 1 - Exemple 1](cells-1.resources/cells_1_1.png "Cellules 1 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Cellules 1 - Exemple 2](cells-1.resources/noise_cells_1_v2_speed0.3_aniso0.3.gif "Cellules 1 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cellules 1 - Exemple 3](cells-1.resources/noise_cells_1_v2_speed0.5_aniso0.6.gif "Cellules 1 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Cellules 1 - Exemple 4](cells-1.resources/noise_cells_1_v2_speed0.3_aniso0.6.gif "Cellules 1 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
