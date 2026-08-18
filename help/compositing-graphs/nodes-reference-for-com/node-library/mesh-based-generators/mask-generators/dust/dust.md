---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Utilisez le nœud Dust pour générer des masques d’accumulation de dusts basés sur la géométrie du maillage afin de créer des effets de dust et de craie réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# Dust

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## Dust

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente le dust accumulé dans les zones obstruées, les zones basses, ainsi que seulement dans les zones tournées vers le haut. Nécessite une atmosphère ambiante et des normales de l&#39;espace universel correctes pour fonctionner.

## Paramètres

### Entrées

* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour le placement du dust. Obligatoire !
* **Espace universel normal** : *entrée de couleur*\
  Map bakée utilisée pour le placement du dust. Obligatoire !
* **Bruit** :*Entrée En Niveaux De Gris*\
  La courbe de dust personnalisée (facultatif) s’affiche uniquement lorsque l’option Remplacer le bruit est définie sur Vrai.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit le montant total du dust.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du dust.
* **Quantité d&#39;Occlusion** : *0,0 - 1,0* définit l&#39;influence de l&#39;AO ; plus de dust apparaîtra dans les zones occultées.
* **Opacité du bruit** : *0.0 - 1.0* Définit la quantité de bruit visible dans les zones poussiéreuses.
* **Remplacer le bruit** : *Faux/Vrai* Définissez pour utiliser l&#39;entrée de mappage de dust personnalisée.

## Exemples d’images

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>
