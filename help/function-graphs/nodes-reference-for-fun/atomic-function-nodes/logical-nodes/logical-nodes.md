---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: Accédez aux nœuds logiques dans les graphes de fonction Substance 3D Designer pour effectuer des comparaisons et des opérations logiques booléennes.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Logique
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Nœuds logiques

Les nœuds logiques sont utilisés pour ajouter plusieurs conditions à votre graphe :

![](logical-nodes.resources/image2015-12-23-11-23-21.png)

## Nœud *And*

![](logical-nodes.resources/image2015-12-23-11-30-9.png)

Le nœud Et prend deux nœuds de Booléen comme entrée :

* Si les deux entrées sont True, la sortie du nœud *And* sera *True*
* Dans tous les autres cas, le nœud *And* retournera *False*

## Le nœud *Or*

![](logical-nodes.resources/image2015-12-23-11-30-44.png)

Le nœud Or prend deux nœuds de Booléen comme entrée :

* Si au moins une des entrées est True (1), la sortie du nœud *Or* sera *True*
* Si les deux entrées sont False, le nœud *Or* renvoie *False*

## Nœud *Not*

![](logical-nodes.resources/image2015-12-23-11-31-46.png)

Le nœud Not prend un Booléen comme entrée : il va regarder la valeur d&#39;entrée et retourner son contraire :

* L&#39;entrée *Vrai* donne une sortie *Faux*
* L&#39;entrée *False* donne une sortie *True*
