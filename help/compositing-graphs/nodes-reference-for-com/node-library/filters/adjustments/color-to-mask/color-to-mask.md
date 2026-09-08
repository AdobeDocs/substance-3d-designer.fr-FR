---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur vers masque pour convertir des couleurs spécifiques en masques afin de créer des effets de traitement et de masquage sélectifs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur au masque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# Couleur au masque

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Couleur à masquer - Icône](../../../../../../assets/color_to_mask.png "Couleur à masquer - Icône"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Extrait un masque de niveaux de gris des couleurs sélectionnées dans une image couleur.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Couleur</i> | Image couleur d’entrée à partir de laquelle un masque doit être extrait en fonction de ses couleurs. |
| <b>Entrée couleur</b> <i>Couleur</i>   *Disponible lorsque &#39;Utiliser l&#39;entrée de couleur&#39; est défini sur &#39;True&#39;* | Image couleur d’entrée utilisée pour définir la couleur de référence par pixel. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Masque généré sous forme d’image bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Utiliser l&#39;entrée de couleur</b> *Booléen* | Utilisez une image d’entrée au lieu d’une couleur uniforme, afin de définir une couleur de référence par pixel.    L&#39;image d&#39;entrée est fournie par l&#39;entrée <b>Entrée couleur</b>. |
| <b>Couleur</b> *Flottant 3* *Disponible lorsque &#39;Utiliser l&#39;entrée de couleur&#39; est défini sur &#39;False&#39;* | Couleur uniforme de référence autour de laquelle la sélection de couleurs doit être effectuée. |
| <b>Seuil</b> *Flotter* | Distance jusqu’à la couleur de référence en dessous de laquelle les couleurs sont sélectionnées. |
| <b>atténuation de la sélection</b> *Flotter* | Atténuez la sélection de couleurs en fonction de la distance par rapport à la couleur de référence. |
| <b>Espace colorimétrique de distance</b> *Nombre entier* | Le processus Égaliser consiste à comparer les couleurs afin de déterminer la distance les séparant. Certains algorithmes d’espace colorimétrique et de distance sont mieux adaptés à des cas d’utilisation spécifiques.   Cette liste déroulante vous permet de sélectionner l’espace colorimétrique utilisé pour comparer les couleurs :<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB (données) :</i></b> la couleur est divisée en canaux rouge, vert et bleu et distribuée directement le long de ces axes, sans tenir compte de la perception humaine. Ceci est approprié pour les images contenant des données brutes.</li> <li data-preserve-html="true"><i>SRVB linéaire (couleur) :</i> la couleur est divisée en canaux rouge, vert et bleu et répartie de manière linéaire par rapport à l&#39;intensité lumineuse en pixels. Ceci est approprié pour l&#39;image qui peut être visualisée sur les écrans.</li> <li data-preserve-html="true"><b><i>Luminance (couleur) :</i></b> la couleur est divisée en valeurs Teinte, Chrominance et Luminance, où seule la valeur Luminance est utilisée dans la comparaison. Ceci est approprié pour l&#39;image qui peut être visualisée sur les écrans.</li> <li data-preserve-html="true"><i>Lab (couleur) :</i> un espace colorimétrique perceptif normalisé, qui distribue les couleurs de telle sorte que les couleurs qui « se rapprochent » se rapprochent réellement dans le cube. Ceci est approprié pour l&#39;image qui peut être visualisée sur les écrans.</li> <li data-preserve-html="true"><i>Angle (normal) :</i> la couleur est divisée en axes X, Y et Z d&#39;un vecteur et comparée à un produit point. Cette option convient aux images contenant des normales d’espace tangentes.</li> </ul> |
| <b>Épaisseurs de distance</b> *Float3* | L’algorithme de distance des couleurs Lab (DeltaE2000) introduit certains facteurs de pondération pour chaque valeur de luminosité, de chrominance et de teinte.   Des valeurs faibles réduisent l’influence des facteurs dans l’algorithme de différence de couleur.   Étant donné que l&#39;œil accepte généralement des différences de luminosité (L) plus grandes que celles de chrominance (C) ou de teinte (H), le rapport par défaut de (L:C:H) est de (0,5:1:1). Un rapport de 0,5:1:1 permet une différence de luminosité deux fois supérieure à celle de la chrominance ou de la teinte. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
