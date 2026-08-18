---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: Utilisez le nœud Dirt d'arête pour générer des masques d'accumulation de dirt sur les arêtes de maillage afin de créer des effets d'altération des arêtes réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt Edge
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# Dirt Edge

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## Dirt Edge

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente un effet de dirt qui s’accumule autour des contours, en fonction uniquement d’une courbe de référence.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour le placement de l’effet. Obligatoire !
* **Masque De Variation** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud, utilisé uniquement lorsque le paramètre de remplacement est activé.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit le montant du dirt.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Variation** :*0.0 - 1.0* Mélange de la quantité de masquage/rupture à grande échelle qui doit se produire.
* **Remplacer le masque de variation** : *Faux/Vrai*

## Exemples d’images

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>
