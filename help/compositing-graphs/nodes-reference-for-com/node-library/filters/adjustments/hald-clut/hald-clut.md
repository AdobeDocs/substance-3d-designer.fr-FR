---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Utilisez le nœud Hald CLUT pour appliquer des tables de correspondance de couleur à l'aide du format Hald CLUT pour l'étalonnage et la correction des couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

## Hald CLUT

**Entrée :** *Filtres/Réglages*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Applique une table LUT à l’image d’entrée. Le LUT doit être au format Hald en résolution 4096\*4096. Voir <http://www.quelsolaar.com/technology/clut.html> pour plus d&#39;informations.

### Entrées

* **entrée** : *entrée de couleur*\
  Image sur laquelle appliquer le LUT.
* **lut** : emplacement d&#39;entrée *Color Input* Lut. Doit être 4096x4096.

## Paramètres

* **Intensité LUT par Alpha** : *Faux/Vrai* Définit si l’effet LUT est pondéré par la couche alpha.

Exemples

![](../../../../../../assets/content-hald-clut.jpg)

</td>
</tr>
</table>
