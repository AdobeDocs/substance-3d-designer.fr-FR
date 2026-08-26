---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation de spline pour déformer des textures le long de tracés de spline afin de créer des motifs courbes et organiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation de la spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---


# Déformation de la spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-warp-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Déplace les splines d&#39;entrée en fonction de la texture d&#39;intensité ou de la texture vectorielle d&#39;entrée.

L&#39;intensité de l&#39;effet de déformation peut être ajustée le long de la spline à l&#39;aide des commandes d&#39;atténuation.

</td>
</tr>
</table>

## Connecteurs d’entrée

<b>Aperçu</b> *Niveaux de gris* Aperçu des splines d&#39;entrée sous la forme d&#39;une image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points des splines d&#39;entrée codées dans les couches RVBA d&#39;une image couleur :\
<b> R</b> - Position X\
<b> G</b> - Position Y\
<b> B</b> - Height\
<b>A</b> - Données compressées :\
* Signe : la spline est fermée (négative) ou ouverte (positive);\
* Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Inutilisé\
<b> A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines d&#39;entrée.

<b>Carte d&#39;intensité</b> *Niveaux de gris* (disponible lorsque l’option Utiliser la carte vectorielle est définie sur Faux)\
Image en niveaux de gris utilisée pour contrôler la direction et l&#39;intensité de l&#39;effet de déformation sur les splines d&#39;entrée.\
La couleur de chaque pixel de l’image définit un multiplicateur qui permet de déplacer les points de la spline le long de leur normale (c’est-à-dire dans le sens perpendiculaire à la spline) jusqu’à la plage entière de l’image.\
Les valeurs [0 ; 1] de l&#39;image sont remappées sur la plage [-1 ; 1] lorsqu&#39;elles sont lues comme un multiplicateur : 0 et 1 déplacent la spline de la même distance mais dans des directions opposées. 0,5 laisse la spline en place.

<b>Carte vectorielle</b> *Niveaux de gris* (disponible lorsque l&#39;option Utiliser la carte vectorielle est définie sur Vrai)Image couleur d&#39;entrée utilisée pour contrôler la direction et l&#39;intensité de l&#39;effet de déformation sur les splines d&#39;entrée.\
La couleur de chaque pixel de l’image indique le vecteur (X, Y) dont les coordonnées sont codées dans les canaux rouge (X) et vert (Y). +X à droite et +Y en bas.\
Les valeurs [0 ; 1] de l’image sont remappées sur la plage [-1 ; 1] lorsqu’elles sont lues en tant que coordonnées vectorielles : 0 rouge déplace les points vers la gauche et 0 vert déplace les points vers le haut. 0,5 rouge et vert laisse la spline en place.

<b>Courbe D&#39;Atténuation</b> *Niveaux de gris* L&#39;image décrivant une courbe en utilisant les valeurs de sa première ligne de pixels.\
Lorsque le paramètre Utiliser la courbe d&#39;atténuation est défini sur True, cette entrée est utilisée pour contrôler l&#39;atténuation de l&#39;effet de déformation près du début et de la fin de la spline.\
La courbe fournit un profil pour l&#39;atténuation, où le premier pixel de la ligne est l&#39;intensité de l&#39;effet de déformation au début de la spline, et le dernier est l&#39;intensité à la fin. La valeur Niveaux de gris correspond à l’intensité.\
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

<b>Intensité de déformation</b> *Flottant* L&#39;intensité selon laquelle les splines sont déplacées.

<b>Centre de déformation</b> *Flottant* Spécifie la valeur de la courbe d&#39;intensité correspondant au maintien des splines en place.\
Une valeur de 0 ou 1 signifie que les splines ne peuvent être déplacées que d&#39;un seul côté.

<b>Mode d&#39;échantillonnage</b> *Nombre entier* Méthode de mappage des valeurs de la courbe d&#39;intensité ou de la courbe vectorielle aux splines :\
*- Espace de texture* : les valeurs sont appliquées aux splines où elles se trouveraient si elles étaient placées dans une texture à l&#39;aide des coordonnées UV de la texture. Cela applique effectivement la valeur aux cannelures « en place »;\
*- Horizontal le long de la spline* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cordons de spline), où chaque ligne est appliquée à une spline différente de haut en bas ;\
*- Heure. le long de la spline (rand. offset X)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir entrée Spline Coords), avec un décalage horizontal aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans Spline Coords);\
*- Heure. le long de la spline (rand. décalage Y)* : les valeurs sont appliquées directement aux coordonnées des splines codées (voir Entrée des cœurs de spline), avec un décalage vertical aléatoire dans la carte d&#39;échelle pour chaque spline (c&#39;est-à-dire chaque ligne dans les cœurs de spline).

<b>Utiliser la carte vectorielle</b> *Booléen* Bascule la méthode de déplacement des splines sur l&#39;utilisation d&#39;une entrée de mappage vectoriel pour spécifier la direction du displacement.\
La couleur de chaque pixel de l’image indique le vecteur (X, Y) dont les coordonnées sont codées dans les canaux rouge (X) et vert (Y). +X à droite et +Y en bas.\
Les valeurs [0 ; 1] de l’image sont remappées sur la plage [-1 ; 1] lorsqu’elles sont lues en tant que coordonnées vectorielles : 0 rouge déplace les points vers la gauche et 0 vert déplace les points vers le haut. 0,5 rouge et vert laisse la spline en place.

<b>Utiliser la courbe d&#39;atténuation</b> *Booléen* Permet de contrôler l’intensité de l’effet de déformation le long d’une spline à l’aide d’une courbe codée dans l’image d’entrée Courbe d’atténuation.<b></b>

<b>Carrelage de la carte d&#39;intensité</b> *Flottant* (disponible lorsque le mode d&#39;échantillonnage n&#39;est pas défini sur l&#39;espace de texture) ajuste la disposition de la carte d&#39;intensité lorsqu&#39;elle est mappée directement aux coordonnées de la spline (voir Entrée des codes de spline).<b></b>

<b>Démarrer l&#39;atténuation</b> *Flotter* (disponible lorsque l&#39;option Utiliser la courbe d&#39;atténuation est définie sur Faux) : multiplicateur pour l&#39;atténuation de l&#39;effet de déformation vers le début de la spline.\
Une valeur de 1 signifie qu&#39;aucune déformation n&#39;est appliquée au début de la spline.

<b>Fin de l&#39;atténuation</b> *Flotter* (disponible lorsque l&#39;option Utiliser la courbe d&#39;atténuation est définie sur Faux) : multiplicateur pour l&#39;atténuation de l&#39;effet de déformation vers l&#39;extrémité de la spline.\
Une valeur de 1 signifie qu&#39;aucune déformation n&#39;est appliquée à l&#39;extrémité de la spline.<b></b>

<b>Recalculer les tangentes</b> *Booléen* Lorsque la valeur est True, les tangentes d’une spline sont recalculées après l’application de l’effet de déformation.\
Cela garantit que les tangentes de la spline restent cohérentes avec sa trajectoire lorsqu’elles sont utilisées dans des nœuds tels que la Dispersion sur la spline ou le mappeur de flux de spline.

+++Prévisualiser
<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Afficher l&#39;enveloppe de Thickness</b> *Booléen*\
Affiche des lignes supplémentaires sur les thickness de la spline.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness de la visualisation de la spline en pixels dans la sortie d&#39;aperçu.

<b>Intensité de l&#39;aperçu de l&#39;arrière-plan</b> *Flotter*\
Valeur multipliée par rapport à l’image d’entrée Aperçu en arrière-plan.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/SplineWarp-Demo.gif "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">



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
