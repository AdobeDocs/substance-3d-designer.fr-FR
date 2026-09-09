---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/channels/alpha-merge.html"
breadcrumb-title: ''
description: Utilisez le nœud de fusion Alpha pour combiner des textures RGB avec des couches alpha afin de créer des textures RVBA.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Channels > Alpha Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alpha de la fusion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# Alpha de la fusion

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](alpha-merge.resources/rgb-a-merge.png)

<b>Entrées :</b> Filtres > Canaux

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ajoute une couche alpha à une entrée sans couche alpha. À ne pas confondre avec la [fusion RVBA](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), ce nœud est beaucoup plus simple et n&#39;ajoute que de l&#39;alpha !

Nœud simple mais pratique lorsque vous souhaitez simplement masquer quelque chose, ou lorsque votre résultat nécessite un alpha.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>RGB</b> <i>Entrée couleur</i> | Image couleur sans alpha |
| <b>A</b> <i>Entrée en niveaux de gris</i> | Image en niveaux de gris à utiliser comme alpha du résultat. |
