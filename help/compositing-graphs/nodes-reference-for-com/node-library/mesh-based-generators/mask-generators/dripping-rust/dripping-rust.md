---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Utilisez le nœud Rouille d'égouttage pour générer des motifs d'égouttement de rouille en fonction de la géométrie du maillage et de la direction de la gravité.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rouille goutte-à-goutte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# Rouille goutte-à-goutte

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## Rouille goutte-à-goutte

**Entrée :** *Générateurs basés sur le maillage**/Générateurs de masques*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Similaires aux [masques dynamiques](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) dans [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Ce masque représente des flocons de rouille et des taches, avec des fuites qui s&#39;écoulent.

## Paramètres

### Entrées

* **Courbure** : *Entrée en niveaux de gris*\
  Mappage cuit ou généré pour faciliter le placement des rouilles.
* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Mappage cuit ou généré pour faciliter le placement des rouilles.
* **Position** : *Entrée En Niveaux De Gris*\
  Carte préparée ou générée pour les directions de goutte à goutte.
* **Masque (facultatif)** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.

### Paramètres

* **Répartition des Rouilles** : *0,0 - 1,0* Contrôle principal de la quantité de rouille.
* **Contraste de Rouille** : *0,0 - 1,0* définit la quantité de contraste dans les taches de rouille générées (n&#39;affecte pas les gouttes).
* **Smoothness d&#39;étalement** : *0,0 - 1,0* quantité d&#39;effet de flou/maculage à appliquer aux taches de rouille.
* **Intensité des gouttes** : *0,0 - 1,0* Définit la force et la longueur des gouttes des taches.
* **Smoothness des gouttes** : *0,0 - 1,0* quantité de flou et de lissage à appliquer aux gouttes.
* **Quantité d’échantillons goutte** : *0 - 32* définit le niveau de qualité (étapes) de l’effet goutte-à-goutte. A un léger effet sur la vitesse.

## Exemples d’images

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>
