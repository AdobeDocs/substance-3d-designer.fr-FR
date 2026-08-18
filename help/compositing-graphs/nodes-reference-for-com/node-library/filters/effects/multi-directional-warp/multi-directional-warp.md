---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Utilisez le nœud Déformation multidirectionnelle pour appliquer des effets de déformation dans plusieurs directions afin de créer des motifs de distorsion complexes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Déformation multidirectionnelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---


# Déformation multidirectionnelle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-directional-warp-color.png)![](../../../../../../assets/multi-directional-warp-grayscalepng.png)

## Déformation multidirectionnelle (niveaux de gris)

**Entrée :** *Filtres/Effets*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

La déformation multidirectionnelle applique la [déformation directionnelle](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) plusieurs fois dans des directions opposées, tandis que la texture déplacée reste en place. Elle diffère de la déformation directionnelle standard en ce qu’elle peut pousser dans plusieurs directions, alors que la version atomique n’en autorise qu’une. De cette façon, cela résout le problème classique où la déformation directionnelle semble toujours repousser votre image dans une seule direction, au lieu de travailler dans plusieurs directions ou axes au lieu d’une seule direction.

Il diffère principalement du [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) en ce sens qu&#39;il est légèrement plus restreint : la direction de la déformation est uniquement contrôlée par des paramètres et ne peut pas être définie par une texture d&#39;entrée. L&#39;avantage est qu&#39;il est légèrement plus facile à utiliser et peut être plus précis en fonction de votre cas d&#39;utilisation.

## Paramètres

### Entrées

* **Entrée** :*Entrée Niveaux De Gris/Couleur*\
  Carte de base à laquelle la déformation sera appliquée. Il peut s’agir de couleurs ou de niveaux de gris.
* **Entrée d&#39;intensité** : *Entrée en niveaux de gris*\
  La texture de masque obligatoire qui détermine l’intensité de l’effet de déformation doit être en niveaux de gris.

### Paramètres

* **Intensité** : *0,0 - 20,0*\
  Définit l’intensité de l’effet de déformation et la distance à laquelle les pixels doivent être sortis.
* **Angle de déformation** : *0.0 - 1.0*\
  Définit l’angle ou la direction d’application de l’effet de déformation.
* **Mode** : *Moyenne, Max, Min, Chaîne*\
  Définit le mode de fusion pour les passes consécutives. N&#39;a d&#39;effet que si Directions est 2 ou 4 !
* **Directions** :*1, 2, 4* définit le nombre d’axes de la déformation. 1 signifie qu&#39;il se déplace dans la direction de l&#39;angle, et l&#39;opposé de cette direction, 2 signifie l&#39;axe de l&#39;angle, plus l&#39;axe perpendiculaire, 4 signifie les axes précédents, plus 45 degrés d&#39;inclinaison.

## Exemples d’images

</td>
</tr>
</table>
