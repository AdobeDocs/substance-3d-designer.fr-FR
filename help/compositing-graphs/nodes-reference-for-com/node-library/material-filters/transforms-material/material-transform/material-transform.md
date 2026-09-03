---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud de Transforme Matériau pour appliquer des transformations aux sorties du matériau, notamment la rotation, l’échelle et le décalage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation de matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# Transformation de matière

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transform-01.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

La Transforme de matériau est simplement la version de Matériaux « multicanaux » du [nœud Transformation 2D atomique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Il transforme tous les canaux d&#39;un matériau d&#39;entrée en même temps, avec la même interface que le Transforme 2D.

Assurez-vous simplement de configurer correctement les canaux ! Par défaut, les options Métallique/Rugosité et Specular/Brillance sont activées, ce qui peut entraîner une certaine confusion.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Transformation</b> <i>(Matrice de transformation)</i> | Fait pivoter et met à l’échelle le résultat. Le déplacement/panoramique s’effectue via le paramètre Décalage |
| <b>Décalage</b> <i>-0.5 - 0.5</i> | Déplace ou translate le résultat. Lorsque la commande Transformation est présente, le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Format normal</b> | Choisissez entre les formats DirectX et OpenGL (symétrie verte). |
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité. |
