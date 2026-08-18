---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Utilisez le nœud Scratches Generator pour créer des motifs de rayures procédurales afin d'ajouter de l'usure et des dommages aux matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Générateur Scratches
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Générateur Scratches

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Générateur Scratches (Normal)

**Entrée :** *Générateurs de textures**/Motifs*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Cela place des rayures aléatoires avec beaucoup d’options de personnalisation, vous permettant par exemple de définir la direction, l’étendue et la distorsion.

Il existe une version spéciale de Scratches Generator, Scratches Generator Normal, qui génère des cartes de normales en fonction de la profondeur de ces rayures. La plupart des options sont identiques, mais quelques paramètres supplémentaires sont clairement indiqués pour les paramètres Normal (voir ci-dessous).

## Paramètres

* **Nombre de splines** : *1 - 512* quantité de rayures (splines) à placer.
* **Segments max. par spline** : *2 - 256* quantité de segments/subdivisions sur la longueur d’une rayure. Permet d’obtenir des courbes et des distorsions plus lisses. L’effet est plus perceptible avec des valeurs de Distorsion plus élevées.
* **Rotation de la spline** :*0.0 - 1.0* Rotation uniforme de toutes les splines, pour les orienter dans une direction.
* **Aléatoire de la rotation de la spline** : *0.0 - 1.0* Variation de l&#39;angle, fait pivoter chaque spline de manière aléatoire.
* **Échelle de spline** : *0.0 - 1.0* met à l&#39;échelle de manière uniforme toutes les splines.
* **Échelle aléatoire de la spline** :*0.0 - 1.0* L&#39;échelle aléatoire met à l&#39;échelle chaque spline individuellement.
* **Distorsion de la spline** : *0.0 - 1.0* Niveau de distorsion uniforme sur toutes les splines.
* **Aléatoire de la Distorsion de la spline** : *0,0 - 1,0* aléatoire le niveau de distorsion de chaque spline individuellement.
* **Fréquence de Distorsion de la spline** : *0.0 - 1.0* Définit la fréquence de distorsion, contrôle l&#39;échelle des détails de la distorsion.
* **Largeur de spline** : *0.0 - 2.0* Définit uniformément la largeur de toutes les splines.
* **Aléatoire de la largeur de spline** : *0.0 - 1.0* aléatoire la largeur de spline de chaque spline individuellement.
* **Position aléatoire de la spline** :*0.0 - 1.0* aléatoire la position de chaque spline individuellement. Plus cette valeur est faible, plus les splines seront regroupées au centre de la zone de travail. Peut être utilisé pour créer des taches de rayures.
* **Définir la largeur de la spline en px** : *Faux/Vrai* détermine les unités utilisées pour les paramètres de largeur de spline.
* **Luminance aléatoire (version en niveaux de gris uniquement)** : *0.0 - 1.0* aléatoire la luminance de chaque spline individuellement.
* **Intensité normale (version normale uniquement)** : *0.0 - 1.0* Définit globalement l&#39;intensité de l&#39;effet Normal pour chaque spline.
* **&#x200B; Intensité normale Aléatoire &#x200B;** (version normale uniquement)**&#x200B;** : *0.0 - 1.0*aléatoire individuellement l&#39;intensité normale de chaque spline.
* **&#x200B; Format normal &#x200B;**(version normale uniquement)**&#x200B;** : *DirectX, OpenGL*\
  Bascule entre différents formats de mappage normal (inverse la couche verte).
* **Mode de fondu** : *Aucun, Début, Fin, Début + Fin* Définit si et dans quelle direction les splines fondent.
* **Longueur du fondu** : *0.0 - 1.0* Définit la longueur de l’effet de fondu, si cette option est activée ci-dessus.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
