---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ''
description: Utilisez le nœud Dégradé (dynamique) pour créer des dégradés dynamiques qui peuvent être contrôlés par des paramètres et des valeurs d’entrée.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé (dynamique)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 9%

---


# Dégradé (dynamique)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : Dégradé dynamique](../../../../assets/comp_dyngradient_1.png "Nœud atomique : Dégradé dynamique"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Remappe les valeurs de niveaux de gris d’une image, en utilisant un dégradé fourni par une ligne ou une colonne de pixels d’une autre image.

Elle constitue une légère alternative au nœud de dégradé, mais contrairement à ce dernier, les dégradés ne sont pas définis en interne, mais proviennent d’une entrée externe.

</td>
</tr>
</table>

Cela permet principalement d&#39;éviter le problème où les paramètres ne peuvent pas être exposés, car les paramètres de couleur sont déplacés en dehors du nœud. C&#39;est ce qui la rend « dynamique ».

Bien que le dégradé (dynamique) ne soit pas un nœud difficile à utiliser seul, ses cas d&#39;utilisation sont un peu plus avancés : la plupart des utilisations standard peuvent être couvertes par le nœud de dégradé régulier.

Ce nœud entre en jeu lorsque vous êtes trop limité par le système clé de l’éditeur de dégradé et souhaitez que les couleurs et les positions du dégradé soient déterminées par d’autres entrées, paramètres et parties de votre graphique.

Vous pouvez également utiliser le curseur Position de l’entrée de dégradé pour alterner entre plusieurs dégradés stockés dans une seule entrée Dégradé.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Paramètres

</td>
<td style="border: 0;" valign="top">

### Connecteurs d’entrée

</td>
<td style="border: 0;" valign="top">

### Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Adressage de dégradé</b> *Booléen* | Définit si le dégradé se répète (carreaux) ou se bloque.   Ce paramètre détermine le mode de traitement des pixels HDR hors plage de [0, 1] de l’entrée en niveaux de gris : bridé ou plié jusqu’à [0, 1]. |
| <b>Orientation du dégradé</b> *Nombre entier* | Définit l&#39;axe le long duquel le &#39;Dégradé d&#39;entrée&#39; doit être échantillonné :<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Horizontal :</i> échantillonnez une ligne de pixels sur l&#39;axe X.</li> <li data-preserve-html="true"><i>Vertical :</i> échantillonnez une colonne de pixels sur l&#39;axe Y.</li> </ul> |
| <b>Position d&#39;entrée de dégradé</b> *Flotter* | Position normalisée de la ligne ou de la colonne de pixels à échantillonner dans l&#39;«entrée de dégradé». |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée en niveaux de gris</b> *Niveaux de gris* PRINCIPAUX | Image en niveaux de gris à remapper. |
| <b>Entrée de dégradé</b> *Couleur/Niveaux De Gris* | Le dégradé est prélevé sur cette image |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Couleur/Niveaux De Gris* |  |

## Exemples

*Bientôt disponible.*
