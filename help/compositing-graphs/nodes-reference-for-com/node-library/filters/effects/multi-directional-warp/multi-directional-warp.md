---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation directionnelle multiple pour appliquer des effets de déformation dans plusieurs directions afin de créer des motifs de distorsion complexes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation directionnelle multiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 3%

---


# Déformation directionnelle multiple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-directional-warp.resources/multi-directional-warp-color.png)![](multi-directional-warp.resources/multi-directional-warp-grayscalepng.png)

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

La Déformation directionnelle multiple applique la [Déformation directionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) plusieurs fois dans des directions opposées, tandis que la texture déplacée reste en place. Il diffère de la Déformation directionnelle classique en ce qu&#39;il peut pousser dans plusieurs directions, alors que la version atomique n&#39;en permet qu&#39;une. De cette façon, cela résout le problème classique où la Déformation directionnelle semble toujours repousser votre image dans une seule direction, au lieu de travailler dans plusieurs directions ou axes au lieu d’une seule direction.

Il diffère principalement du [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) en ce sens qu&#39;il est légèrement plus restreint : la direction de la déformation est uniquement contrôlée par des paramètres et ne peut pas être définie par une map d&#39;entrée. L&#39;avantage est qu&#39;il est légèrement plus facile à utiliser et peut être plus précis en fonction de votre cas d&#39;utilisation.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Entrée Niveaux de gris/Couleur</i> | Carte de base à laquelle la déformation sera appliquée. Il peut s’agir de couleurs ou de niveaux de gris. |
| <b>Entrée d&#39;intensité</b> <i>Entrée en niveaux de gris</i> | La texture de masque obligatoire qui détermine l’intensité de l’effet de déformation doit être en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 20.0</i> | Définit l’intensité de l’effet de déformation et la distance à laquelle les pixels doivent être sortis. |
| <b>Angle de déformation</b> <i>0.0 - 1.0</i> | Définit l’angle ou la direction d’application de l’effet de déformation. |
| <b>Mode</b> <i>Moyenne, Max, Min, Chaîne</i> | Définit le mode de Fusion pour les passes consécutives. N&#39;a d&#39;effet que si Directions est 2 ou 4 ! |
| <b>Directions</b> <i>1, 2, 4</i> | Définit le nombre d’Axes de la déformation. 1 signifie qu&#39;il se déplace dans la direction de l&#39;Angle, et l&#39;opposé de cette direction, 2 signifie l&#39;axe de l&#39;angle, plus l&#39;axe perpendiculaire, 4 signifie les axes précédents, plus les inclinaisons de 45 degrés. |
