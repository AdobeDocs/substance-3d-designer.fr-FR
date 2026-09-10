---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: Utilisez le nœud Niveaux de gris du mappeur de spline pour mapper les textures de niveaux de gris le long des tracés de spline avec des paramètres personnalisables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Niveaux de gris du mappeur de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---


# Niveaux de gris du mappeur de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-mapper-grayscale.resources/spline-mapper-grayscale-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Mappe une image en niveaux de gris d&#39;entrée sur une forme primitive étirée le long des splines d&#39;entrée.

La forme primitive peut être un plan, un demi-cylindre ou un cylindre. Les cylindres peuvent être tordus le long de la spline pour déformer l&#39;image mappée en conséquence.

</td>
</tr>
</table>

Le nœud produit l&#39;image mappée sous forme d&#39;image en niveaux de gris, ainsi que d&#39;autres informations telles que l&#39;height, les UV (c&#39;est-à-dire les coordonnées de l&#39;image) et un masque d&#39;ID pour sélectionner chaque spline mappée indépendamment.

>[!IMPORTANT]
>
> Il peut en résulter des artefacts indésirables en dehors de l&#39;enveloppe de la spline lors de l&#39;utilisation de valeurs de thickness très faibles. Il s’agit d’un problème connu.

>[!NOTE]
>
> Voir aussi [Couleur du mappeur de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br> - signe : la spline est fermée (négative) ou ouverte (positive);<br> - Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Entier</i> | Nombre de splines d&#39;entrée. |
| <b>Color Map</b> <i>Niveaux de gris</i> | Image en niveaux de gris d&#39;entrée à mapper le long des splines d&#39;entrée. |
| <b>Map height</b> <i>Niveaux de gris</i> | Map height de niveaux de gris d&#39;entrée à mapper le long des splines d&#39;entrée. |
| <b>Twist curve</b> <i>Niveaux de gris</i> | Image décrivant une courbe en utilisant les valeurs de sa première ligne de pixels.<br>Lorsque le paramètre <b>Forme</b> est défini sur <i>Demi-cylindre</i> ou <i>Cylindre</i>, cette entrée est utilisée pour contrôler la torsion des UV autour de la forme. Son impact est contrôlé à l&#39;aide du paramètre <b>Multiplicateur de courbe de torsion des UV</b>.<br>La courbe fournit un profil pour le degré de rotation le long de la spline, où le premier pixel de la ligne correspond à la rotation au début de la spline et le dernier à la rotation à la fin. La valeur Niveaux de gris représente un nombre de tours.<br>Vous pouvez utiliser un nœud [Courbe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) pour créer la courbe. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Couleur</b> <i>Niveaux de gris</i> | Résultat du mappage de l’image couleur d’entrée sur les splines d’entrée, en tant qu’image en niveaux de gris. |
| <b>Height</b> <i>Niveaux de gris</i> | Résultat du mappage de l&#39;image d&#39;Height d&#39;entrée sur les splines d&#39;entrée, en tant qu&#39;image en niveaux de gris. |
| <b>UV</b> <i>Couleur</i> | UV (coordonnées) du mapping sur les splines d&#39;entrée, codés dans une image couleur. |
| <b>ID</b> <i>Niveaux de gris</i> | Masque des images mappées le long des splines d’entrée, où les valeurs de blanc sont incrémentées de 1 d’une spline à la suivante afin que chaque forme puisse être sélectionnée indépendamment. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité de segments</b> <i>Nombre entier</i> | Les splines sont simplifiées en segments avant que les coordonnées de l&#39;image ne les traversent.<br>Une plus grande quantité de segments permet une mise en correspondance plus fluide le long des courbes. |
| <b>Mise à l&#39;échelle automatique des UV</b> <i>Booléen</i> | Ajuste automatiquement l&#39;échelle des coordonnées pour conserver une image carrée lors du mappage le long des splines. |
| <b>Échelle UV</b> <i>Flottant 2</i> | Ajuste l&#39;échelle des coordonnées mappées en X (horizontalement) et Y (verticalement).<br>Plus la valeur est élevée, plus la densité de la mosaïque de l&#39;image est élevée. |
| <b>Mode</b> <i>Entier</i> | Méthode de sélection des splines le long desquelles l&#39;image doit être mappée :<br>- <i>Dessiner une spline</i> : toutes les splines de la liste d&#39;entrée sont utilisées ;<br>- <i>Dessiner une spline unique</i> : seule la spline avec l&#39;index spécifié est utilisée ;<br>- <i>Dessiner une plage de splines</i> : seules les splines dont l&#39;index est inclus dans la plage spécifiée sont utilisées. |
| <b>Dessiner l&#39;index spline</b> <i>Entier</i> | (Disponible lorsque le mode est défini sur Tracer une seule spline) Index de la spline le long de laquelle l’image doit être mappée. |
| <b>Tracer la plage de splines</b> <i>Entier 2</i> | (Disponible lorsque le mode est défini sur Tracer la plage de splines) Plage d&#39;index des splines le long desquelles l&#39;image doit être mappée. |
| <b>Démarrer</b> <i>Flottant</i> | Décale le début de la partie de la spline à plaquer.<br>La valeur représente la longueur normalisée de la spline. |
| <b>Fin</b> <i>Flottant</i> | Décale l&#39;extrémité de la partie de la spline à plaquer.<br>La valeur représente la longueur normalisée de la spline. |
| <b>Mode Thickness</b> <i>Entier</i> | Méthode de définition du thickness de l&#39;image mappée :<br>- <i>Manuel</i> : définissez le thickness explicitement avec une valeur arbitraire ;<br>- <i>À partir de la spline</i> : utilisez le thickness de la spline. |
| <b>Thickness</b> <i>Flotter</i> | (Disponible lorsque le mode Thickness est défini sur Manuel) Valeur arbitraire pour le thickness de l&#39;image mappée le long des splines. |
| <b>Multiplicateur de Thickness</b> <i>Flotter</i> | (Disponible lorsque le mode Thickness est défini sur Spline) Multiplicateur global pour le thickness de l&#39;image mappée le long des splines, lorsque ce thickness est piloté par celui des splines. |
| <b>Forme</b> <i>Nombre entier</i> | Forme primitive utilisée pour mapper les coordonnées de l&#39;image le long des splines :<br>- <i>Plan</i> : les coordonnées sont mappées sur un plan plat ;<br>- <i>Demi-cylindre</i> : les coordonnées sont mappées sur un demi-cylindre dont l&#39;axe du cercle de base suit la direction de la spline ;<br>- <i>Cylindre</i> : les coordonnées sont mappées sur un cylindre dont l&#39;axe du cercle de base suit la direction de la spline. |
| <b>Multiplicateur d&#39;Height du cylindre</b> <i>Flotter</i> | (Disponible lorsque « Forme » est défini sur « Demi-cylindre » ou « Cylindre ») Multiplicateur de l’intensité de la contribution de la bouteille à l’height dans la sortie d’Height.<br>Les ajustements d&#39;Height sont cumulatifs. |
| <b>Décalage de l&#39;Height du cylindre</b> <i>Flotter</i> | (Disponible lorsque l&#39;option Forme est définie sur Demi-cylindre ou Cylindre) Décale le centre du profil de forme Cylindre ou Demi-cylindre de la surface de la spline d&#39;un diamètre sous la surface. |
| <b>Intensité de torsion des UV</b> <i>Flotter</i> | (Disponible lorsque « Forme » est défini sur « Demi-cylindre » ou « Cylindre ») La torsion des coordonnées de l’image autour du cylindre, en nombre de tours.<br>La torsion implique la rotation du cylindre à l&#39;extrémité de la spline uniquement. La rotation est ensuite interpolée le long de la spline. |
| <b>Multiplicateur de courbe de torsion UV</b> <i>Flotter</i> | (Disponible lorsque le paramètre Forme est défini sur Demi-cylindre ou Cylindre) Multiplicateur de l’intensité de la contribution du Twist curve à la torsion de la bouteille.<br>La courbe fournit un profil pour le degré de rotation le long de la spline, où le premier pixel de la ligne correspond à la rotation au début de la spline et le dernier à la rotation à la fin. La valeur Niveaux de gris représente un nombre de tours. |
| <b>Décalage de la courbe de torsion UV</b> <i>Flottant</i> | (Disponible lorsque l’option Forme est définie sur Demi-cylindre ou Cylindre) Applique un décalage global aux valeurs de rotation fournies par le Twist curve, en nombre de tours. |
| <b>Multiplicateur d&#39;Height spline</b> <i>Flottant</i> | Règle l’intensité de la contribution de l’entrée d’Height spline à la sortie d’Height.<br>Les ajustements d&#39;Height sont cumulatifs. |
| <b>Multiplicateur d&#39;Height d&#39;entrée</b> <i>Flottant</i> | Règle l’intensité de la contribution de l’entrée de Map height à la sortie d’Height.<br>Les ajustements d&#39;Height sont cumulatifs. |
| <b>Correction Non Carrée</b> <i>Booléen</i> | Ajustez la position et le thickness des points pour conserver la forme de la spline dans des résolutions autres que carrées.<br>Cela a également un impact sur la distribution uniforme. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-mapper-grayscale.resources/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-mapper-grayscale.resources/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapperGrayscale-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](spline-mapper-grayscale.resources/SplineMapperGrayscale-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 3](spline-mapper-grayscale.resources/SplineMapperGrayscale-Variant1-After1.jpg "Exemple de nœud 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
