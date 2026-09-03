---
title: Atlas en grille des niveaux de gris
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Générateur > Motif > Niveaux de gris Atlas en grille
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Atlas en grille des niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône ![Atlas en grille en niveaux de gris](grid-atlas-grayscale.resources/grid-atlas-grayscale-01.png "Atlas en grille en niveaux de gris")

<b>Entrée :</b> Générateur > Motif

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Emportez jusqu&#39;à 16 images en niveaux de gris sur une grille de taille XY réglable.<br>L&#39;image de l&#39;atlas de sortie peut être échantillonnée à partir d&#39;un nœud [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) ou [Shape splatter mapper grayscale](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md).

Voir aussi [Couleur Atlas en grille](../grid-atlas-color/grid-atlas-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|                             |                                |
|:----------------------------|:-------------------------------|
| <b>Entrée 1</b> *Niveaux de gris* | La saisie de l’image en niveaux de gris #1. |
| <b>Entrée 2</b> *Niveaux de gris* | La saisie de l’image en niveaux de gris #2. |
| <b>Entrée 3</b> *Niveaux de gris* | La saisie de l’image en niveaux de gris #3. |
| <b>Entrée 4</b> *Niveaux de gris* | La saisie de l’image en niveaux de gris #4. |
| <b>Entrée 5</b> *Niveaux de gris* | La saisie de l’image en niveaux de gris #5. |
| <b>Entrée 6</b> *Niveaux de gris* | #6 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 7</b> *Niveaux de gris* | #7 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 8</b> *Niveaux de gris* | #8 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 9</b> *Niveaux de gris* | #9 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 10</b> *Niveaux de gris* | #10 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 11</b> *Niveaux de gris* | #11 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 12</b> *Niveaux de gris* | #12 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 13</b> *Niveaux de gris* | #13 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 14</b> *Niveaux de gris* | #14 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 15</b> *Niveaux de gris* | #15 d’entrée de l’image en niveaux de gris. |
| <b>Entrée 16</b> *Niveaux de gris* | #16 d’entrée de l’image en niveaux de gris. |

<a name="outputs"></a>

## Sorties

|               |                                  |
|:--------------|:---------------------------------|
| <b>Sortie</b> | Atlas en grille en niveaux de gris de la sortie. |

<a name="parameters"></a>

## Paramètres

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Taille de la grille X</b> *Nombre entier* | Taille de la grille sur l&#39;axe X.<br>C&#39;est-à-dire le nombre d&#39;images compressées sur l&#39;axe X. |
| <b>Taille de la grille Y</b> *Nombre entier* | Taille de la grille sur l&#39;axe Y.<br>C&#39;est-à-dire le nombre d&#39;images compressées sur l&#39;axe Y. |
| <b>Mode Taille de sortie</b> *Nombre entier* | Méthode de définition de la taille de l&#39;image de sortie en fonction du paramètre de base « Taille de sortie » du nœud :<br><br>- <b>Manuel :</b> Utilisez la taille telle quelle.<br>- <b>Rapport automatique :</b> Ajustez le rapport d&#39;image en fonction de la taille de la grille afin de réduire la taille de l&#39;image. La déformation se produira pour les grilles non carrées utilisant 3 lignes ou colonnes, par exemple (3, 2), (4, 3) |

## Exemples

<img src="./grid-atlas-grayscale.resources/grid-atlas-grayscale-02.png" alt="Nœud d&#39;Atlas en grille en niveaux de gris dans le contexte d&#39;un graphe" style="width: 50%"><br>
<i>Nœud en niveaux de gris Atlas en grille dans le contexte d&#39;un graphique</i>
