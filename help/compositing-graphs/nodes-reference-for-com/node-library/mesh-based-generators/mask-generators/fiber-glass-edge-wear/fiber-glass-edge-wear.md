---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Edge Wear Fibre Glass pour générer des masques d'usure sur les bords en fibre de verre en fonction de la courbure du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear en fibre de verre
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Edge Wear en fibre de verre

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## Edge Wear en fibre de verre

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Représente un masque spécifiquement destiné à une usure de type fibre de verre, qui pourrait éventuellement être utilisé pour un tissu. En raison de la nature très mosaïque et répétitive des fibres, le mélange triplanaire peut éventuellement être activé.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour la mise en surbrillance des contours. Obligatoire !
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour masquer les zones occultées. Non requis, mais certainement recommandé.
* **Entrée Usure/salissures** : *Entrée Niveaux De Gris*\
  Emplacement personnalisé en option pour remplacer le motif de fibre.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Espace universel normal** : *entrée de couleur*\
  Utilisé uniquement pour le format triplanaire.
* **Position** : *Entrée Couleur*\
  Utilisé uniquement pour le format triplanaire.

### Paramètres

* **Niveau d&#39;usure** :*0,0 - 1,0* Comme un [histogramme de balayage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), révèle progressivement l&#39;usure.
* **Contraste d&#39;usure** : *0,0 - 1,0* définit le contraste total de l&#39;effet.
* **Smoothness des contours** :*0.0 - 16.0* définit le fond perdu/le flou à partir des contours mis en surbrillance.
* **Quantité d&#39;Usure/salissures** : *0,0 - 1,0* Définit la proportion de l&#39;effet de fibre à fusionner entre les contours. Réglez-le avec le niveau d’usure pour obtenir un contrôle maximal.
* **Masquage de l&#39;Occlusion ambiante** : *0.0 - 1.0* Définit l&#39;influence de l&#39;AO sur le masquage de l&#39;effet.
* **Épaisseur de courbure** :*0.0 - 1.0* définit le degré d&#39;influence des bords convexes à partir de la courbe.
* **Utiliser l&#39;Usure/salissures personnalisée** : *Faux/Vrai* Remplace les fibres intégrées par un mappage personnalisé.
* **Utiliser triplanaire** : *Faux/Vrai* Permet à [triplanaire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) de masquer les coutures.
* **Contraste de fusion triplanaire** : *0.0 - 1.0* contrôle le contraste de l&#39;effet triplanaire.

## Exemples d’images

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>
