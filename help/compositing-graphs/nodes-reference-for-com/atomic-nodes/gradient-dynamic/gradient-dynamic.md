---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ""
description: Utilisez le nœud Dégradé (dynamique) pour créer des dégradés dynamiques contrôlables par des paramètres d'entrée et des valeurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé (dynamique)
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 8%
---

# Dégradé (dynamique)

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Noeud atomique : Dégradé dynamique](gradient-dynamic.resources/comp_dyngradient_1.png "Noeud atomique : Dégradé dynamique"){width="100%"}

<b>Entrée :</b> Noeuds atomiques

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Remappe les valeurs de niveaux de gris d’une image, en utilisant un dégradé fourni par une ligne ou une colonne de pixels d’une autre image.

Elle constitue une légère alternative au nœud de dégradé, mais contrairement à ce dernier, les dégradés ne sont pas définis en interne, mais proviennent d’une entrée externe.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="gradient-dynamic.resources/gradient-dynamic-tooltip.gif" alt="info-bulle dégradé-dynamique" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Cela permet principalement d&#39;éviter le problème où les paramètres ne peuvent pas être exposés, car les paramètres de couleur sont déplacés en dehors du nœud. C&#39;est ce qui la rend « dynamique ».

Bien que le dégradé (dynamique) ne soit pas un nœud difficile à utiliser seul, ses cas d&#39;utilisation sont un peu plus avancés : la plupart des utilisations standard peuvent être couvertes par le nœud de dégradé régulier.

Ce nœud entre en jeu lorsque vous êtes trop limité par le système de touches de l’éditeur de dégradé et que vous souhaitez que les couleurs et les positions du dégradé soient déterminées par d’autres entrées, paramètres et parties de votre graphe.

Vous pouvez également utiliser le curseur Position de l’entrée de dégradé pour alterner entre plusieurs dégradés stockés dans une seule entrée Dégradé.



## Paramètres

|  |  |
| --- | --- |
| <b>Adressage de dégradé</b> *Booléen* | Définit si le dégradé se répète (carreaux) ou se bloque.   Ce paramètre détermine la façon dont les pixels HDR de l’entrée en niveaux de gris sont manipulés hors de la plage [0, 1] : ils sont bridés ou pliés jusqu’à [0, 1]. |
| <b>Orientation du dégradé</b> *Entier* | Définit l’axe d’échantillonnage de la « saisie de dégradé » :<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Horizontal :</i> échantillonnez une ligne de pixels sur l&#39;axe X.</li> <li data-preserve-html="true"><i>Vertical :</i> échantillonnez une colonne de pixels sur l&#39;axe Y.</li> </ul> |
| <b>Position d&#39;entrée de dégradé</b> *Flottant* | Position normalisée de la ligne ou de la colonne de pixels à échantillonner dans l&#39;«entrée de dégradé». |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée en niveaux de gris</b> *Niveaux de gris* PRINCIPAUX | Image en niveaux de gris de remappage. |
| <b>Entrée de dégradé</b> *Couleur/Niveaux De Gris* | Le dégradé est prélevé sur cette image |


## Exemples

*Bientôt disponible.*
