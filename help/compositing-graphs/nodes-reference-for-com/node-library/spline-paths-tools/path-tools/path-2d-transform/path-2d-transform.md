---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation 2D de tracé pour transformer des tracés à l’aide d’opérations de translation, de rotation et de mise à l’échelle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation 2D du tracé
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Transformation 2D du tracé

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/path-2d-transform-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Transforme les tracés à l’aide d’un widget.

</td>
</tr>
</table>

## Connecteurs d’entrée

<b>Tracés</b> *Couleur*\
Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre nœud de traitement de tracé.

## Connecteurs de sortie

<b>Tracés</b> *Couleur*\
Les tracés transformés. Vous pouvez utiliser [Prévisualiser les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) pour vous faire une idée de ce que le résultat représente, utiliser un autre nœud de traitement des tracés ou l&#39;entrer dans un [Tracés de la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour continuer à le traiter en tant que splines.

## Paramètres

<b>Matrice de transformation</b> *Float4*\
Matrice de transformation appliquée aux splines. Trois modes de modification des paramètres de matrice sont disponibles :\
*- Widget de transformation :* ajustez les poignées du widget affiché dans la [Vue 2D](../../../../../../interface/2d-view/2d-view.md) lorsque le nœud de transformation 2D spline est sélectionné ;\
*- Rotation/Étirement :* contrôlez individuellement la rotation et l&#39;étirement des splines. Notez que les valeurs sont toujours appliquées par rapport à la transformation courante. Par exemple, si vous appliquez une largeur de 50 % deux fois, vous obtenez une largeur de 25 %.\
*- Valeurs de matrice :* Cliquez sur le bouton <b>Modifier les valeurs de matrice</b> pour saisir directement les valeurs numériques brutes de la matrice.

<b>Décalage</b> *Float2*\
Applique un décalage de position aux splines en X (horizontal) et Y (vertical).

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
