---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure de la peinture pour générer des masques d’usure de peinture basés sur la géométrie du maillage afin de créer des effets d’écaillage de peinture réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usure de la peinture
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# Usure de la peinture

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## Usure de la peinture

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente l&#39;écaillage de la peinture et l&#39;usure des bords.

## Paramètres

### Entrées

* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Masque De Variation** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit la quantité totale d’usure de la peinture, en la révélant progressivement.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Occlusion** :*0,0 - 1,0* définit l&#39;effet de l&#39;AO cuit sur la prévention de l&#39;usure dans les zones sombres.
* **Rayon** : *0.0 - 2.0* Définit la distance à laquelle l&#39;effet d&#39;écaillage se propage à partir des bords convexes.
* **Variation** : *0,0 - 1,0* Définissez la quantité de variation (usure/salissures) à fusionner avec l&#39;effet.
* **Remplacer le masque de variation** : *Faux/Vrai* Active l&#39;emplacement d&#39;entrée de mappage de variation personnalisée (usure/salissures).

## Exemples d’images

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>
