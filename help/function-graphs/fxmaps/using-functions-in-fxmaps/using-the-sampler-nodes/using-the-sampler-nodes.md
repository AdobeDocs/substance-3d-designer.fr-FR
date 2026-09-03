---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: Apprenez à utiliser des nœuds d’échantillonnage dans FXMaps pour échantillonner des textures et créer des variations de matériau procédurales.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des nœuds Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Utilisation des nœuds Sampler

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-01.jpg)

Le nœud d’échantillonnage peut être utilisé pour échantillonner des valeurs de pixels dans une entrée d’image connectée au nœud fx-map. Les valeurs échantillonnées peuvent ensuite être utilisées pour piloter des paramètres quelconques à l&#39;aide de fonctions.

## Exemple simple

Dans cet exemple, une chaîne de nœuds quadrants a été créée pour générer une grille de motif. Une fonction est créée dans le paramètre Opacité/Luminance du dernier quadrant.

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-02.jpg){width="300px"}![](using-the-sampler-nodes.resources/using-the-sampler-nodes-03.jpg){width="300px"}

Le nœud Échantillon prend une entrée float2 comme coordonnées d’échantillonnage (x, y). Dans cet exemple, nous avons utilisé la variable $pos : pour chaque motif, la valeur de pixel est échantillonnée à la position du motif dans la première entrée d’image connectée au nœud FxMap.

Le nœud Sample Gray renvoie une valeur float1 comprise dans la plage 0, 1.

Le nœud Sample Color renvoie une valeur float4 (rgba) comprise dans la plage 0, 1.

## Exemple avancé

Ici, nous comparons la valeur échantillonnée à une constante (0,3). Si la valeur échantillonnée est supérieure à 0,3, la fonction renvoie 1 ; sinon, elle renvoie 0.

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-04.jpg){width="300px"}![](using-the-sampler-nodes.resources/using-the-sampler-nodes-05.jpg){width="300px"}

## Télécharger l’exemple

[Icône de fichier ![SBS](using-the-sampler-nodes.resources/using-the-sampler-nodes-06.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
