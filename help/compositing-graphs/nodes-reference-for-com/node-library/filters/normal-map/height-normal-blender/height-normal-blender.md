---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Utilisez le nœud Mélangeur Height normal pour fusionner les cartes d'height et de normales afin de combiner les informations de détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mélangeur Height normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Mélangeur Height normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Mélangeur Height normal

**Entrée :** *Filtres/Mappage de normales*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud de raccourci qui fusionne une image en niveaux de gris en hauteur sur une image normale. L’entrée Height est convertie en mappage normal en interne, puis fusionnée correctement avec l’entrée Normal.

Il s&#39;agit d&#39;un moyen plus rapide de fusionner les détails que de le faire manuellement avec des nœuds distincts, mais vous pourriez trouver qu&#39;il manque un peu de contrôle et d&#39;affinement pour certains besoins.

## Paramètres

### Entrées

* **Height** : *Entrée en niveaux de gris*\
  Fusion de la hauteur des niveaux de gris
* **Normal** : *Entrée Couleur*\
  Fond normal sur lequel fusionner.

### Paramètres

* **Intensité normale** : *0.0 - 16.0* Intensité de la conversion normale de l&#39;entrée d&#39;Height.
* **Format normal** : *DirectX, OpenGL*\
  Bascule entre différents formats de mappage normal (inverse la couche verte).

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
