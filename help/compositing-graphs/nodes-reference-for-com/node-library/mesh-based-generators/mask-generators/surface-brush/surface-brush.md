---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Utilisez le nœud Pinceau de surface pour générer des masques en fonction de l'orientation de la surface afin de créer des effets directionnels d'usure.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pinceau de surface
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# Pinceau de surface

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## Pinceau de surface

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente un effet intéressant de brossage du métal sur une surface de l&#39;objet, occulté par la géométrie de l&#39;objet et l&#39;AO.

## Paramètres

### Entrées

* **Espace universel normal** : *entrée de couleur*
* **Courbure** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Position** : *Entrée En Niveaux De Gris*
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Niveau** : *0.0 - 1.0*\
  Définit le niveau d’effet global, progressivement révélateur.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.
* **Longueur Scratches** : *0.0 - 8.0* Définit la longueur des rayures. Les valeurs plus faibles sont plus semblables à des points, les valeurs plus élevées sont des traits longs.
* **Axe d&#39;occlusion** : *axe X, Y, Z, aucun* de l&#39;objet qui doit recevoir les rayures. Ne modifie pas le sens des rayures.
* **Intensité de l&#39;axe d&#39;occlusion** : *0.0 - 1.0* Intensité de l&#39;effet d&#39;occlusion de l&#39;axe.
* **Occlusion** : *0,0 - 1,0* Force de l&#39;AO sur les rayures d&#39;occlusion.
* **Intensité de la netteté** : *0,0 - 1,0* Définissez la quantité de post-netteté à appliquer aux rayures.

## Exemples d’images

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
