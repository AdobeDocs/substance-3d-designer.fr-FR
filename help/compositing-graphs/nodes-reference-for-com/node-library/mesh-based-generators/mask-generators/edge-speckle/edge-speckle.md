---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Utilisez le nœud Moucheture des bords pour générer des motifs d'usure mouchetés sur les bords du maillage afin de créer des effets d'endommagement des bords réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## Edge Speckle

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente les contours avec une légère moucheté ajoutée pour les séparer. Voir également [Dirt Edge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour la mise en surbrillance des contours. Obligatoire !
* **Masque De Variation** : *Entrée En Niveaux De Gris*\
  Emplacement de masque facultatif utilisé pour masquer les effets du nœud. Activez avec « Remplacer le masque de variation ».
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit la quantité totale de mise en surbrillance des contours.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Sélection des contours** :*0.0 - 1.0* définit l&#39;influence des contours convexes.
* **Variation** : *0.0 - 1.0* Définit l&#39;étendue à laquelle le masque de variation casse l&#39;effet.
* **Remplacer le masque de variation** :*Faux/Vrai* Remplace le masque intégré par un emplacement d&#39;entrée personnalisé.

## Exemples d’images

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
