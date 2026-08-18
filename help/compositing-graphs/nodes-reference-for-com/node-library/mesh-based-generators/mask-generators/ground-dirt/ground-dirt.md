---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: Utilisez le nœud Dirt au sol pour générer des masques d’accumulation de dirt en fonction de la position et de l’orientation du maillage par rapport au sol.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt au sol
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Dirt au sol

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## Dirt au sol

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente le dirt qui s&#39;est accumulé de bas en haut, à l&#39;opposé de [Bas en haut](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) ou [Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md). Il n’a pas de mappage personnalisé personnalisé personnalisé personnalisé personnalisé.

## Entrées

* **Position** : *Entrée En Niveaux De Gris*\
  Positionnement ancré sur lequel baser l’effet. Obligatoire !
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

## Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit le niveau d’aspect total du dirt.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Height du Dirt** : *0.0 - 1.0* Définit à quel height (proportionnellement) le dirt doit apparaître.

## Exemples d’images

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
