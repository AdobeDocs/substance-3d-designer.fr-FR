---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Utilisez le nœud Mélangeur Height normal pour fusionner l'height et les maps normal de combinaison des informations de détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mélangeur Height normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Mélangeur Height normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-normal-blender.resources/height-normal-blender.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud de raccourci qui fusionne une carte de hauteur en niveaux de gris en une carte normale. L’entrée Height est convertie en mappage normal en interne, puis fusionnée correctement avec l’entrée Normal.

Il s&#39;agit d&#39;un moyen plus rapide de fusionner les détails que de le faire manuellement avec des nœuds distincts, mais vous pourriez trouver qu&#39;il manque un peu de contrôle et d&#39;affinement pour certains besoins.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Height</b> <i>Entrée en niveaux de gris</i> | Fusion de la hauteur des niveaux de gris |
| <b>Normal</b> <i>Entrée couleur</i> | Fond normal sur lequel fusionner. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité normale</b> <i>0.0 - 16.0</i> | Intensité de la conversion normale de l&#39;entrée Height. |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
