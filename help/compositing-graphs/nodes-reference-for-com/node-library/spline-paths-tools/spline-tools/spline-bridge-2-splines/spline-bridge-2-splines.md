---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
breadcrumb-title: ''
description: Utilisez le nœud Pont de spline pour relier des textures entre deux splines afin de créer des connexions homogènes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (2 Splines)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pont Spline (2 Splines)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---


# Pont Spline (2 Splines)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-bridge-2splines-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère des splines de <b>#1 spline</b> à <b>#2 spline</b> le long de ces splines. Les splines générées peuvent être linéaires (droites) ou cubiques (courbes).

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Si les données fournies aux entrées <b>Spline #1</b> et <b>Spline #2</b> contiennent plusieurs splines, seule la dernière spline de chaque liste est utilisée.

## Connecteurs d’entrée

<b>Aperçu #1</b> *Niveaux de gris* L&#39;aperçu des splines d&#39;entrée #1 sous forme d&#39;image en niveaux de gris.

<b>Cœurs splines #1</b> *Couleur* Les coordonnées des points des splines d&#39;entrée #1 codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Position X\
<b>G</b> - Position Y\
<b>B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>#1 de données splines</b> *Couleur* Les données supplémentaires des splines d&#39;entrée #1 codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de spline #1</b> *Nombre entier* Nombre de splines d&#39;entrée #1.

<b>Aperçu #2</b> *Niveaux de gris* L&#39;aperçu des splines d&#39;entrée #2 sous forme d&#39;image en niveaux de gris.

<b>Cœurs splines #2</b> *Couleur* Les coordonnées des points de #2 des splines d&#39;entrée sont codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Position X\
<b>G</b> - Position Y\
<b>B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>#2 de données splines</b> *Couleur* Les données supplémentaires des splines d&#39;entrée #2 codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de spline #2</b> *Nombre entier* Nombre de splines d&#39;entrée #2.

<b>Courbe de longueur tangente de début</b> *Niveaux de gris* (disponible lorsque l’option Type de spline de pont est définie sur Bézier cube) L’image décrivant une courbe utilise les valeurs de sa première ligne de pixels.\
Cette entrée est utilisée pour contrôler la longueur des tangentes de sortie pour le point de départ de chaque spline générée le long de la spline #1.\
Vous pouvez utiliser un nœud Courbe pour créer la courbe.

<b>Courbe de rotation tangente de départ</b> *Niveaux de gris* (disponible lorsque l’option Type de spline de pont est définie sur Bézier cube) L’image décrivant une courbe utilise les valeurs de sa première ligne de pixels.\
Cette entrée est utilisée pour contrôler la rotation des tangentes de sortie pour le point de départ de chaque spline générée le long de la spline #1.\
La valeur de niveaux de gris de l’image représente un certain nombre de tours.\
Vous pouvez utiliser un nœud Courbe pour créer la courbe.

<b>Courbe de longueur tangente de fin</b> *Niveaux de gris* (disponible lorsque l’option Type de spline de pont est définie sur Bézier cube) L’image décrivant une courbe utilise les valeurs de sa première ligne de pixels.\
Cette entrée est utilisée pour contrôler la longueur des tangentes d&#39;entrée pour le point d&#39;extrémité de chaque spline générée le long de la spline #2.\
Vous pouvez utiliser un nœud Courbe pour créer la courbe.

<b>Courbe de rotation tangente de fin</b> *Niveaux de gris* (disponible lorsque l’option Type de spline de pont est définie sur Bézier cube) L’image décrivant une courbe utilise les valeurs de sa première ligne de pixels.\
Cette entrée est utilisée pour contrôler la rotation des tangentes d&#39;entrée pour le point d&#39;extrémité de chaque spline générée le long de la spline #2.\
La valeur de niveaux de gris de l’image représente un certain nombre de tours.\
Vous pouvez utiliser un nœud Courbe pour créer la courbe.

## Connecteurs de sortie

<b>Aperçu</b> *Niveaux de gris* L’aperçu des splines de sortie sous forme d’image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points splines de sortie sont codées dans les couches RVBA d&#39;une image couleur.\
<b>R</b> - Position X\
<b>G</b> - Position Y\
<b>B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Inutilisé\
<b>A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines de sortie.

## Paramètres

