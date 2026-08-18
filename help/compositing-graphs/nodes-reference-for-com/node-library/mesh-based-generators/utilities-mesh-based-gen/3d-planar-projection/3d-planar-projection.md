---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Utilisez le nœud Projection planaire 3D pour projeter des textures sur des surfaces maillées à l’aide de la projection planaire pour le placage de textures.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Projection planaire 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Projection planaire 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## Projection planaire 3D (couleur)

**Entrée :** *Générateurs Basés Sur Le Maillage**/Utilitaires*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Effectue une projection plane en fonction des données de maillage corrigées (cartes de position et de normales mondiales). Permet de projeter et de placer des décalcomanies entre les coutures, indépendamment de la cartographie UV d’origine.

## Paramètres

### Entrées

* **Carte De Position** : *Entrée De Couleur* Carte De Position Cuite
* **Espace Mondial Normal** : *Entrée De Couleur* Carte De L&#39;Espace Mondial Normalisé Cuite
* **Texture projetée** : *entrée de couleur* texture d&#39;entrée à projeter sur la cible.

### Paramètres

* **Positionnement**
  * **Entrée du projet** : *Position UV, Position dans l&#39;espace universel* Choisissez si la position de projection est définie en 2D/UV ou en 3D/espace universel.
  * **Position UV cible** :\
    Uniquement avec l’entrée de position UV, à utiliser de préférence pour sélectionner un point dans la vue 2D sur la carte de position.
  * **Position cible** : *(valeur chromatique)*L&#39;entrée Position dans l&#39;espace universel vous permet de définir une coordonnée 3D exacte.
  * **Cible normale** : *(valeur chromatique)*
  * **Rotation** : *0,0 - 1,0\
    Fait pivoter la texture projetée le long de son axe normal.*
  * **Échelle** : *0.0 - 1.0*\
    Définissez l’échelle globale de la texture projetée.
  * **Taille** :*0.0 - 2.0* Effectuez une mise à l’échelle non uniforme sur la texture projetée.
* **Masquage**
  * **Profondeur maximale** :*0.0 - 1.0* Contrôle la profondeur d&#39;affichage de la texture projetée, le moment où elle sera coupée.
  * **Fondu de Profondeur** :*0.0 - 1.0* Définissez la transition pour que la profondeur de coupure soit soudaine ou fondue.
  * **Seuil normal** : *-1.0 - 1.0* Définissez le seuil pour les surfaces qui ne sont pas exactement alignées avec la normale de projection.
  * **Fondu normal** : *0.0 - 1.0* Définissez la transition pour les surfaces non alignées sur soudain ou fondu.

## Exemples d’images

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>
