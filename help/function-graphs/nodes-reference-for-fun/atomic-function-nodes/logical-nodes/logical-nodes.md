---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: Accédez aux nœuds logiques des graphiques de fonction Substance 3D Designer pour effectuer des opérations et des comparaisons logiques booléennes.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Logique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Nœuds logiques

Les nœuds logiques sont utilisés pour ajouter plusieurs conditions à votre graphique :

![](logical-nodes.resources/logical-nodes-01.png)

## Nœud *And*

![](logical-nodes.resources/logical-nodes-02.png)

Le nœud And prend deux nœuds booléens comme entrée :

* Si les deux entrées sont True, la sortie du nœud *And* sera *True*
* Dans tous les autres cas, le nœud *And* retournera *False*

## Le nœud *Or*

![](logical-nodes.resources/logical-nodes-03.png)

Le nœud Or prend deux nœuds booléens comme entrée :

* Si au moins une des entrées est True (1), la sortie du nœud *Or* sera *True*
* Si les deux entrées sont False, le nœud *Or* renvoie *False*

## Nœud *Not*

![](logical-nodes.resources/logical-nodes-04.png)

Le nœud Not prend un booléen comme entrée : il va regarder la valeur d&#39;entrée et retourner son contraire :

* L&#39;entrée *Vrai* donne une sortie *Faux*
* L&#39;entrée *False* donne une sortie *True*
