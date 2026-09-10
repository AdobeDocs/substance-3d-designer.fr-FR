---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: Utilisez le nœud Sélection de tracés pour sélectionner et filtrer des tracés spécifiques dans une liste de tracés en fonction de critères.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sélection de tracés
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# Sélection de tracés

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](paths-select.resources/paths-select-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Isolez un tracé parmi les multiples contenus dans les tracés.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Libellé</b> <i>Type</i> | Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre nœud de traitement de tracé. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | L’entrée Tracés comporte un seul tracé. Vous pouvez utiliser [Prévisualiser les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) pour vous faire une idée de ce que le résultat représente, utiliser un autre nœud de traitement des tracés ou l&#39;entrer dans un [Tracés de la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour continuer à le traiter en tant que splines. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode de sélection</b> <i>Nombre entier</i> | La méthode utilisée pour sélectionner les chemins :<br>*- Par ID :* sélectionne le chemin dans la liste dont l&#39;index correspond à celui spécifié dans <b>ID de chemin</b>;<br>*- Par longueur :* sélectionne les chemins dont la longueur est supérieure ou inférieure au seuil spécifié dans <b>Longueur cible</b>. |
| <b>Path ID</b> <i>Nombre entier</i> (disponible lorsque <b>Mode de sélection</b> est défini sur *Par ID*) | Index du chemin sélectionné.<br>Une valeur supérieure au nombre de chemins dans <b>Chemins d&#39;accès *entraîne*</b> une sortie vide. |
| <b>Longueur supérieure ou inférieure ?</b> <i>Booléen</i> (disponible lorsque le <b>mode de sélection</b> est défini sur *Par longueur*) | Détermine si la sélection doit inclure une longueur supérieure ou inférieure à la <b>longueur cible</b>. |
| <b>Longueur cible</b> <i>Flottant</i> (disponible lorsque <b>Mode de sélection</b> est défini sur *Par longueur*) | Seuil de longueur utilisé pour sélectionner les splines. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
