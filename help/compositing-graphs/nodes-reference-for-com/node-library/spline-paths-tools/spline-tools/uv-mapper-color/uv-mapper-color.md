---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur du mappeur d'UV pour mapper les textures de couleur le long des splines pour une génération de texture procédurale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur du mappeur d’UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# Couleur du mappeur d’UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](uv-mapper-color.resources/uv-mapper-color-icon.png "Icône de nœud")

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
> Voir aussi [Niveaux de gris du mappeur d&#39;UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>UV</b> <i>Couleur</i> | Coordonnées d’image codées dans les couches rouge (U) et vert (V) d’une image couleur. |
| <b>Entrée</b> <i>Couleur</i> | Image couleur qui doit être mappée aux coordonnées fournies dans l’entrée UV. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Résultat du mappage de l’Image d&#39;entrée à l’aide des coordonnées de l’UV d’entrée, sous la forme d’une image couleur. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Couleur d&#39;arrière-plan</b> <i>Flottant4</i> | Couleur d’arrière-plan de l’image de sortie.<br>L&#39;arrière-plan est visible dans les zones de l&#39;image où les UV ne sont pas définis (c&#39;est-à-dire, la valeur est (0, 0, 0, 0)). |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nœud dans le graphe](uv-mapper-color.resources/UVMapperColor-Graph.jpg "Nœud dans le graphe")
