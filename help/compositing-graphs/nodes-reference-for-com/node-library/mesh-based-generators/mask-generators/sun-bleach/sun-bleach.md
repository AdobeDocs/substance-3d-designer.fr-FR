---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: Utilisez le nœud Javel au soleil pour générer des masques basés sur l’exposition au soleil afin de créer des effets réalistes décolorés et estompés au soleil.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Javel solaire
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Javel solaire

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## Javel solaire

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque est similaire à [Lumière](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md), mais prend également en charge l&#39;IA. Il permet d&#39;obtenir un masque qui représente le blanchiment de la lumière et l&#39;atténuation sur un effet.

## Entrées

* **Espace universel normal** : *entrée de couleur*
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

## Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit la quantité totale de blanchiment et déplace l&#39;effet vers le bas.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Occlusion** : *0,0 - 1,0* définit l&#39;influence de l&#39;AO sur le résultat final.

## Exemples d’images

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
