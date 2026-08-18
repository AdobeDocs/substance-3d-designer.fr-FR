---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur du mappeur UV pour mapper les textures colorimétriques le long des splines pour la génération de textures procédurales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur du mappeur UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Couleur du mappeur UV

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/uv-mapper-color-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Mappe l’image couleur d’entrée à l’aide des coordonnées fournies dans l’entrée UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Voir aussi [Niveaux de gris du mappeur UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md).

## Connecteurs d’entrée

<b>UV</b> *Couleur* Les coordonnées de l&#39;image codées dans les couches rouge (U) et verte (V) d&#39;une image couleur.

<b>Entrée</b> *Couleur* L&#39;image couleur qui doit être mappée aux coordonnées fournies dans l&#39;entrée UV.

## Connecteurs de sortie

<b>Sortie</b> *Couleur* Résultat du mappage de l’image d’entrée à l’aide des coordonnées UV d’entrée, en tant qu’image couleur.

## Paramètres

<b>Couleur d&#39;arrière-plan</b> *Float4* Couleur d&#39;arrière-plan de l&#39;image de sortie.\
L’arrière-plan est visible dans les zones de l’image où les UV ne sont pas définis (c’est-à-dire que la valeur est (0, 0, 0, 0)).

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nœud dans le graphique](../../../../../../assets/UVMapperColor-Graph.jpg "Nœud dans le graphique")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
