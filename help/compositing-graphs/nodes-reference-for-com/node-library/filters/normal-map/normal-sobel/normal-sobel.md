---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: Utilisez le nœud Sobel normal pour générer des cartes de normales à partir de cartes d'height à l'aide de la détection de contour de Sobel pour les détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# Sobel normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-hq.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Convertit une entrée Heighmap en sortie Normalmap. Version légèrement plus avancée du [nœud atomique normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), ce nœud utilise l&#39;échantillonnage Sobel plutôt que la méthode d&#39;échantillonnage standard.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 3.0</i> | Force des normales converties. |
| <b>Format normal</b> <i>OpenGL, DirectX</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
