---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Utilisez le nœud Recadrage automatique pour recadrer automatiquement les textures afin de supprimer les bordures vides et d’optimiser les dimensions de la texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recadrage automatique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Recadrage automatique

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

**Entrée :** Filtres*/Transformations*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Recadrage automatique** ajuste l&#39;**entrée** de sorte que son contenu soit placé au *centre* de l&#39;image sans être redimensionné, ou *redimensionné à la plage* de l&#39;image.

Le contenu de l&#39;image est défini par une case ajustée aux *premier et dernier pixels* sur **X** et **Y** dont les valeurs sont *supérieures à 0* (c&#39;est-à-dire non noires). La version **Color** vous permet de choisir parmi les couches RGB et Alpha pour définir cette zone.

</td>
</tr>
</table>

## Paramètres

* **Mode** *Nombre entier* Définissez la méthode de recadrage à appliquer :
  * *Recadrer le carré* : l&#39;image est recadrée de sorte que la forme soit au centre de la plus petite image *carrée* qui puisse l&#39;inclure entièrement
  * *Recadrage automatique* : l&#39;image est recadrée de sorte que la forme soit au centre de la plus petite image *carrée ou non carrée* qui puisse l&#39;inclure entièrement
  * *Adapter (Conserver le rapport)* : l&#39;image est redimensionnée à *la plage complète* de l&#39;image tout en conservant ses *proportions* (c&#39;est-à-dire le rapport largeur/longueur)
  * *Remplir (étirer)* : l&#39;image est redimensionnée à la *plage complète* de l&#39;image
* **Utiliser l&#39;alpha** *booléen* Utilisez la couche alpha de l&#39;**entrée** pour déterminer les *limites* du contenu de l&#39;image à recadrer. Lorsque cette option est définie sur *Faux*, les pixels noirs sont utilisés à la place.\
  *Remarque* : ce paramètre est uniquement disponible dans la version **Color** du nœud.
* Le **mode de filtrage** *entier* définit comment traiter les résultats échantillonnés lors de l&#39;*interpolation* entre les pixels :
  * *Nearest* : échantillonnera exactement la *même* valeur (plus rapide)
  * *Bilinéaire* : appliquera un filtre bilinéaire au résultat pour un aspect *plus lisse*
  * *Auto* : utilise le mode le plus approprié des deux modes ci-dessus en fonction du **Mode** sélectionné pour le recadrage

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-demo-01-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant.jpg){width="128px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant4.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant3.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-node.png){width="420px"}

</td>
</tr>
</table>
