---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Utilisez le nœud HQ Normal à l'Height pour convertir les maps normal en maps height de haute qualité pour l'extraction des détails de surface.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal à l’Height du QG
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# Normal à l’Height du QG

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud de conversion inverse qui tente de reconvertir un espace de tangente Normalmap en Heightmap. Il s&#39;agit du nœud le plus avancé ; l&#39;option [Normal à l&#39;Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) offre moins d&#39;options et utilise des calculs différents.

Utile lorsque vous n&#39;avez qu&#39;une source Normalmap, mais que vous souhaitez néanmoins effectuer des opérations la combinant avec une carte de hauteur. Gardez à l’esprit que cela ne permettra jamais d’obtenir un résultat correct à 100 %, car les informations sont perdues par nature lors de la conversion de l’Height en normalité. Il ne peut jamais remplacer une carte de hauteur correctement générée !

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Balance des Reliefs</b> <i>0.0 - 1.0</i> | Fusions entre polarisation basse et polarisation haute fréquence. |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> | L’intensité ou le multiplicateur de la carte de hauteur fonctionne un peu comme l’opacité globale. |
| <b>Normaliser l&#39;Height</b> <i>Faux/Vrai</i> | Met automatiquement à l&#39;échelle la plage de la carte de hauteur pour utiliser le contraste complet, comme un [niveau automatique](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md). |
| <b>Qualité</b> <i>Normal, Élevé</i> | Bascule entre vitesse et qualité. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal2height-hq-ex.png" />
        </td>
    </tr>
</table>
