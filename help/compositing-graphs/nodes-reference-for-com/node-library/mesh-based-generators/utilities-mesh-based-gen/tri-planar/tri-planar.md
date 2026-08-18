---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Utilisez le nœud Plan triangulaire pour projeter les textures de trois plans orthogonaux afin d'obtenir un mappage de texture fluide sur une géométrie complexe.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triplan
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Triplan

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## Tri planaire (niveaux de gris)

**Entrée :** *Générateurs Basés Sur Le Maillage**/Utilitaires*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud avancé effectue un mappage de projection triplanaire en 2D, en fonction des données de position et de normale de l&#39;espace universel. Cela signifie qu’il convertit essentiellement toutes les coordonnées UV en une cartographie (principalement) sans couture basée sur le maillage lui-même.

C&#39;est une bonne façon d&#39;éviter les coutures sans avoir à refaire à chaque fois (il est possible d&#39;obtenir quelque chose de similaire avec le boulanger). L&#39;inconvénient est que ce nœud est assez lourd et donc pas rapide.

Gardez à l&#39;esprit que vos pâtisseries doivent être de haute précision : les pâtisseries 8 bits ne donneront pas de très bons résultats.

## Paramètres

### Entrées

* **Position** : *Entrée Couleur*\
  Mappage de position ancrée. Idéalement, précision de 16 bits ou supérieure.
* **Espace universel normal** : *entrée de couleur*\
  Carte des normales de l&#39;espace mondial au four, idéalement précision de 16 bits ou plus.
* **Entrée X** : *Entrée couleur (Entrée niveaux de gris)*Carte d&#39;entrée pour remapper l&#39;espace UV vers l&#39;espace mondial via une projection triplanaire. Utilisé pour tous les axes lorsque la valeur Entrée image est définie sur 1, pour l’axe X si elle est définie sur 3.
* **Entrée Y** : *Entrée couleur (entrée niveaux de gris)*uniquement si la valeur Entrée image est définie sur 3. Mappage d’entrée pour remapper l’espace universel sur l’axe Y.
* **Entrée Z** : *Entrée couleur (entrée niveaux de gris)*uniquement si la valeur Entrée image est définie sur 3. Carte d&#39;entrée pour remapper l&#39;espace universel sur l&#39;axe Z.

### Paramètres

* **Projection** :*Tous les axes, X uniquement, Y uniquement, Z uniquement* définit les axes avec lesquels fusionner.
* **Entrées d’image** : *1 entrée, 3 entrées*\
  Indiquez si vous souhaitez utiliser une carte pour tous les axes ou une carte spécifique par axe.
* **Mode de fusion** : *linéaire, avancé* augmente la précision.
* **Contraste de fusion** :*0.001 - 1.0* Contraste de transition, mélange entre des transitions lisses ou dures.
* **Facteur De Normalisation** : *0,0 - 1,0*\
  Améliore la fusion par projection en rétablissant la perte de contraste dans la zone de fusion.
* **Mosaïque de texture** : *0.0 - 10.0* nombre de fois où les textures d&#39;entrée sont mosaïquées.
* **Rotation globale** : *0.0 - 1.0*\
  Rotation globale pour tous les axes.
* **Corriger la projection mise en miroir** : *Faux/Vrai* Définissez la façon de gérer les projections mises en miroir.
* **Rotation X** : *0,0 - 1,0* Rotation individuelle sur l&#39;axe X de projection.
* **Rotation Y** : *0,0 - 1,0* Rotation individuelle sur l&#39;axe Y de projection.
* **Rotation Z** : *0,0 - 1,0* Rotation individuelle sur l&#39;axe Z de projection.
* **Décalage X** : *0,0 - 1,0* Décalage sur l&#39;axe X de projection.
* **Décalage Aléatoire X** : *0,0 - 1,0*\
  Permet de rendre aléatoire le décalage de l’axe X.
* **Décalage Y** : *0,0 - 1,0* Décalage sur l&#39;axe Y de projection.
* **Décalage aléatoire Y** : *0.0 - 1.0*\
  Permet de rendre aléatoire le décalage de l’axe Y.
* **Décalage Z** : *0,0 - 1,0* Décalage sur l&#39;axe Z de projection.
* **Décalage aléatoire Z** : *0,0 - 1,0*\
  Permet de rendre aléatoire le décalage de l’axe Z.

## Exemples d’images

</td>
</tr>
</table>
