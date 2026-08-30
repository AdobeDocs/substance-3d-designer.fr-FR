---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: Utilisez le nœud Height aux unités universelles normales pour convertir les maps height en maps normal en utilisant la mise à l'échelle des unités universelles pour obtenir des détails précis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height aux unités universelles normales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# Height aux unités universelles normales

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/normal-hq.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud avancé de conversion Height à normal qui utilise des unités réelles pendant la conversion.

Utile lorsque vous connaissez les dimensions de votre carte de hauteur source et souhaitez effectuer la conversion la plus précise possible, par exemple lorsque vous travaillez avec du matériau numérisé.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Taille de la surface (cm)</b> <i>0.0 - 1000.0</i> | Dimensions de la carte de hauteur d’entrée. |
| <b>Profondeur Height (cm)</b> <i>0.0 - 100.0</i> | Profondeur maximale des détails de la carte de hauteur. |
| <b>Format normal</b> <i>OpenGL, DirectX</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Échantillonnage</b> <i>Standard, Sobel</i> | Bascule entre deux modes d’échantillonnage déterminant la précision. |
