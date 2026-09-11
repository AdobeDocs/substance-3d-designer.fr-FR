---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: Découvrez les fonctions de Substance 3D Designer et comment les utiliser pour créer des réseaux de nœuds réutilisables.
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Qu’est-ce qu’une fonction ? '
user-guide-description: ''
user-guide-title: ''
source-git-commit: baf36ab85717512cc9e52d67d00293eabb5ebcf6
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Qu’est-ce qu’une fonction ?

Les fonctions de Substance 3D Designer permettent à l’utilisateur de générer des résultats en utilisant la logique que vous retrouverez dans un langage de programmation.

Mais plutôt que d’utiliser des lignes de codes, les fonctions de Designer conservent la même approche nodale. À première vue, un graphe de fonction ressemble beaucoup à un graphe normal.

![](what-is-a-function.resources/image2015-12-17-18-19-37.png)

Vous pouvez rencontrer des fonctions dans 2 cas principaux :

* pour contrôler le résultat d&#39;un paramètre
* si vous modifiez un processeur de pixels

## Contrôle du résultat d’un paramètre

Dans Substance 3D Designer, n’importe quel paramètre peut être contrôlé par une fonction.

![](what-is-a-function.resources/image2015-12-17-21-3-46.png)

Par conséquent, vous pouvez imaginer des règles et des dépendances entre les parties de votre graphe, pour obtenir des résultats uniques.

Par exemple, vous pouvez décider que l’opacité d’un nœud de fusion correspondra à la moitié de l’intensité d’un nœud de déformation :

![](what-is-a-function.resources/warpblend.gif)

En fait, vous avez peut-être déjà créé des fonctions sans en être conscient :

si vous avez exposé un paramètre, vous avez automatiquement créé une fonction et une variable : la fonction contient un nœud get float qui capture la valeur de la nouvelle variable créée :

![](what-is-a-function.resources/expose.gif)