<b>Quantité de splines du pont</b> *Nombre entier* Nombre de splines générées le long de la spline #1 à la spline #2.

<b>Type de splines Bridge</b> *Nombre entier* Type de spline généré :
* Linéaire : une spline droite du début à la fin ;
* Bézier cubique : spline incurvée de début à fin, la courbe étant contrôlée par la longueur et l&#39;angle des points de début et de fin.

<b>Démarrer la spline #1</b> *Flottant* Décale l&#39;emplacement le long des #1 splines à partir duquel les splines sont générées. Cette valeur correspond à la longueur normalisée de la #1 spline.\
Plus la valeur est élevée, plus le même nombre de splines est resserré.

<b>Démarrer la spline #2</b> *Flottant* Décale l&#39;emplacement le long des #2 splines à partir duquel les splines sont générées. Cette valeur correspond à la longueur normalisée de la #2 spline.\
Plus la valeur est élevée, plus le même nombre de splines est resserré.

<b>Terminer la spline #1</b> *Flottant* Décale l&#39;emplacement le long des #1 splines jusqu&#39;à l&#39;endroit où les splines sont générées. Cette valeur correspond à la longueur normalisée de la #1 spline.\
Une valeur inférieure permet de tasser le même nombre de splines de manière plus serrée.

<b>Terminer la spline #1</b> *Flottant* Décale l&#39;emplacement le long des #2 splines jusqu&#39;à l&#39;endroit où les splines sont générées. Cette valeur correspond à la longueur normalisée de la #2 spline.\
Une valeur inférieure permet de tasser le même nombre de splines de manière plus serrée.

<b>Décaler la spline #1</b> *Flottant* Applique un décalage au point de départ de toutes les splines le long des #1 splines. Cette valeur correspond à la longueur normalisée de la #1 spline.\
Les splines qui correspondent au début ou à la fin de la spline y sont conservées.

<b>Décaler la spline #2</b> *Flottant* Applique un décalage au point de départ de toutes les splines le long des #2 splines. Cette valeur correspond à la longueur normalisée de la #2 spline.\
Les splines qui correspondent au début ou à la fin de la spline y sont conservées.

<b>Décalage aléatoire de début</b> *Flottant* Applique un décalage aléatoire au point de départ de chaque spline le long des #1 de spline. Cette valeur correspond à la distance normalisée entre les splines sur les #1 splines.\
&#x200B;#1 A 0, les splines sont régulièrement espacées entre les points de #1 Spline de début et Spline de fin.

<b>Décaler la fin aléatoire</b> *Flottant* Applique un décalage aléatoire au point d&#39;extrémité de chaque spline le long du #2 de spline. Cette valeur correspond à la distance normalisée entre les splines sur les #2 splines.\
&#x200B;#2 A 0, les splines sont régulièrement espacées entre les points de #2 Spline de début et Spline de fin.

<b>Début de la longueur tangente</b> *Flottant* (disponible lorsque « Bridge Splines Type » est défini sur « Cubic Bézier »)Longueur de la tangente de sortie pour le point de départ sur la #1 de spline de toutes les splines générées.

<b>Fin de longueur tangente</b> *Flottant* (disponible lorsque « Bridge Splines Type » est défini sur « Cubic Bézier »)Longueur de la tangente d&#39;entrée pour le point d&#39;extrémité sur la #2 de spline de toutes les splines générées.

<b>Début de rotation tangente</b> *Flottant* (disponible lorsque « Bridge Splines Type » est défini sur « Cubic Bézier »)La rotation de la tangente de sortie pour le point de départ sur la #1 de spline de toutes les splines générées.\
La valeur est un nombre de tours.

<b>Fin de rotation tangente</b> *Flottant* (disponible lorsque « Bridge Splines Type » est défini sur « Cubic Bézier »)Rotation de la tangente d&#39;entrée pour le point d&#39;extrémité sur la #2 de spline de toutes les splines générées.\
La valeur est un nombre de tours.

+++Prévisualiser
<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Afficher l&#39;enveloppe de Thickness</b> *Booléen*\
Affiche des lignes supplémentaires sur les thickness de la spline.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness de la visualisation de la spline en pixels dans la sortie d&#39;aperçu.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-Before.jpg" alt="SplineBridge-2Splines_Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-After.jpg" alt="SplineBridge-2Splines_Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineBridge-2Splines_Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>
