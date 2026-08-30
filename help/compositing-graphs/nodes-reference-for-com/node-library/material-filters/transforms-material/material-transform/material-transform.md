---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation de matière pour appliquer des transformations aux sorties de matière, y compris la rotation, l’échelle et le décalage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation de matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# Transformation de matière

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

La transformation de matériau est simplement la version « multicanaux » des matériaux du [nœud 2D de transformation atomique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Il transforme tous les canaux d’un matériau d’entrée en même temps, avec la même interface que la transformation 2D.

Assurez-vous simplement de configurer correctement les canaux ! Par défaut, les options Métallique/Rugosité et Specular/Lustre sont toutes deux activées, ce qui peut entraîner une certaine confusion.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Transformation</b> <i>(Matrice de transformation)</i> | Fait pivoter et met à l’échelle le résultat. Le déplacement/panoramique s’effectue via le paramètre Décalage |
| <b>Décalage</b> <i>-0.5 - 0.5</i> | Déplace ou traduit le résultat. Lorsque la commande Transformation est présente, le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Format normal</b> | Choisissez entre les formats DirectX et OpenGL (symétrie verte). |
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité. |
