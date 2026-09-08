---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
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
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

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

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br>- Signe : la spline est fermée (négative) ou ouverte (positive);<br>- Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines d&#39;entrée. |
| <b>Color Map</b> <i>Couleur</i> | Image couleur d&#39;entrée à mapper sur les splines d&#39;entrée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Couleur</b> <i>Niveaux de gris</i> | Résultat du mappage de l’image couleur d’entrée sur les splines de l’arrière-plan, en tant qu’image couleur. |
| <b>Height</b> <i>Niveaux de gris</i> | Height des splines mappées sur les splines, sous forme d&#39;image en niveaux de gris. |
| <b>UV</b> <i>Couleur</i> | Les UV (c’est-à-dire les coordonnées) de l’image mappée, codés dans les canaux rouge (U) et vert (V) d’une image couleur. |
| <b>Masquer</b> <i>Niveaux de gris</i> | Masque du placage sur les splines. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité de segments</b> <i>Nombre entier</i> | Les splines sont simplifiées en segments avant que les coordonnées de l’image ne les traversent. Plus le nombre de segments est élevé, plus le placage le long des courbes est fluide. |
| <b>Réduction des UV</b> <i>Booléen</i> | Ajuste la méthode utilisée pour interpoler les coordonnées d’image d’une spline à la suivante afin de minimiser le étiré lorsque la distance entre les splines est irrégulière. |
| <b>Échelle UV</b> <i>Float2</i> | Règle l’échelle des coordonnées de l’image. Plus la valeur est élevée, plus la densité de mosaïque de l’image est élevée. |
| <b>Rotation UV</b> <i>Flotter</i> | Fait pivoter les coordonnées de l’image autour de leur centre. |
| <b>Couleur d&#39;arrière-plan</b> <i>Float4</i> | Couleur d’arrière-plan dans l’image de sortie. |

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
