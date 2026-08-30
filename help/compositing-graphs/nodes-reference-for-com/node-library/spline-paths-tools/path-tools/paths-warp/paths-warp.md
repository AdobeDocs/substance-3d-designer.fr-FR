---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation de tracés pour déformer des textures le long de courbes de tracé afin de créer des motifs courbes et organiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation des tracés
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Déformation des tracés

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](paths-warp.resources/paths-warp-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Déformez les tracés d&#39;entrée en fonction de l&#39;<b>Entrée de dégradé</b>. (Même effet que le nœud [Déformation](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).)

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre nœud de traitement de tracé. |
| <b>Entrée de dégradé</b> <i>Niveaux de gris</i> | Entrée de type height contrôlant à la fois la quantité et la direction de la déformation. (Même effet que le nœud [Déformation](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).) |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Les tracés transformés. Vous pouvez utiliser [Prévisualiser les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) pour vous faire une idée de ce que le résultat représente, utiliser un autre nœud de traitement des tracés ou l&#39;entrer dans un [Tracés de la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour continuer à le traiter en tant que splines. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>Flotter</i> | Le paramètre <b>Intensité</b> définit l&#39;intensité de la déformation. |
| <b>Nombre d’étapes</b> <i>Nombre entier</i> | Utilisez une valeur plus élevée pour déformer les tracés d’entrée par petits incréments multiples.<br>Cela peut empêcher le tracé de se croiser, en particulier lors de l&#39;utilisation de valeurs <b>Intensité</b> élevées. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="paths-warp.resources/PathsWarp-Variant1-After.jpg" alt="PathsWarp-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="paths-warp.resources/PathsWarp-Variant2-After.jpg" alt="PathsWarp-Variant2-After">
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

![Exemple de nœud 1](paths-warp.resources/PathsWarp-Demo1.gif "Exemple de nœud 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
