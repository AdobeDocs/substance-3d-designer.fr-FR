---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation quadratique sur tracé pour appliquer des transformations quadratiques aux éléments le long des courbes du tracé.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quad Transform on Path
user-guide-description: ''
user-guide-title: ''
source-git-commit: 29dd2e6adc826f63ee26defc0032b0e52d4e30fb
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Quad Transform on Path

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](quad-transform-on-path.resources/quad-transform-on-paths-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Déformez un tracé à l’aide de 4 poignées.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque aux tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre nœud de traitement de *tracé*. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Les tracés transformés. Vous pouvez utiliser [Prévisualiser les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) pour vous faire une idée de ce que le résultat représente, utiliser un autre nœud de traitement des tracés ou l&#39;entrer dans un [Tracés de la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour continuer à le traiter en tant que splines. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>p00</b> <i>Float2</i> | Position de la poignée en haut à gauche. |
| <b>p01</b> <i>Float2</i> | Position de la poignée en haut à droite. |
| <b>p02</b> <i>Float2</i> | Position de la poignée inférieure gauche. |
| <b>p03</b> <i>Float2</i> | Position de la poignée inférieure droite. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant1-After.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant2-After.jpg" alt="QuadTransformOnPaths-Variant2-After">
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

![Exemple de nœud 1](quad-transform-on-path.resources/QuadTransformOnPaths-Demo2.gif "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](quad-transform-on-path.resources/QuadTransformOnPaths-Demo1.gif "Exemple de nœud 2")

</td>
</tr>
</table>
