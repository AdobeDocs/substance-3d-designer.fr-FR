---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Utilisez le nœud Lumière pour générer des masques en fonction des conditions d’éclairage du maillage afin de créer des variations de matériau réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lumière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# Lumière

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## Lumière

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque est un peu différent des autres générateurs : il ne fait que de faux éclairages, basés sur la carte normale de l&#39;espace mondial, renvoyant un masque « lightmap » en noir et blanc.

## Paramètres

* **Angle horizontal** : *0,0 - 1,0* définit l’angle horizontal de la fausse lumière.
* **Angle vertical** : *0.0 - 1.0* Définit l’angle vertical de la fausse lumière.
* **Éclat des tons clairs** : *0,0 - 0,999* définit l&#39;étendue de retrait de la zone en surbrillance.
* **Niveau de surbrillance** : *0.0 - 1.0* définit le niveau de luminosité de la zone mise en surbrillance.

## Exemples d’images

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
