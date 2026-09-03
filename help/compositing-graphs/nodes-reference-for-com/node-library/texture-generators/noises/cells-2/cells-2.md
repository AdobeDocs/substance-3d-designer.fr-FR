---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-2.html"
breadcrumb-title: ''
description: Utilisez le nœud Cellules 2 pour générer des motifs cellulaires intermédiaires afin de créer des effets de texture organique et biologique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELLULES 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# CELLULES 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cellules 2 - Icône](cells-2.resources/cells-2-01.png "Cellules 2 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits murés des <b>Cellules</b>.

Masque binaire des cellules avec un thickness mural réglable.

Voir aussi : [Cellules 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Cellules 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md), [Cellules 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Largeur du contour</b> <i>Flotter</i> | Ajuste le thickness des parois entre les cellules, en tant que rapport de la grille. (C&#39;est-à-dire non dépendant de la résolution) |
| <b>Inverser</b> <i>Booléen</i> | Bascule entre les noirs et les blancs dans l’image de sortie. |
| <b>Désordre</b> <i>Flotter</i> | Déplace les ingrédients du bruit.    Cela permet d’animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flotter</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cellules 2 - Exemple 1](cells-2.resources/cells-2-02.png "Cellules 2 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Cellules 2 - Exemple 2](cells-2.resources/cells-2-03.gif "Cellules 2 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>
