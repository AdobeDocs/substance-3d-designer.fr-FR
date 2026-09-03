---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transforme normal pour appliquer des transformations aux maps normal tout en conservant correctement les directions des vecteurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transforme normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Transforme normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform-01.png){width="128px"}

<b>Entrée :</b> Filtres > Map normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Comme le nœud 2D de Transforme atomique, cela permet la transformation des cartes normales sans rupture de l&#39;espace de Tangente. Au lieu de cela, il est recalculé à la volée, ce qui permet de toujours corriger les cartes normales.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Matrix2x2</b> <i>(Matrice de transformation) :</i> | Faites pivoter ou mettez à l’échelle l’entrée. |
| <b>Décalage</b> <i>-0.5 - 0.5</i> | Déplace ou traduit le résultat. Lorsque la commande Transformation est présente, le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Basculer entre différents Formats de map normaux (inverse la couche verte) |
