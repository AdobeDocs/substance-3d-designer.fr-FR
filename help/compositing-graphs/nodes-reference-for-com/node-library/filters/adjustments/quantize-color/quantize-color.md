---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Quantifier la couleur pour réduire le nombre de niveaux de couleur des effets de postérisation stylisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quantifier la couleur
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---


# Quantifier la couleur

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Quantifier la couleur](quantize-color.resources/QuantizeColor.png "Quantifier la couleur"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Réduit la quantité de couleurs dans une image en couleurs, aplatissant efficacement les dégradés.

En plus de l’image traitée, le nœud extrait également les éléments suivants :

* Une <b>palette</b> des couleurs restantes, qui peut être utilisée pour coloriser d&#39;autres images
* Un <b>Map id</b> des zones quantifiées, qui peut être utilisé pour redéfinir les couleurs de l&#39;image traitée à l&#39;aide d&#39;une palette différente
* <b>quantité</b> de couleurs restantes en tant que valeur d&#39;entier brut

</td>
</tr>
</table>

Si le paramètre Ignorer alpha est défini sur Faux, le canal Alpha de l’image d’origine est utilisé pour sélectionner les zones de l’image dans lesquelles les couleurs doivent être extraites pour le processus de quantification, tandis que les couleurs des zones transparentes sont ignorées.

Cela permet de mieux contrôler les couleurs extraites.

Ce nœud peut être utilisé en combinaison avec les nœuds suivants : [Créer une palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Appliquer la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Modifier la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Afficher la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Couleur</i> PRINCIPALE | Image couleur à quantifier. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Image couleur quantifiée. |
| <b>ID</b> <i>Niveaux de gris</i> | Carte dans laquelle chaque couleur quantifiée se voit attribuer un identifiant d’entier unique.   Il peut être utilisé pour :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Extraire un masque</b> de certaines zones quantifiées avec le nœud [ID vers masque](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/id-to-mask/id-to-mask.md)</li> <li data-preserve-html="true"><b>Redéfinir les couleurs</b> de l&#39;image quantifiée avec les nœuds [Appliquer la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md) ou [Modifier la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)</li> </ul> |
| <b>Palette</b> <i>Couleur</i> | Palette extraite de l’image, contenant les couleurs restantes après quantification.   L’image est une liste ordonnée de couleurs RGB codées sous la forme d’une ligne de pixels et peut contenir jusqu’à 256 couleurs.   La palette peut être visualisée avec le nœud [Afficher la palette de couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md). |
| <b>Quantité de couleur de la palette</b> <i>Entier</i> | Quantité de couleurs stockées dans la palette. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Max. quantité de couleur</b> *Entier* | Quantité maximale de couleurs à utiliser dans l’image quantifiée.   Cette valeur est identique à celle utilisée dans la palette extraite de l’image.   «Maximum» signifie que ce montant peut ne pas être atteint en raison de la technique de quantification utilisée. Vérifiez dans la sortie « Quantité de couleur de la palette » la quantité réelle de couleurs extraites. |
| <b>Lissage de contour</b> *Flottant* | Contrôle le rayon d’un effet de lissage appliqué à l’image d&#39;entrée, utilisé pour simplifier l’image quantifiée en formes plus unies et cohérentes.   Remarque : ce lissage nécessite des calculs intensifs. Par conséquent, l’augmentation de cette valeur augmente sensiblement le temps de calcul du nœud. |
| <b>Dithering</b> *Flottant* | Applique un motif de dithering afin de recréer les dégradés et les mélanges de couleurs dans l’image d’origine, tout en utilisant uniquement les couleurs restantes après la quantification.   Assurez-vous d’utiliser la valeur de lissage de contour de 0 pour produire l’effet de dithering attendu. |
| <b>Motif de Dithering</b> *Entier* | Motif de dithering utilisé pour recréer les dégradés et les mélanges de couleurs de l’image d’origine :<ul data-preserve-html="true"> <li data-preserve-html="true">Bruit bleu</li> <li data-preserve-html="true">Bayer</li> </ul> |
| <b>Ignorer alpha</b> *Booléen* | Par défaut, le canal Alpha de l’image d’origine est utilisé pour sélectionner les zones de l’image dans lesquelles les couleurs doivent être extraites pour le processus de quantification, tandis que les couleurs des zones transparentes sont ignorées. Cela permet de mieux contrôler les couleurs extraites.   En effet, vous pouvez utiliser uniquement les couleurs dans les parties visibles de l’image pour le processus de quantification.   Cette option vous permet de désactiver ce masquage et d&#39;utiliser l&#39;image *complète*, quelle que soit la transparence. |
| <b>Espace colorimétrique de distance</b> *Entier* | Les couleurs sont disposées dans un *cube* dont la largeur, l&#39;height et la profondeur sont un dégradé où chaque composante d&#39;une couleur augmente de 0 à 1 (par ex. rouge, vert et bleu en RGB).   Le processus de quantification consiste à sélectionner les *couleurs de définition* dans une image, puis à trouver les couleurs les plus proches dans le cube et à les remplacer par cette couleur de définition.   Ce paramètre vous permet de sélectionner l’espace colorimétrique utilisé pour répartir les couleurs dans le cube. Cela modifie le résultat de la quantification en modifiant les critères de détection d’une couleur de définition et de réorganisation des couleurs voisines.   Vous pouvez sélectionner l’espace colorimétrique qui correspond à votre cas d’utilisation :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Lab (couleur) :</b> un espace colorimétrique perceptif normalisé, qui distribue les couleurs de telle sorte que les couleurs qui « se rapprochent » se rapprochent en fait dans le cube. Ceci est approprié pour l&#39;image qui peut être visualisée sur les écrans</li> <li data-preserve-html="true"><b>RGB (données) :</b> la couleur est divisée en rouge, vert et bleu et distribuée directement le long de ces axes, sans tenir compte de la perception humaine. Cela convient aux images contenant des données brutes, telles que des maps normal</li> </ul> |
| <b>Mode de tri d&#39;ID</b> *Entier* | Les couleurs sont disposées dans un *cube* où la largeur, l&#39;height et la profondeur sont un dégradé où chaque composante d&#39;une couleur augmente de 0 à 1 (par ex. rouge, vert et bleu en RGB).   Ce paramètre sélectionne la méthode utilisée pour classer la liste des couleurs dans la palette extraite et les index dans les zones du Map id extrait :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Courbe Z :</b> les couleurs sont triées par la suivante trouvée dans le cube de couleurs à l&#39;aide d&#39;une courbe Z, du blanc au noir</li> <li data-preserve-html="true"><b>Teinte :</b> couleurs sont triées par teinte la plus proche</li> <li data-preserve-html="true"><b>Représentativité :</b> les couleurs sont triées de la plus utilisée à la moins utilisée dans l&#39;image quantifiée</li> </ul> |
| <b>filtrage de réduction d&#39;échelle</b> *Entier* | Le processus de quantification des couleurs consiste à calculer un histogramme d&#39;une image de taille réduite (c&#39;est-à-dire réduite), afin de trier ses couleurs par importance. Ce paramètre contrôle la méthode de filtrage de l&#39;image réduite avant de calculer son histogramme :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bilinéaire :</b> applique un filtrage bilinéaire à l&#39;image, ce qui entraîne un histogramme avec des couleurs interpolées qui peuvent ne pas faire partie de l&#39;image d&#39;origine, diluant certaines des couleurs d&#39;origine. Cela aide avec les images utilisant beaucoup de couleurs.</li> <li data-preserve-html="true"><b>Le plus proche :</b> échantillonne la couleur du pixel le plus proche sans filtrage, ce qui entraîne un histogramme utilisant uniquement les couleurs de l’image d’origine. Ceci est approprié pour les images utilisant peu de couleurs.</li> </ul> |

## Exemples

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_6_before.jpg" alt="quantize_color_example_6_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_6_after.jpg" alt="quantize_color_example_6_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_2_before.jpg" alt="quantize_color_example_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_2_after.jpg" alt="quantize_color_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_3_before.jpg" alt="quantize_color_example_3_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_3_after.jpg" alt="quantize_color_example_3_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_4_before.jpg" alt="quantize_color_example_4_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_4_after.jpg" alt="quantize_color_example_4_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="quantize-color.resources/quantize_color_example_5_before.jpg" alt="quantize_color_example_5_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="quantize-color.resources/quantize_color_example_5_after.jpg" alt="quantize_color_example_5_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>
