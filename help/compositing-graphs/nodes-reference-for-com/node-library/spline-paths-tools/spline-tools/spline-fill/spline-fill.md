---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: Utilisez le nœud Remplissage de spline pour remplir des zones définies par des splines fermées avec des textures ou des couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Remplissage spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Remplissage spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-fill-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Remplit l&#39;intérieur des splines d&#39;entrée avec du blanc uni. L&#39;extérieur est rempli de noir uni.

Les splines ouvertes sont fermées par une ligne droite du début à la fin. Les intersections où la spline se croise sont résolues en inversant les côtés intérieur et extérieur des lignes à ces jonctions.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Il n&#39;est pas recommandé d&#39;utiliser ce nœud sur les splines qui ne se trouvent pas dans la mosaïque [0 ,1]. Le processus de remplissage n&#39;est pas fiable dans ce cas.

## Connecteurs d’entrée

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

<b>Sortie</b> *Niveaux de gris*\
Image finale du remplissage des splines d’entrée avec un blanc plat sur un arrière-plan noir plat.

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-Before.jpg" alt="SplineFill-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-After.jpg" alt="SplineFill-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineFill-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>
