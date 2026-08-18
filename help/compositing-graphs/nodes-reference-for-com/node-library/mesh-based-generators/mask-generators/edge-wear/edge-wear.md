---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Edge Wear pour générer des masques d'usure sur les bords du maillage afin de créer des effets réalistes d'endommagement des bords et d'altération.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce nœud représente l&#39;usure des bords des objets. Il a pas mal de paramètres, mais n&#39;est pas le plus facile à utiliser : nous vous recommandons de jouer et de se faire une idée des choses. Le nœud est assez puissant, bien qu&#39;aucun masque de remplacement personnalisé ne puisse être effectué.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit l’étendue totale de l’effet.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Seuil** : *0,0 - 1,0* Similaire à Niveau, définit l&#39;étendue totale de l&#39;effet.
* **Largeur des contours** : *0.0 - 1.0* Définit l&#39;intégralité de l&#39;effet de mise en surbrillance. Réduisez pour les rendre plus clairsemés.
* **Trouble** : *0,0 - 1,0*\
  Définit la quantité de bruit à intégrer pour rompre le smoothness.

## Exemples d’images

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
