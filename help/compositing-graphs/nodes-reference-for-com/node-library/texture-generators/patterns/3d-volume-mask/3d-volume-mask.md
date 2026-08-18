---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: Utilisez le nœud Masque de volume 3D pour créer des masques volumiques basés sur la position 3D pour des effets de matériau avancés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Masque de volume 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# Masque de volume 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask.png){width="256px"}

**Entrée :** Générateur*/Motif*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Masque de volume 3D** génère une représentation d&#39;une *forme primitive* basée sur le mappage d&#39;entrée **Position**.

</td>
</tr>
</table>

## Paramètres

### Entrées

* **Position** *Couleur*\
  La carte décrivant les *coordonnées de l&#39;espace 3D* dans laquelle la primitive est représentée.\
  Les coordonnées **X/Y/Z** sont mappées aux canaux **R/G/B** respectivement.

### Paramètres

* **Forme** *Nombre entier*\
  La forme primitive qui doit être représentée:
  * *Cube*- *Cylindre*- *Sphère*
* **Échelle** *Flottant*\
  Définit l&#39;échelle *globale* de la primitive, appliquée *uniformément* sur tous les axes.
* **Taille** *Float3*\
  Définit la taille de la forme sur chaque axe.
* **Entrée de position** *Nombre entier*\
  Méthode de *représentation de l&#39;espace* via l&#39;entrée **Position** :
  * *Position UV* : utilisez une *carte UV*. Les coordonnées X/Y (U/V) sont respectivement mappées aux canaux R/G. L&#39;axe Z est supposé être le vecteur *avant orthogonal*.
  * *Position dans l&#39;espace universel* : utilisez une *carte de position* pour mapper la primitive dans l&#39;espace 3D. Les coordonnées X/Y/Z sont respectivement mappées sur les canaux R/G/B.
* **Positionner les UV** *Flotter2*\
  Position de la primitive dans l’espace UV.\
  *Remarque* : ce paramètre est uniquement disponible lorsque le paramètre **Entrée de position** est défini sur *Position UV*.
* **Position** *Float3*\
  La position du primitif dans l&#39;espace.\
  *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Entrée de position** est défini sur *Position dans l&#39;espace universel*.
* **Rotation** *Float3*\
  Définit la rotation de la forme dans l’espace univers.
* **Largeur du contour progressif** *Flottant*\
  Ajuste la largeur du *dégradé de fondu* de la surface de la primitive vers l&#39;intérieur.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant4.jpg){width="256px"}

</td>
</tr>
</table>
