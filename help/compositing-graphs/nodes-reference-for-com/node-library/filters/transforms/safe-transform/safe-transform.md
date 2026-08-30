---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Utilisez le nœud Transformation sécurisée pour appliquer des transformations tout en préservant les limites de la texture et en évitant les artefacts.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformation sécurisée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# Transformation sécurisée

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform.png)

![](safe-transform.resources/safe-transform-grayscale.png)

<b>Entrées :</b> Filtres > Transformes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Version sans mosaïque de [Transformation 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Permet de mettre à l’échelle, de faire pivoter et de décaler sans casser la mosaïque et sans perdre les détails des pixels (perte de netteté) en raison de petits décalages et rotations.

Utile pour transformer le bruit lorsque un contrôle maximal ou une netteté parfaite sont requis.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mosaïque</b> <i>1 - 16</i> | Diminue l’échelle de l’entrée par répétition. |
| <b>Mode Décalage</b> <i>Manuel, Aléatoire</i> | Bascule vers un décalage aléatoire au lieu d’un décalage défini manuellement. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Déplace ou traduit le résultat. S’assure que les pixels sont accrochés et non interpolés. |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Fait pivoter l’entrée selon un angle. |
| <b>Rotation de mosaïque sécurisée</b> <i>Faux/Vrai</i> | Détermine le comportement de la Rotation, s’il doit contraindre sur des valeurs sûres qui ne floutent aucun pixel. |
| <b>Symétrie</b> <i>aucun, X, Y, X+Y</i> |  |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur) (version de couleur uniquement)</i> |  |
| <b>Mode Mipmap</b> <i>Automatique, Manuel</i> | Détermine le mode mipmapping. Le réglage manuel permet d’obtenir des résultats plus nets. |
| <b>Niveau du mipmap</b> <i>0 - 10</i> | Lorsque le mode Mipmap est défini sur Manuel, vous pouvez choisir un autre Mipmap. |
