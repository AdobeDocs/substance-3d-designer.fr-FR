---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: Utilisez le nœud de fusion HDR pour fusionner plusieurs images HDR en un seul panorama afin de créer des maps d'environnement composites.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion en HDR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# Fusion en HDR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hdr-merge.resources/hdr-merge.png){width="200px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fusionnez plusieurs expositions photographiques pour créer une image de Plage dynamique élevée. La première entrée est l’image la moins exposée.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée 1-16</b> <i>Entrée couleur</i> | Images d&#39;entrée. La quantité disponible dépend du paramètre. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Entrées</b> <i>2 - 16</i> | Définit la quantité d&#39;entrées disponibles. |
| <b>Delta d&#39;exposition (EV)</b> <i>0.0 - 4.0</i> | Définit la différence d’exposition pour interpréter les différentes images. |
| <b>Point blanc</b> <i>0.0 - 13.0</i> | Définissez le point blanc pour effectuer un réglage sur le résultat final. |
