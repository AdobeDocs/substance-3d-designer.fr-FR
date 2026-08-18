---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

## Rép. non uniforme. Déformation (niveaux de gris)

**Entrée :** *Filtres/Effets*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Déformation dans une direction non uniforme est une version avancée de [Déformation directionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) qui permet de piloter l&#39;intensité et la direction de la déformation par une entrée d&#39;image. Il offre beaucoup plus de contrôle et peut créer une distorsion d&#39;image très utile et intéressante, dans le même esprit que le [flou de Pente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Elle diffère de la [déformation multidirectionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) en ce qu&#39;elle permet de contrôler l&#39;angle via une entrée de courbe de transfert personnalisée, tandis que la déformation multidirectionnelle permet uniquement de contrôler la direction via des paramètres. Cela signifie que vous pouvez créer des effets avancés de traînée et de courbure qui ne seraient pas possibles autrement.

## Paramètres

### Entrées

* **Entrée** :*Entrée En Niveaux De Gris*\
  Carte de base à laquelle la déformation sera appliquée.
* **Entrée d&#39;intensité** : *Entrée en niveaux de gris*\
  La texture de masque obligatoire qui détermine l’intensité de l’effet de déformation doit être en niveaux de gris.
* **Entrée Angle De Déformation** : *Entrée Niveaux De Gris*\
  La texture de masque obligatoire qui détermine l’angle de l’effet de déformation doit être en niveaux de gris.

### Paramètres

* **Intensité** : *0,0 - 20,0*\
  Définit l’intensité de l’effet de déformation et la distance à laquelle les pixels doivent être sortis.
* **Angle de déformation** : *0.0 - 1.0*\
  Définit l’angle ou la direction d’application de l’effet de déformation.
* **Multiplicateur d&#39;entrée d&#39;angle de déformation** : *0.0 - 1.0*\
  Définit l’effet de la courbe d’entrée d’angle de déformation. La texture d’entrée Angle de déformation sera ensuite utilisée pour effectuer une interpolation de 0 à la valeur de ce paramètre.
* **Mode De Piste** : *Min, Max, Moyenne*\
  Définit la façon dont les traînées sont fusionnées.
* **Longueur de piste** : *0.0 - 1.0*\
  Définit la longueur des pistes.
* **Fondu de piste** : *0.0 - 1.0*\
  Définit la quantité de fondu de chaque piste
* **Courbe de traînée** : *-1.0 - 1.0* N’est effective que si l’option Fondu de traînée n’est pas définie sur 0. Définit le comportement de l’effet de fondu.

## Exemples d’images

</td>
</tr>
</table>
