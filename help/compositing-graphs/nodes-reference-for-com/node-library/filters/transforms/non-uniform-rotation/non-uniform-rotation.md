---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: Utilisez le nœud Rotation non uniforme pour appliquer des transformations de rotation non uniformes afin de créer des effets de spirale et de vortex.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotation non uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Rotation non uniforme

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**Entrée :** Filtres*/Transformations*

**Intermédiaire**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Rotation non uniforme** fait pivoter l&#39;**entrée** à l&#39;aide de l&#39;entrée **Map rotation**.

Les valeurs de l&#39;image représentent un *nombre de tours*. La rotation s&#39;effectue autour de la position spécifiée par la valeur **Position de pivot** ou l&#39;entrée **Position de pivot map**.\
Les valeurs positives de l&#39;entrée **Map rotation** entraînent une rotation *horaire*.

</td>
</tr>
</table>

## Paramètres

### Entrées

* **Entrée** *Niveaux De Gris/Couleur*\
  Image en niveaux de gris en entrée qui doit pivoter.
* **Map rotation** *Niveaux de gris* La carte utilisée pour contrôler le degré de rotation, en *nombre de tours*. Les valeurs échantillonnées sont multipliées par rapport au **multiplicateur d&#39;angle de rotation**. Les valeurs négatives entraînent une rotation *antihoraire*.
* **Cartographie De Position de pivot De Rotation** *Couleur*\
  Image utilisée pour spécifier la position de la rotation *pivot*. La position **X/Y** est mappée aux couches **R/G** de l&#39;image.

### Paramètres

* **Multiplicateur D&#39;Angle De Rotation** *Flottant*\
  Règle l&#39;intensité de l&#39;entrée de **Map rotation**.
* **Décalage De L&#39;Angle De Rotation** *Flottant*\
  Applique la rotation supplémentaire spécifiée.
* **Utiliser le mappage de Position de pivot** *booléen*\
  Utilisez une *entrée bitmap* pour spécifier la position du pivot de rotation. La position **X/Y** est mappée aux canaux **R/G** de l&#39;entrée **Mappage de position**.
* **Position de pivot** *Float2*\
  Position du pivot autour duquel l&#39;image est pivotée.
* **Couleur D&#39;Arrière-Plan** *Float/Float4*\
  Couleur d&#39;arrière-plan pour afficher *à l&#39;extérieur* des limites de l&#39;image au cas où la mosaïque n&#39;est pas définie sur **Mosaïque de type H et V**.
* **Mode De Filtrage** *Nombre Entier*\
  Définit le traitement des résultats échantillonnés lors de l&#39;*interpolation* entre les pixels :
  * *Nearest* : échantillonnera exactement la *même* valeur (plus rapide)
  * *Bilinéaire* : appliquera un filtre bilinéaire au résultat pour un aspect *plus lisse*

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>
