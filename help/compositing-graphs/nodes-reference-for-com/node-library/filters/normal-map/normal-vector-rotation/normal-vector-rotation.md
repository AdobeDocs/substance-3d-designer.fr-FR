---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: Utilisez le nœud Rotation des vecteurs normaux pour faire pivoter les vecteurs de map normal afin de régler l’éclairage de la surface et l’orientation des détails.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotation vectorielle normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# Rotation vectorielle normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation-01.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud utilitaire normal qui fait pivoter tous les vecteurs d&#39;un mappage normal d&#39;entrée dans l&#39;espace de Tangente. Ne transforme pas réellement les pixels, mais modifie les valeurs qu’ils représentent. Il peut utiliser un mappage facultatif pour ajouter des rotations aléatoires à des facettes en niveaux de gris.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Normal</b> <i>Entrée couleur</i> | Mappage de base sur lequel effectuer la rotation. Obligatoire. |
| <b>Map rotation (facultatif)</b> <i>Entrée en niveaux de gris</i> | Carte en niveaux de gris qui module la force de rotation. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Angle De Rotation</b> <i>0.0 - 1.0</i> | Définit l&#39;angle de rotation de la texture normale |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Basculer entre différents Formats de map normaux (inverse la couche verte) |
