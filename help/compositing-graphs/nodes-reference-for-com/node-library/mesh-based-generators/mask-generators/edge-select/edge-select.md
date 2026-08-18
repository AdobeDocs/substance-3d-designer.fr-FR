---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Utilisez le nœud de sélection d'arête pour générer des masques en sélectionnant des arêtes de maillage pour créer des effets d'usure et de vieillissement basés sur les arêtes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Select
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Edge Select

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## Edge Select

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque est le meilleur moyen de sélectionner n&#39;importe quel type de bord en fonction de la courbure. Convexe, Concave à n&#39;importe quel niveau ou contraste peut être isolé, fournissant un excellent raccourci pour éviter de le faire manuellement via un [nœud Levels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour mettre en surbrillance les contours. Obligatoire !
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit la quantité totale de mise en surbrillance des contours pour les modes Convexe et Concave.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste de la mise en surbrillance pour les modes Convexe et Concave.
* **Convexe**
  * **Largeur des bords convexes** : *0.0 - 1.0* définit la largeur de la mise en surbrillance des bords convexes. Gardez à l’esprit qu’une légère augmentation de la valeur Lissage peut entraîner un amincissement des bords.
  * **Lissage convexe** : *0.0 - 1.0* Définissez le lissage de la transition pour les bords convexes.
  * **Intensité convexe** : *0,0 - 1,0* définit l&#39;intensité maximale de la mise en surbrillance des contours pour les contours convexes. Définissez la valeur sur 0 pour ne pas mettre en surbrillance.
* **Concave**
  * **Largeur des bords concaves** : *0.0 - 1.0* Définissez la largeur de la mise en surbrillance pour les bords concaves. Gardez à l’esprit qu’une légère augmentation de la valeur Lissage peut entraîner un amincissement des bords.
  * **Lissage concave** :*0.0 - 1.0* Définissez le lissage de la transition pour les bords concaves.
  * **Intensité concave** : *0,0 - 1,0* Définissez l&#39;intensité maximale de la mise en surbrillance des contours pour les contours concaves. Définissez la valeur sur 0 pour ne pas mettre en surbrillance.

## Exemples d’images

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
