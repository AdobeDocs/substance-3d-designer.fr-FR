---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: Apprenez à utiliser des variables dans les graphiques fonctionnels Substance 3D Designer pour stocker et réutiliser efficacement des valeurs.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Variables

>[!NOTE]
>
> Pour plus d&#39;informations sur la création et l&#39;utilisation des nœuds de variables, consultez la *[section Nœuds de variables](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*.

## Définition

Si vous avez peu de connaissances en programmation, vous connaissez peut-être le concept de variable.

Sinon, voici une définition simple :

>[!NOTE]
>
> Une variable est simplement un « conteneur » avec un nom spécifique qui contient une valeur.
> 
> Vous pouvez utiliser la valeur contenue dans une variable en l’appelant avec son nom.

## Types de variables

Dans Substance 3D Designer, vous disposez de deux familles de variables : numériques et booléennes.

## Variables numériques

Les variables numériques sont essentiellement des nombres. Mais nous faisons une distinction claire entre deux types de chiffres :

* Entiers : 0 | 1 | -1 | 203568 , etc...
* Flotteurs : 0,23 | 1.0 | -0,3546 | etc.

>[!WARNING]
>
> Designer établit une distinction claire entre les nombres entiers et les nombres flottants : par défaut, vous ne pouvez pas les utiliser ensemble.
> 
> Heureusement, vous pouvez utiliser les nœuds *To Integer* ou To Float pour effectuer des conversions de type.

### Plusieurs valeurs numériques dans la même variable

Selon vos besoins, vous pouvez accumuler jusqu’à 4 valeurs numériques dans la même variable.

Encore une fois, toutes les valeurs doivent être du même type.

Pour ce faire, vous avez le choix entre toutes ces valeurs numériques :

![](variables.resources/image2015-12-18-14-10-36.png)

## Booléen

Un booléen est une valeur binaire pure, ce qui signifie que sa valeur ne peut être que *True* ou *False* (vous pouvez également dire 0 ou 1).
