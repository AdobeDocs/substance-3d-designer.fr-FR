---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Polygone 1 pour générer des motifs polygonaux de base avec des côtés et des propriétés personnalisables pour les textures géométriques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Polygone 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---


# Polygone 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/polygon-1-1.png){width="128px"}

## Polygone 1

**Entrée :** *Générateurs de textures**/Motifs*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère une forme polygonale avec de nombreuses options de réglage. Voir [Polygone 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md) pour une version plus simple.

## Paramètres

* **Côtés** : *3 - 32* Définit le nombre de côtés que le polygone doit avoir.
* **Éclatement** :*0.0 - 1.0*&#x200B;éloigne les « tranches » du polygone.
* **Taille du triangle** : *0.0 - 1.0* ajuste la taille des tranches/triangles. Tout réglage peut décomposer la forme, seulement 1,1. est parfaitement connecté !
* **Échelle** :*0.0 - 1.0* met à l’échelle la forme entière en une seule fois.
* **Échelle automatique** :*Faux/Vrai* Ajuste les échelles de sorte que l’ensemble du polygone s’affiche, avec les paramètres par défaut.
* **Rotation** : *0.0 - 1.0* Fait pivoter la forme entière.
* **Dégradé** :*Faux/Vrai* génère des tranches/triangles dégradés au lieu de triangles pleins. Remarque : devient similaire à Polygone 2 lorsque ce paramètre est activé.
* **Inversion de dégradé** :*Faux/Vrai* inverse la direction du dégradé si l’option « Dégradé » est activée.
* **Mosaïque** : *1 - 16*\
  Définit le nombre de fois où le résultat doit se produire.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.
* **Carrelage non carré**&#x200B;**:** *Faux/Vrai*Lorsque l’Extension non carrée est activée, la forme est carrelée sans être écrasée.

## Exemples d’images

![](../../../../../../assets/polygon-1-ex.gif)

</td>
</tr>
</table>
