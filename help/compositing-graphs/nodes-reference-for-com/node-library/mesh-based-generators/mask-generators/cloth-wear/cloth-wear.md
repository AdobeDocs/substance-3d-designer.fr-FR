---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure du tissu pour générer des masques d'usure sur les surfaces du tissu en fonction de la courbure du maillage et des zones de contact.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usure du tissu
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# Usure du tissu

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cloth-wear.png){width="128px"}

## Usure du tissu

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Le masque représente les bords effilochés sur les matériaux en tissu. Il utilise une carte de hauteur de détail de tissu qui détermine la plupart de l&#39;aspect ; sans une carte appropriée, l&#39;effet semble très basique.

## Paramètres

### Entrées

* **Height Du Tissu** : *Entrée En Niveaux De Gris*\
  Height pour le motif de tissu uniquement. Il ne s’agit pas de l’height de votre objet (cuit), mais plutôt d’un motif de détail en mosaïque.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Courbure** : *Entrée en niveaux de gris*\
  Courbure cuite/générée pour déterminer les bords relevés.

### Paramètres

* **Quantité de bords nets** : *0,0 - 1,0*
* **Lissage à l’usure** : *0.0 - 5.0* Détermine le degré de flou/douceur des bords usés.

## Exemples d’images

![](../../../../../../assets/cloth-wear-ex.gif)

</td>
</tr>
</table>
