---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Utilisez le nœud Extend Shape pour étendre les formes au-delà de leurs limites afin de créer des effets de masque et de motif étendus.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

**Entrée :** Filtres*/Effets*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Extend Shape** étend une *section* de l&#39;**entrée** sur une direction et une distance définies.

Le paramètre **Afficher l&#39;assistant** vous permet de visualiser la section étendue et la direction de l&#39;extension.

</td>
</tr>
</table>

## Paramètres

* **Mode** *Entier* Définit les *paramètres* utilisés pour appliquer l&#39;extension :
  * *Bidirectionnelle* : la section de l&#39;**entrée** spécifiée par **position d&#39;extension** et **angle d&#39;extension** est étendue sur la **distance d&#39;extension** dans *des directions opposées*
  * *Unidirectionnelle* : la section de l&#39;**entrée** spécifiée par **position d&#39;extension** et **angle d&#39;extension** est étendue sur la **distance d&#39;extension** dans une *direction unique*
  * *Positions de début/fin* : une extension *vectorielle* est définie par **Position de début** et **Position de fin**. La section *perpendiculaire* de l&#39;**entrée** à la **position de départ** est étendue *sur ce vecteur* jusqu&#39;à la **position de fin**
* **Distance d&#39;extension** *Flotter* La distance sur laquelle la section spécifiée par **Position d&#39;extension** et **Angle d&#39;extension** doit être étendue. La distance est exprimée en *proportion* de l&#39;étendue d&#39;image.
* **Position d&#39;extension** *Flotter* La position dans l&#39;image de la section qui doit être étendue. La valeur est exprimée en un *décalage par rapport au centre*.
* **Angle d&#39;extension** *Flottant* L&#39;angle de la section qui doit être étendue, compte tenu du point de départ, est une *section verticale*.
* **Position de départ** *Float2* Position de départ du *vecteur d&#39;extension*.
* **Position de fin** *Float2* La position de fin du *vecteur d&#39;extension*.
* **Décalage de luminance de début** *Flottant* Applique un décalage de luminance à la zone de l&#39;image *précédant* la section étendue. Ce décalage de luminance est *interpolé le long de la section* à la luminance de la zone de l&#39;image suivant la section.\
  *Remarque* : ce paramètre est uniquement disponible dans la version **en niveaux de gris** du nœud.
* **Décalage de luminance de fin** *Flottant* Applique un décalage de luminance à la zone de l&#39;image *suivant* la section étendue. Ce décalage de luminance est *interpolé le long de la section* à la luminance de la zone de l&#39;image précédant la section.\
  *Remarque* : ce paramètre est uniquement disponible dans la version **en niveaux de gris** du nœud.
* **Lum. Le décalage ignore les pixels noirs** *booléens* Lorsque cette option est définie sur *True*, les décalages de luminance spécifiés dans *Décalage de luminance de début *** et** Décalage de luminance de fin **ne sont appliqués qu&#39;à des pixels *non noirs*, c&#39;est-à-dire des pixels dont la valeur est supérieure à 0.**\
  *Remarque* : ce paramètre est uniquement disponible dans la version **en niveaux de gris** du nœud.
* Le **mode de filtrage** *entier* définit comment traiter les résultats échantillonnés lors de l&#39;*interpolation* entre les pixels :
  * *Nearest* : échantillonnera exactement la *même* valeur (plus rapide)
  * *Bilinéaire* : appliquera un filtre bilinéaire au résultat pour un aspect *plus lisse*
* **Afficher l&#39;assistant** *booléen* Visualisez la *section étendue* sous la forme d&#39;une incrustation avec des flèches indiquant la *direction* de l&#39;extension.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>
