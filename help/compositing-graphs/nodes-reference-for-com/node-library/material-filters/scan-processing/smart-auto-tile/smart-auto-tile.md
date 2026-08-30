---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: Utilisez le nœud Mosaïque automatique dynamique pour créer automatiquement des mosaïques homogènes à partir de matériaux numérisés à l’aide de la détection intelligente de motif.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque automatique dynamique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# Mosaïque automatique dynamique

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud transforme un ensemble sans mosaïque de couleurs de base, de normales et de hauteurs en une version de mosaïque en fonction de l’analyse intelligente des entrées. Il est similaire à [Make It Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), mais beaucoup plus avancé car il utilise des informations de tous les canaux pour fusionner les éléments de la manière la plus intelligente (similaire à ce que fait [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)). Il possède également une fonction interne [Recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) pour déterminer la zone à utiliser lors de la juxtaposition. Pour bien comprendre cette fonction, [en savoir plus sur le nœud Recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md).

Pour utiliser ce nœud, commencez par définir votre zone recadrée, puis utilisez les paramètres Contour pour déterminer la manière dont les contours carrelés sont fusionnés au centre. Les paramètres Seuil sont d&#39;une importance capitale pour cela ! Gardez à l’esprit que les zones grandes et uniformes ne fonctionnent pas très bien avec cet effet ; plus il y a de détails et de formes, plus cela doit fonctionner.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Utiliser le masque ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Recadrer</b> |  |
| <b>Taille d&#39;entrée</b> <i>0 - 8192</i> | Résolution et proportions des Images d&#39;entrée. Très important pour les images non carrées. |
| <b>Transformation</b> <i>(Matrice de transformation)</i> | Fait pivoter et met à l’échelle le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Edge</b> |  |
| <b>Détecter les contours</b> <i>Faux/Vrai</i> | Active ou désactive la fusion détectée par arête spéciale. |
| <b>Utiliser Le Seuil Par Canal</b> <i>Faux/Vrai</i> | Bascule entre une valeur de seuil globale ou une valeur pour chaque canal. |
| <b>Seuil</b> <i>0.0 - 1.0</i> |  |
| <b>Base color de seuil</b> <i>0.0 - 1.0</i> |  |
| <b>Seuil normal</b> <i>0.0 - 1.0</i> |  |
| <b>Height du seuil</b> <i>0.0 - 1.0</i> |  |
| <b>Décalage de coupe</b> <i>0.0 - 0.5</i> | Contrôle principal pour déplacer la coupe, les axes X et Y sont séparés. |
| <b>Flou</b> <i>0.0 - 2.0</i> | Atténue la transition de fusion. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Contrôle l&#39;irrégularité des résultats de l&#39;analyse des contours. |
| <b>Résolution de Grille</b> <i>1 - 11</i> | Résolution de la qualité de l&#39;analyse des contours. |
| <b>Utiliser la Base color</b> <i>Faux/Vrai</i> | Active/désactive le traitement de Base color (entrée et sortie). |
| <b>Utiliser la normale</b> <i>Faux/Vrai</i> | Active/désactive le traitement normal (entrée et sortie). |
| <b>Utiliser l&#39;Height</b> <i>Faux/Vrai</i> | Active/désactive le traitement normal (entrée et sortie). |
| <b>Utiliser le masque</b> <i>Faux/Vrai</i> | Active ou désactive l’utilisation de la carte de masque pour les formes de masque de tampon personnalisées. |
