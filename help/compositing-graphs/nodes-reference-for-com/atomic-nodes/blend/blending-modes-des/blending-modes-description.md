---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend/blending-modes-description.html"
breadcrumb-title: ''
description: Découvrez les modes de fusion disponibles dans Substance 3D Designer pour combiner des textures avec différents effets de composition.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend > Blending modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modes de fusion
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 2%

---


# Modes de fusion

Le nœud [Fusion](../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) offre les modes de fusion suivants :

## Copier

Le mode de fusion *Copier* place simplement le premier plan sur l&#39;arrière-plan.

![Mode de fusion : Copier](../../../../../assets/image2015-8-20-9-38-0.png "Mode de fusion : Copier"){zoomable="yes"}

Pour les images couleur, la couche alpha est prise en compte par défaut dans l’opacité.

Vous pouvez modifier ce paramètre à l’aide du paramètre Fusion d’Alpha.

![Mode de fusion : Copier (2)](../../../../../assets/image2015-8-20-14-15-29.png "Mode de fusion : Copier (2)"){zoomable="yes"}

## Ajouter (Densité linéaire)

Le mode de fusion *Ajouter* ajoute la valeur d&#39;entrée de premier plan à chaque pixel correspondant en arrière-plan.

![Mode de fusion : Ajouter (Densité linéaire)](../../../../../assets/image2015-8-20-9-38-19.png "Mode de fusion : Ajouter (Densité linéaire)"){zoomable="yes"}

## Soustraction

Le mode de fusion *Soustraction* soustrait la valeur d&#39;entrée de premier plan de chaque pixel correspondant en arrière-plan.

Si le résultat de la soustraction est inférieur à 0, la valeur est plafonnée à 0, ce qui donne un noir pur.

![Mode de fusion : Soustraction](../../../../../assets/image2015-8-20-9-38-35.png "Mode de fusion : Soustraction"){zoomable="yes"}

## Multiplication

Le mode de fusion *Multiplier* multiplie la valeur d&#39;entrée d&#39;arrière-plan par chaque pixel correspondant au premier plan.

Comme la valeur de chaque pixel est comprise entre 0 et 1, le résultat est toujours égal ou inférieur (plus foncé) à l’original.

![Mode de fusion : Produit](../../../../../assets/image2015-8-20-9-38-53.png "Mode de fusion : Produit"){zoomable="yes"}

## Add-sub

Le mode de fusion *Ajouter sub* fonctionne comme suit :

* Les pixels de premier plan dont la valeur est supérieure à 0,5 sont ajoutés à leurs pixels d’arrière-plan respectifs.
* Les pixels de premier plan dont la valeur est inférieure à 0,5 sont soustraits de leurs pixels d’arrière-plan respectifs.

![Mode de fusion : Ajouter sub](../../../../../assets/image2015-8-20-9-39-11.png "Mode de fusion : Ajouter sub"){zoomable="yes"}

## Max. (Éclaircir)

Le mode de fusion *Max* sélectionnera la valeur la plus élevée entre l&#39;arrière-plan et le premier plan.

![Mode de fusion : Max (Éclaircir)](../../../../../assets/image2015-8-20-9-40-12.png "Mode de fusion : Max (Éclaircir)"){zoomable="yes"}

## Min. (obscurcir)

Le mode de fusion *Min* sélectionnera la valeur inférieure entre l&#39;arrière-plan et le premier plan.

![Mode de fusion : Min (Obscurcir)](../../../../../assets/image2015-8-20-9-40-31.png "Mode de fusion : Min (Obscurcir)"){zoomable="yes"}

## Basculer

Le mode de fusion du *commutateur* est similaire au mode de copie, avec une différence *cruciale* :

* &#39;Opacité&#39; définie sur 0 : le flux de nœuds connectés à l&#39;entrée &#39;Foreground&#39; *ne sera pas calculé*.
* « Opacité » définie sur 1 : le flux de nœuds connectés à l&#39;entrée « Arrière-plan » *ne sera pas calculé*.

Par conséquent, ce mode peut être utilisé pour améliorer les performances de votre graphique.

Les nœuds [Switch](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) et [Switch grayscale](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) sont configurés pour utiliser les nœuds de fusion dans ces configurations spécifiques.

![Mode de fusion : Basculer](../../../../../assets/image2015-8-20-9-38-0.png "Mode de fusion : Basculer"){zoomable="yes"}

## Division

Le mode de fusion *Division* divise la valeur des pixels d&#39;entrée de l&#39;arrière-plan par chaque pixel correspondant au premier plan.

![Mode de fusion : Division](../../../../../assets/image2015-8-20-9-41-32.png "Mode de fusion : Division"){zoomable="yes"}

## Superposition

Le mode de fusion *Incrustation* combine les modes de fusion Produit et Superposition :

* 
  * Si la valeur du pixel du calque inférieur est inférieure à 0,5, une fusion de type *Produit* est appliquée
  * Si la valeur du pixel du calque inférieur est supérieure à 0,5, une fusion de type *Écran* est appliquée

![Mode de fusion : Incrustation](../../../../../assets/image2015-8-20-9-41-50.png "Mode de fusion : Incrustation"){zoomable="yes"}

## Écran

Avec le mode de fusion Superposition, les valeurs des pixels dans les deux entrées sont inversées, multipliées, puis de nouveau inversées.

L’effet inverse est à multiplier, et la luminosité est toujours égale ou supérieure (plus vive) à celle de l’original.

![Mode de fusion : Écran](../../../../../assets/image2015-8-20-9-42-11.png "Mode de fusion : Écran"){zoomable="yes"}

## Soft light

Le mode de fusion Lumière tamisée crée un résultat subtil plus clair ou plus sombre selon la luminosité de la couleur de premier plan.

Les couleurs de fusion dont la luminosité est supérieure à 50 % éclaircissent les pixels de l’arrière-plan, tandis que les couleurs dont la luminosité est inférieure à 50 % assombrissent les pixels de l’arrière-plan.

![Mode de fusion : Lumière tamisée](../../../../../assets/image2015-8-20-9-42-32.png "Mode de fusion : Lumière tamisée"){zoomable="yes"}
