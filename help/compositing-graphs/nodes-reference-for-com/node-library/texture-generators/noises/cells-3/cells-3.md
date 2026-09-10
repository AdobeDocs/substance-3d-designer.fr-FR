---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: Utilisez le nœud Cellules 3 pour générer des motifs cellulaires intermédiaires afin de créer des effets de texture organique et biologique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELLULES 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# CELLULES 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cellules 3 - Icône](cells-3.resources/cells_3.png "Cellules 3 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits murés des <b>Cellules</b>.

L&#39;intersection des disques produit des cellules avec des parois minces d&#39;une douceur inégale.

Voir aussi : [Cellules 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Cellules 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Cellules 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Échelle</b> <i>Nombre entier</i> | Subdivision de la grille utilisée pour générer les carreaux de bruit.    Plus la valeur est élevée, plus le nombre de carreaux dessinés est important et plus le bruit est dense. |
| <b>Dureté</b> <i>Flotter</i> | La définition des parois de cellule, où une valeur plus élevée donne des parois plus nettes et mieux définies. |
| <b>Inverser</b> <i>Booléen</i> | Inverse les valeurs de niveaux de gris de la sortie de l’image. |
| <b>Désordre</b> <i>Flotter</i> | Déplace les ingrédients du bruit.    Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flotter</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Désorganiser l&#39;anisotropie</b> <i>Flotter</i> | Contrôle l&#39;étendue des directions du displacement appliqué par le paramètre <b>Désordre</b>, où une valeur plus élevée entraîne une direction plus étroite et plus définie.    La direction est contrôlée par le paramètre <b>Désorganiser l&#39;angle d&#39;anisotropie</b>. |
| <b>Désorganiser l&#39;anisotropy angle</b> <i>Flotter</i> | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre « Disorder anisotropie » n&#39;est pas nul. |
| <b>Taille du motif</b> <i>Float2</i> | Multiplicateur de la taille d&#39;un disque dispersé dans sa cellule, où 1,0 correspond à l&#39;étendue complète de la cellule. |
| <b>Échelle du motif</b> <i>Flotter</i> | Multiplicateur pour la <b>taille du motif</b>, où 1,0 correspond à la taille réelle. |
| <b>Angle</b> <i>Flotter</i> | Angle utilisé pour définir la direction des disques, en nombre de tours et à partir de l&#39;horizontale droite. |
| <b>Angle aléatoire</b> <i>Flotter</i> | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Décalage de mosaïque</b> <i>Float2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cellules 3 - Exemple 1](cells-3.resources/cells_3_1.png "Cellules 3 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Cellules 3 - Exemple 2](cells-3.resources/noise_cells_3_v2_speed0.6_aniso0.gif "Cellules 3 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cellules 3 - Exemple 3](cells-3.resources/noise_cells_3_v2_speed0.6_aniso1.gif "Cellules 3 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Cellules 3 - Exemple 4](cells-3.resources/noise_cells_3_v2_speed0.3_aniso0.6.gif "Cellules 3 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
