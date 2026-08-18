---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-blur.html"
breadcrumb-title: ''
description: Utilisez le nœud Flou des bords pour flouter les masques de contour afin de créer des transitions douces et des effets d’usure progressifs basés sur les contours.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flou de contour
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# Flou de contour

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-blur.png){width="128px"}

## Flou de contour

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque met en surbrillance les bords en fonction d&#39;une courbe de courbe plaquée. Il s’agit de l’un des générateurs de masques les plus simples.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour créer l’effet.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit la quantité de mise en surbrillance des contours.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Rayon de flou** : *0.0 - 8.0* Définit le niveau de flou sur les bords mis en surbrillance.

## Exemples d’images

![](../../../../../../assets/edge-blur-ex.gif)

</td>
</tr>
</table>
