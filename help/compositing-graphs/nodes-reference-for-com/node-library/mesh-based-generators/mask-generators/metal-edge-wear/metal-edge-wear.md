---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Edge Wear de métal pour générer des masques d'usure sur les bords métalliques en fonction de la courbure et de la position du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de métal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Edge Wear de métal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## Edge Wear de métal

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente l&#39;usure des bords d&#39;un objet métallique, avec des rayures et des copeaux apparaissant sur les bords relevés convexes, potentiellement masqués par les zones sombres de l&#39;AO cuites.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Entrée Usure/salissures** : *Entrée Niveaux De Gris*
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Espace universel normal** : *entrée de couleur*
* **Position** : *Entrée Couleur*

### Paramètres

* **Niveau d&#39;usure** : *0,0 - 1,0* Définit la quantité totale d&#39;usure, révèle progressivement.
* **Contraste d&#39;usure** : *0.0 - 1.0* Définit le contraste du résultat final.
* **Smoothness des contours** :*0.0 - 16.0* définit le smoothness de la atténuation à partir des contours de la courbure.
* **Quantité d&#39;Usure/salissures** : *0,0 - 1,0* définit la quantité d&#39;usure/salissures à mélanger entre les contours.
* **Échelle d&#39;Usure/salissures** : *1 - 16* définit l&#39;échelle de l&#39;Usure/salissures.
* **Masquage de l&#39;Occlusion ambiante** :*0.0 - 1.0* Définit la quantité d&#39;effet de l&#39;IA sur l&#39;effet final, les zones sombres étant masquées.
* **Épaisseur de courbure** :*0.0 - 1.0* définit l&#39;effet que les bords convexes de la courbure ont sur l&#39;effet final.
* **Utiliser l&#39;Usure/salissures personnalisée** : *Faux/Vrai* Active un emplacement d&#39;entrée de mappage Usure/salissures personnalisé.
* **Utiliser triplanaire** :*faux/vrai* Activez la projection [triplanaire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) pour masquer les coutures.
* **Contraste de fusion triplanaire** : *0.0 - 1.0* définit le contraste de fusion pour la projection triplanaire.

## Exemples d’images

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
