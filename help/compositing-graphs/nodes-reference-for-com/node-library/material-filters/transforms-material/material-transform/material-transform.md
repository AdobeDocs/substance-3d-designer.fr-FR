---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# Transformation de matière

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## Transformation de matière

**Entrée :** *Filtres/Transformations de matériau*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

La transformation de matériau est simplement la version « multicanaux » des matériaux du [nœud 2D de transformation atomique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Il transforme tous les canaux d’un matériau d’entrée en même temps, avec la même interface que la transformation 2D.

Assurez-vous simplement de configurer correctement les canaux ! Par défaut, les options Métallique/Rugosité et Specular/Lustre sont toutes deux activées, ce qui peut entraîner une certaine confusion.

## Paramètres

* **Transformation** : *(Matrice De Transformation)*\
  Fait pivoter et met à l’échelle le résultat. Le déplacement/panoramique s’effectue via le paramètre Décalage
* **Décalage** : *-0.5 - 0.5*\
  Déplace ou traduit le résultat. Lorsque la commande Transformation est présente, le résultat peut être modifié en interagissant directement avec la zone de travail.
* **Format normal**\
  Choisissez entre les formats DirectX et OpenGL (symétrie verte).
* **Canaux**\
  Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
