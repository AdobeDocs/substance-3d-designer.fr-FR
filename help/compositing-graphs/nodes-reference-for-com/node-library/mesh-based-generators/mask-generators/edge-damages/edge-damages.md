---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: Utilisez le nœud Endommagement des contours pour générer des masques d'endommagement sur les contours du maillage afin de créer des effets d'usure et de cassure réalistes des contours.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dommages aux contours
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# Dommages aux contours

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-damages.png){width="128px"}

## Dommages aux contours

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente les dommages infligés aux bords relevés et convexes en fonction de la courbure et de l&#39;AO cuit.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour le placement de l’effet. Obligatoire !
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour le placement de l’effet. Obligatoire !
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Quantité d’endommagement des bords à appliquer.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Intensité des dommages** : *0,0 - 1,0* Passe d’un aspect écaillé et cohérent à un aspect chaotique, rayé et fortement endommagé.

## Exemples d’images

![](../../../../../../assets/edge-damages-ex.gif)

</td>
</tr>
</table>
