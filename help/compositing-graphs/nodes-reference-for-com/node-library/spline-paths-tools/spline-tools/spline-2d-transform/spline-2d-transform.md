---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-2d-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation 2D de spline pour transformer des splines avec des opérations de translation, de rotation et de mise à l'échelle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation 2D spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Transformation 2D spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-2d-transform-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique une transformation globale à toutes les splines d&#39;entrée, y compris l&#39;inversion de leur direction.

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

<b>Inverser la direction</b> *Booléen* Inverse la direction de la spline.

<b>Matrice de transformation</b> *Float4* La matrice de transformation appliquée aux splines.\
Trois modes de modification des paramètres de matrice sont disponibles :\
*- Widget de transformation* : ajustez les poignées du widget affiché dans la vue 2D lorsque le nœud de transformation 2D spline est sélectionné ;\
*- Rotation/Étirement* : contrôle individuel de la rotation et de l&#39;étirement des splines. Notez que les valeurs sont toujours appliquées par rapport à la transformation courante. Par exemple, si vous appliquez une largeur de 50 % deux fois, vous obtenez une largeur de 25 %.\
*- Valeurs de matrice* : cliquez sur le bouton Modifier les valeurs de matrice pour saisir directement les valeurs numériques brutes de la matrice.

<b>Décalage</b> *Float2* Applique un décalage de position aux splines en X (horizontal) et Y (vertical).

+++Prévisualiser
<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Afficher l&#39;enveloppe de Thickness</b> *Booléen*\
Affiche des lignes supplémentaires sur les thickness de la spline.

<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness de la visualisation de la spline en pixels dans la sortie d&#39;aperçu.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant2-After.jpg" alt="Spline2DTransform-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-After.jpg" alt="Spline2DTransform-Variant1-After">
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

![Exemple de nœud 1](../../../../../../assets/Spline2DTransform-Demo1.gif "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
