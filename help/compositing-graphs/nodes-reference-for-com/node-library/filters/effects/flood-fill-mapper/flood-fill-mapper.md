---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Utilisez le nœud Mappeur de Flood Fill pour mapper les valeurs sur les régions connectées à l’aide d’algorithmes de remplissage par diffusion pour le traitement de la texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappeur de mots de Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---


# Mappeur de mots de Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-mapper-gray.png)![](../../../../../../assets/floodfill-mapper-color.png)

## Mappeur de Flood Fill (niveaux de gris)

**Entrée :** *Filtres/Effets*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Le mappeur de Flood Fill permet de remapper un motif ou une texture existants sur chaque cellule à partir d&#39;un [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Elle se distingue des autres conversions Flood Fill comme les [niveaux de gris aléatoires](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) ou les [dégradés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) en ce sens qu&#39;elle ne génère pas de couleurs ou de valeurs unies, mais vous permet d&#39;utiliser vos propres cartes d&#39;entrée. Il peut être considéré comme une sorte de combinaison de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) et de [Mosaïque Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) ou de [Mappeur de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md), car il fournit un certain nombre de contrôles et d&#39;interfaces similaires.

La version Couleur dispose de commandes supplémentaires pour travailler avec les cartes de normales, où elle peut [compenser les rotations des cartes de normales de l&#39;espace tangent](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

## Paramètres

### Entrées

* **Boîte de Flood Fill** : *entrée de couleur* entrée de Flood Fill standard, requise.
* **Entrée de motif 1-8** : *Entrée niveaux de gris/couleur*\
  Entrée d’image de motif personnalisée.
* **Carte de distribution de motif** : *carte d&#39;ID d&#39;entrée en niveaux de gris* pour déterminer quel motif va à quelle cellule. Peut provenir d’un autre mappage de Flood Fill, tel que Flood Fill vers index.
* **Mappage d&#39;échelle** : *entrée en niveaux de gris* mappage pour déterminer l&#39;échelle par cellule.
* **Map rotation** : *entrée en niveaux de gris* mappage pour déterminer la rotation par cellule.
* **Carte de décalage de luminance** : *entrée en niveaux de gris* carte pour définir la luminance par cellule

### Paramètres

* **Mode mosaïque** : *Pas de mosaïque, H+V* Choisissez d&#39;utiliser ou non la mosaïque. Visible uniquement si la taille ou l’échelle est inférieure à 1.
* **Motif**
  * **Numéro d’entrée de motif** : *1 - 8* Définissez la quantité d’entrées de motif personnalisées à utiliser.
  * **Mode de distribution de motif** : *Entrée aléatoire, taille de forme et carte de distribution* Définissez la méthode pour déterminer quel motif est affiché dans une cellule.
  * **Variation de la distribution de motif** : *0.0 - 1.0* Permet une légère variation ou un décalage dans la distribution de motif sans tout modifier via le générateur aléatoire.
* **Taille**
  * **Mode Taille** : *Relatif à la texture, Relatif à la forme BSphere, Relatif à la plus grande forme, Relatif à la plus petite forme, Adapter la forme BBox* Définissez la façon dont la taille du motif dans chaque cellule est déterminée.
  * **Taille** : *0.0 - 1.0* Permet une mise à l’échelle non uniforme du motif.
  * **Échelle** : *0.0 - 1.0*\
    Définissez l’échelle globale (uniforme) de l’effet.
  * **Multiplicateur de mise à l&#39;échelle** : *0.0 - 1.0* Définissez l&#39;influence de la mise à l&#39;échelle facultative.
  * **Échelle aléatoire** : *-1.0 - 1.0* Définissez la quantité de variation aléatoire dans l&#39;échelle du motif.
* **Rotation**
  * **Rotation** : *0,0 - 1,0* Définissez une rotation globale et uniforme pour chaque cellule.
  * **Multiplicateur de Map rotation** : *0.0 - 1.0* Définissez l’influence de la Map rotation facultative.
  * **Rotation aléatoire** : *0.0 - 1.0* Définissez la quantité de rotation aléatoire pour chaque cellule.
  * **Mise à l&#39;échelle automatique de rotation** : *Faux/Vrai* Définissez si un motif doit ajuster son échelle pour s&#39;adapter à l&#39;intérieur d&#39;une cellule lors de la rotation.
* **Position**
  * **Décalage de position** :*0.0 - 1.0* Définissez le décalage de position global pour chaque cellule.
  * **Alignement du décalage de position** : *Texture, motif* Définissez pour aligner le point de décalage 0 sur la cellule du motif ou sur la texture.
  * **Aléatoire de décalage de position** : *0,0 - 1,0* Définissez le degré de randomisation du décalage de position par cellule.
* **Couleur** (uniquement pour la version en niveaux de gris)
  * **Plage de luminance** :*0.0 - 1.0* Définit le contraste global sur la texture, où 0 devient gris moyen.
  * **Aléatoire de gamme de luminance** : *0,0 - 1,0* définit le degré de randomisation pour la gamme de luminance.
  * **Décalage de luminance** : *-1.0 - 1.0* Définit le décalage de la luminance, en agissant comme un contrôle de luminosité.
  * **Décalage de luminance aléatoire** : *0.0 - 1.0* définit le degré de randomisation du décalage de luminance.
  * **Multiplicateur de décalage de la carte de luminance** : *0.0 - 1.0* Définit l&#39;influence de la carte de décalage de luminance facultative.
  * **Couleur d&#39;arrière-plan** : *(valeur Niveaux de gris)*Définit la couleur d&#39;arrière-plan sur laquelle les textures sont fusionnées.
* **Couleur** (uniquement pour la version couleur)
  * **Est une carte normale** : *Faux/Vrai* Défini pour interpréter l&#39;entrée de motif comme une carte normale. Permet de compenser et de corriger la rotation de l’espace tangente normale.
  * **Format normal** : *DirectX, OpenGL*\
    Basculer entre différents Formats de map normaux (inverse la couche verte). Actif uniquement lorsque l’option Est mappage normal a la valeur True.
  * **Réglage TSL** : *-1.0 - 1.0* Ajuster TSL globalement.
  * **HSL aléatoire** : *-1.0 - 1.0* Définir la randomisation HSL par cellule.
  * **Réglage de l&#39;Alpha** : *-1.0 - 1.0* Définissez le réglage global de l&#39;Alpha, afin de réduire le contraste de l&#39;Alpha.
  * **Alpha aléatoire** : *-1.0 - 1.0* Définissez le paramétrage aléatoire du réglage de l&#39;Alpha par cellule.
  * **Couleur d&#39;arrière-plan** : *(Valeur de couleur)*Définit la couleur d&#39;arrière-plan sur laquelle les textures sont fusionnées.

.

## Exemples d’images

![](../../../../../../assets/floodfill-mapper-ex01.png)

![](../../../../../../assets/floodfill-mapper-ex02.jpg)

</td>
</tr>
</table>
