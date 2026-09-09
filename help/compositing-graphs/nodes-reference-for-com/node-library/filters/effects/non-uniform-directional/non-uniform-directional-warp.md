---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Non Uniform Directional Warp pour appliquer une déformation directionnelle non uniforme afin de créer divers effets de distorsion.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 5%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-directional-warp.resources/non-uniform-directional-warp-color.png)![](non-uniform-directional-warp.resources/non-uniform-directional-warp-grayscale.png)

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Déformation dans une direction non uniforme est une version avancée de [Déformation directionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) qui permet de piloter l&#39;intensité et la direction de la déformation par une entrée d&#39;image. Il offre beaucoup plus de contrôle et peut créer une distorsion d&#39;image très utile et intéressante, dans le même esprit que le [flou de Pente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Elle diffère de la [déformation multidirectionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) en ce qu&#39;elle permet de contrôler l&#39;angle via une entrée de courbe de transfert personnalisée, tandis que la déformation multidirectionnelle permet uniquement de contrôler la direction via des paramètres. Cela signifie que vous pouvez créer des effets avancés de traînée et de courbure qui ne seraient pas possibles autrement.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Entrée en niveaux de gris</i> | Carte de base à laquelle la déformation sera appliquée. |
| <b>Entrée d&#39;intensité</b> <i>Entrée en niveaux de gris</i> | La texture de masque obligatoire qui détermine l’intensité de l’effet de déformation doit être en niveaux de gris. |
| <b>Entrée d’angle de déformation</b> <i>Entrée en niveaux de gris</i> | La texture de masque obligatoire qui détermine l’angle de l’effet de déformation doit être en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité</b> <i>0.0 - 20.0</i> | Définit l’intensité de l’effet de déformation et la distance à laquelle les pixels doivent être sortis. |
| <b>Angle de déformation</b> <i>0.0 - 1.0</i> | Définit l’angle ou la direction d’application de l’effet de déformation. |
| <b>Multiplicateur d&#39;entrée d&#39;angle de déformation</b> <i>0.0 - 1.0</i> | Définit l’effet de la courbe d’entrée d’angle de déformation. La texture d’entrée Angle de déformation sera ensuite utilisée pour effectuer une interpolation de 0 à la valeur de ce paramètre. |
| <b>Mode de piste</b> <i>Min, Max, Moyenne</i> | Définit la façon dont les traînées sont fusionnées. |
| <b>Longueur de piste</b> <i>0.0 - 1.0</i> | Définit la longueur des pistes. |
| <b>Atténuation de piste</b> <i>0.0 - 1.0</i> | Définit l’atténuation de chaque piste |
| <b>Courbe De Traînée</b> <i>-1.0 - 1.0</i> | Cette option n’a d’effet que si l’Atténuation de piste est différente de 0. Définit le comportement de l’effet de fondu. |
