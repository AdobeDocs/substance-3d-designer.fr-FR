---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Utilisez le nœud Normal à Height pour convertir les cartes de normales en cartes d'height afin d'extraire les informations de profondeur de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal à l’Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# Normal à l’Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud de conversion inverse qui tente de reconvertir une carte normale d&#39;espace tangent en carte de hauteur. Il s&#39;agit de la version légèrement plus simple ; [Normal à l&#39;Height HQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) dispose de plus d&#39;options.

Utile lorsque vous n&#39;avez qu&#39;une source Normalmap, mais que vous souhaitez néanmoins effectuer des opérations la combinant avec une carte de hauteur. Gardez à l’esprit que cela ne permettra jamais d’obtenir un résultat correct à 100 %, car les informations sont perdues par nature lors de la conversion de l’Height en normalité. Si vous réglez les paramètres en conséquence, cette version hors siège réussit correctement à convertir les détails simples.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Balance des Reliefs</b> <i>0.0 - 1.0</i> | Ajustez la mesure dans laquelle les différentes fréquences influencent le résultat final. Cela dépend en grande partie du mappage d&#39;entrée et nécessite un peu de réglages. |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Opacité globale</b> <i>0.0 - 1.0</i> | Règle l’opacité globale de l’effet. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/normal2heightex.png" />
        </td>
    </tr>
</table>
