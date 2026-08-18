---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Utilisez le nœud de 3D linear gradient pour créer des dégradés linéaires basés sur la position universelle 3D pour les effets spatiaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D linear gradient

**Entrée :** *Générateurs de textures**/Motifs*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Crée un dégradé volumique basé sur le mappage de position d’entrée. Génère efficacement une transition du noir au blanc entre 2 points dans l’espace 3D. Destiné à être utilisé uniquement avec le moteur GPU.

Voir également [Masque de volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) pour obtenir un effet similaire.

## Paramètres

* **Mode de position des points** : *Positions UV, positions dans l&#39;espace universel* Choisissez si les points de dégradé fonctionnent dans l&#39;espace UV (cela fonctionne mieux lorsque vous les définissez en vue 2D) ou dans les coordonnées 3D, si vous souhaitez saisir manuellement une position exacte.
* **Point 1** :\
  Point de départ du dégradé. Il peut s’agir de coordonnées 2D ou 3D basées sur le mode Position.
* **Point 2** :\
  Point de fin du dégradé. Il peut s’agir de coordonnées 2D ou 3D basées sur le mode Position.
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat.

## Exemples d’images

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
