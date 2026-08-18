---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit simplifié 3D pour générer des motifs de bruit simplex 3D afin de créer des textures volumiques lisses et naturelles.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bruit simplifié 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Bruit simplifié 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## Bruit simplifié 3D

**Entrée :** *Générateurs De Texture**/Bruits*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un bruit de procédure lorsqu&#39;un mappage de position cuit est branché dans l&#39;emplacement d&#39;entrée. Il est destiné à être utilisé uniquement avec le moteur GPU.\
Similaire au [bruit de Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), mais plus rapide et plus simple, pour les cas où les performances et la vitesse sont importantes.

Ce bruit peut être testé avec [Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) en entrée au lieu d&#39;une map bakée réelle (comme illustré dans l&#39;exemple ci-dessous).

## Paramètres

* **Échelle** : *0,0 - 64,0*\
  Définissez l’échelle globale de l’effet.
* **Taille** :*0.0 - 2.0* Effectuez une mise à l’échelle non uniforme sur les axes X, Y et Z séparément.

## Exemples d’images

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
