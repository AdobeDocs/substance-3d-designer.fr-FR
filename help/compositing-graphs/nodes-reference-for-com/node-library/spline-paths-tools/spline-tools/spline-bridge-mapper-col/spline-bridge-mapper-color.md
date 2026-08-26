---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur du mappeur de pont de splines pour relier les textures entre deux splines avec le mappage de couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur du mappeur de pont de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Couleur du mappeur de pont de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-bridge-mapper-color-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Etablit une correspondance entre une image couleur et une liste de splines d&#39;entrée, de sorte que l&#39;image traverse les splines dans l&#39;ordre.

</td>
</tr>
</table>

>[!TIP]
>
> La mise en correspondance va de la première spline de la liste à la dernière et traverse les splines intermédiaires en suivant rigoureusement l&#39;ordre de ces splines dans la liste.
> 
> Par conséquent, vous devez être attentif à l&#39;ordre dans lequel vous ajoutez des splines ensemble au préalable.

>[!NOTE]
>
> Voir aussi [Mappeur de pont spline en niveaux de gris](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md).

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

<b>Color Map </b>*Color* Image couleur d&#39;entrée qui doit être mappée sur les splines d&#39;entrée.

## Connecteurs de sortie

<b>Couleur</b> *Niveaux de gris* Résultat du mappage de l&#39;image couleur d&#39;entrée sur les splines sur l&#39;arrière-plan, en tant qu&#39;image couleur.

<b>Height</b> *Niveaux de gris* L&#39;height des splines mappées sur les splines, sous forme d&#39;image en niveaux de gris.

<b>UV</b> *Couleur* Les UV (c’est-à-dire les coordonnées) de l’image mappée, codés dans les canaux rouge (U) et vert (V) d’une image couleur.

<b>Masquer</b> *Niveaux de gris* Masque du mappage sur les splines.

## Paramètres

<b>Quantité de segments</b> Les splines *entières* sont simplifiées en segments avant que les coordonnées de l&#39;image ne les traversent.\
Plus le nombre de segments est élevé, plus le placage le long des courbes est fluide.

<b>Réduction des UV</b> *Booléen* Ajuste la méthode utilisée pour interpoler les coordonnées d&#39;image d&#39;une spline à la suivante afin de minimiser l&#39;étirement lorsque la distance entre les splines est inégale.

<b>Échelle UV</b> *Float2* Ajuste l’échelle des coordonnées de l’image. Plus la valeur est élevée, plus la densité de mosaïque de l’image est élevée.

<b>Rotation UV</b> *Flottant* Fait pivoter les coordonnées de l&#39;image autour de leur centre.

<b>Couleur d&#39;arrière-plan</b> *Float4* La couleur de l’arrière-plan dans l’image de sortie.

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineBridgeMapperColor-Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/SplineBridgeMapperColor-Variant1-After1.jpg "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineBridgeMapperColor-Graph.jpg "Exemple de nœud 2")

</td>
</tr>
</table>
