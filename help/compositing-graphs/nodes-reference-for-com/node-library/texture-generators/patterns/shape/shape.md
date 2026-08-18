---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Utilisez le nœud Forme pour générer des formes géométriques de base afin de créer des motifs et des textures dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Forme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## Forme

**Entrée :** *Générateurs de textures**/Motifs*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère diverses formes procédurales, avec des options pour modifier les formes de base. Les formes sont toujours parfaitement interpolées et de haute précision.

Malgré sa simplicité, il s&#39;agit d&#39;un nœud très utile : c&#39;est la pierre angulaire de la plupart des générations de Heightmap procédurales ! En combinant des formes simples avec des nœuds de transformation, vous pouvez créer une forme Heightmap entièrement procédurale, beaucoup plus précise qu’une image bitmap.

## Paramètres

* **Mosaïque** : *1 - 16*\
  Définit le nombre de fois où le résultat doit se produire.
* **Motif** : *Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Gradation, Ondes, Demi-Cloche, Cloche Arquée, Croissant, Capsule, Cône*, Hémisphère**\
  Sélectionne la forme de motif à utiliser.
* **Spécifique Au Motif** : *0.0 - 1.0*\
  Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné.
* **Échelle** :*0.0 - 1.0* met à l’échelle la forme entière.
* **Taille** :*0.0 - 1.0* Permet une mise à l’échelle non uniforme sur l’axe X ou Y.
* **Angle** : *0.0 - 1.0* Fait pivoter la forme entière.
* **Rotation 45°** : *Faux/Vrai* Rotation à 45 degrés prédéfinis.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.
* **Carrelage non carré**&#x200B;**:** *Faux/Vrai*Lorsque l’Extension non carrée est activée, la forme est carrelée sans être écrasée.

## Exemples d’images

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
