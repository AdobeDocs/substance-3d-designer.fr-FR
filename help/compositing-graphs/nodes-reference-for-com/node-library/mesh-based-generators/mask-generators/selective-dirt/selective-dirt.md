---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Utilisez le nœud Dirt sélectif pour générer des masques d'accumulation de dirt sélectif basés sur la géométrie du maillage pour un vieillissement réaliste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt sélectif
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# Dirt sélectif

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## Dirt sélectif

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) représente un effet de dirt simple sur les contours convexes.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Masque De Variation** : *Entrée En Niveaux De Gris*\
  Carte de variation facultative, qui peut être activée via des paramètres.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit le niveau total de l’effet, qui s’affiche progressivement.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Variation** : *0,0 - 1,0* définit la quantité de variation/usure/salissures à fusionner avec l&#39;effet.
* **Remplacer le masque de variation** :*Faux/Vrai* Permet de remplacer la variation par un emplacement d&#39;entrée personnalisé.

## Exemples d’images

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
