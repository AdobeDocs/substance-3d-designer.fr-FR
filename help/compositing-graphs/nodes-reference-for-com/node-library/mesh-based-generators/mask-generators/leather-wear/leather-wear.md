---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure du cuir pour générer des masques d'usure sur les surfaces en cuir en fonction de la courbure du maillage et des points de contact.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usure du cuir
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Usure du cuir

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## Usure du cuir

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente l&#39;usure avec un motif en cuir, avec plus d&#39;usure sur les bords en fonction de la courbure. Son fonctionnement est similaire à celui de l&#39;[Edge Wear fibre de verre](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) et ses paramètres sont généralement identiques.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour le placement des contours. Obligatoire !
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour occlure certaines zones. Recommandé, mais pas obligatoire.
* **Entrée Usure/salissures** : *Entrée Niveaux De Gris*\
  Emplacement d&#39;entrée de mappage Usure/salissures facultatif qui peut être basculé via le paramètre « Utiliser l&#39;Usure/salissures personnalisée ».
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau d&#39;usure** : *0,0 - 1,0* Définit le niveau d&#39;usure global, révélateur progressivement.
* **Contraste d&#39;usure** : *0.0 - 1.0* Définit le contraste de l&#39;effet.
* **Quantité d&#39;Usure/salissures** : *0,0 - 1,0* définit la quantité d&#39;usure/salissures (motif de cuir par défaut) à mélanger entre les bords.
* **Masquage de l&#39;Occlusion ambiante** : *0.0 - 1.0* Définit la mesure dans laquelle l&#39;IA masque les effets d&#39;usure.
* **Épaisseur de courbure** : *0.0 - 1.0* Définit la mesure dans laquelle les bords de la courbure affectent le résultat final. Même si la valeur est définie sur 0, vous avez toujours besoin d&#39;une courbe de courbure.
* **Utiliser l&#39;Usure/salissures personnalisée** : *Faux/Vrai* Permet de remplacer le motif en cuir par défaut intégré. Utilisez plutôt un emplacement d’entrée personnalisé.

## Exemples d’images

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>
