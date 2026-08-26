---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: Utilisez le nœud Cellules 4 pour générer des motifs cellulaires avancés afin de créer des effets de texture organique et biologique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELLULES 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---


# CELLULES 4

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cellules 4 - Icône](../../../../../../assets/cells_4.png "Cellules 4 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits murés des <b>Cellules</b>.

Chaque cellule se voit attribuer une couleur plate, qui peut être aléatoire ou échantillonnée à partir d&#39;une image d&#39;entrée.

Voir aussi : [Cellules 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Cellules 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Cellules 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Entrées

</td>
<td style="border: 0;" valign="top">

### Sorties

</td>
<td style="border: 0;" valign="top">

### Paramètres

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Entrées

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris* |  |

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
| Entier <b>source de couleur</b> | Source de la couleur plate appliquée aux cellules :<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>Aléatoire :</i></b> utilisez une couleur aléatoire contrôlée par la valeur de départ aléatoire du nœud</li> <li data-preserve-html="true"><b><i>Pseudorandom :</i></b> utilisez une couleur aléatoire prédéfinie par une valeur distincte définie par l&#39;utilisateur</li> <li data-preserve-html="true"><b><i>Entrée d&#39;image :</i></b> utilisez la couleur échantillonnée à l&#39;emplacement de la cellule dans l&#39;image d&#39;entrée</li> </ul> |
| <b>Valeur de départ pseudo-aléatoire</b> Entier *disponible lorsque &#39;Color source&#39; est défini sur &#39;Pseudorandom&#39;* | Permet de modifier la valeur initiale de la couleur séparément de la valeur initiale du nœud. |
| <b>Expansion non carrée</b> booléenne | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cellules 4 - Exemple 1](../../../../../../assets/cells_4_1.png "Cellules 4 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Cellules 4 - Exemple 2](../../../../../../assets/noise_cells_4_v2_speed0.3_aniso0.6.gif "Cellules 4 - Exemple 2"){zoomable="yes"}

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
