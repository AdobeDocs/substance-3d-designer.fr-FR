---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Utilisez le nœud Chaussée en arc pour générer des motifs de chaussée en forme d'arc afin de créer des textures de route et de tracé courbes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Chaussée Arc
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Chaussée Arc

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## Chaussée Arc

**Entrée :** *Générateurs de textures**/Motifs*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un motif de pavage en arc de Paris. Cet effet ne peut pas être obtenu avec le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)standard ou le [Mosaïque Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md), d&#39;où ce nœud dédié.

## Paramètres

* **Échelle** : *1 - 8* définit l’échelle/la mosaïque globale.
* **Quantité du motif** : *1 -* 32\
  Définit la quantité de briques utilisées dans chaque arc.
* **Quantité aléatoire du motif** : *0,0 - 1,0*\
  Rend aléatoire la quantité de briques dans chaque arc. A pour effet supplémentaire de donner aux briques différentes échelles.
* **Quantité minimale du motif** : *1 - 10*\
  Contrôle la quantité minimale de briques lors de la sélection aléatoire des arcs.
* **Quantité D&#39;Arcs** : *0 - 20*\
  Définit la quantité d’arcs empilés verticalement. Modifie l’height des briques.
* **Motif** :*Image D&#39;Entrée, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Gradations, Ondes, Demi-Cloche, Cloche Arquée, Croissant, Capsule, Cône*\
  Sélectionne la forme de motif à utiliser.
* **Filtrage Des Images D&#39;Entrée** : *Bilinéaire + Mipmaps, Bilinéaire, Au Plus Proche*
* **Échelle du motif** : *0.0 - 1.0* définit l’échelle pour chaque carreau.
* **Largeur du motif** : *0.0 - 1.0*\
  Définit la largeur de chaque carreau.
* **Height du motif** : *0.0 - 1.0*\
  Définit l’height de chaque mosaïque.
* **Largeur aléatoire du motif** : *0.0 - 1.0*\
  Aléatoire la largeur des carreaux.
* **Aléatoire de l&#39;Height du motif** : *0.0 - 1.0*\
  Aléatoire de l’height de la vignette.
* **Aléatoire de la largeur globale du motif** :*0.0 - 1.0* aléatoire la largeur des carreaux, sans créer d’espaces plus grands entre eux.
* **Diminution de l’Height du motif** :*0.0 - 1.0* contrôle l’écrasement de l’height des carreaux à la fin de chaque arc.
* **Color Random** : *0.0 - 1.0*\
  Aléatoire des couleurs des carreaux.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.

## Exemples d’images

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
