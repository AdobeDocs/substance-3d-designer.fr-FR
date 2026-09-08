---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: Utilisez le nœud Niveaux de gris du mappeur d'UV pour mapper les textures en niveaux de gris le long des splines pour une génération de textures procédurale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappeur d’UV en niveaux de gris
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Mappeur d’UV en niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/uv-mapper-grayscale-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Mappe l’image en niveaux de gris d’entrée en utilisant les coordonnées fournies dans l’entrée d’UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Voir aussi [Couleur du mappeur d&#39;UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>UV</b> <i>Couleur</i> | Coordonnées d’image codées dans les couches rouge (U) et vert (V) d’une image couleur. |
| <b>Entrée</b> <i>Couleur</i> | Image en niveaux de gris qui doit être mappée aux coordonnées fournies dans l&#39;entrée UV. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Résultat du mappage de l’Image d&#39;entrée à l’aide des coordonnées d’UV d’entrée, sous la forme d’une image en niveaux de gris. |

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
      <img src="../../../../../../assets/UVMapperGrayscale-Variant1-After.jpg" alt="UVMapperGrayscale-Variant1-After">
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
      <img src="../../../../../../assets/UVMapper-Variant2-After.jpg" alt="UVMapper-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Exemple de nœud 1](../../../../../../assets/UVMapper-Graph.jpg "Exemple de nœud 1")
