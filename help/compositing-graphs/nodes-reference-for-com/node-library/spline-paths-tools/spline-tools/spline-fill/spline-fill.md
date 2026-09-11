---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: Utilisez le nœud Remplissage de spline pour remplir les zones définies par des splines fermées avec des textures ou des couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Remplissage spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Remplissage spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-fill.resources/spline-fill-icon.png "Icône de nœud")

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

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br>- Signe : la spline est fermée (négative) ou ouverte (positive);<br>- Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Entier</i> | Nombre de splines d&#39;entrée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Image finale du remplissage des splines d’entrée avec un blanc plat sur un arrière-plan noir plat. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-Before.jpg" alt="SplineFill-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-After.jpg" alt="SplineFill-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](spline-fill.resources/SplineFill-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>
