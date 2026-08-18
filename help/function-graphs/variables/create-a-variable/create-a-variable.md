---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: Apprenez à créer des variables personnalisées dans les graphiques fonctionnels Substance 3D Designer pour des valeurs et des paramètres réutilisables.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Création d’une variable
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Création d’une variable

Il existe différentes façons de créer une variable dans Substance 3D Designer :

* Utilisation d’un paramètre d’entrée
* Utilisez un nœud Set.

## Utilisation d’un paramètre d’entrée

Lorsque vous créez un paramètre d’entrée, une variable est créée et associée à celui-ci. Vous pouvez ensuite réutiliser cette variable dans n’importe quelle fonction de votre graphique.

Par conséquent, un seul paramètre exposé peut avoir une influence sur plusieurs parties de votre graphique.

## Utilisation d’un nœud Set

Un nœud Set est un nœud disponible uniquement dans les graphiques de fonctions :

Cela permet à l’utilisateur de créer une variable personnalisée :

* Le nom est déclaré dans les paramètres.
* La valeur est définie par l’entrée.

### Comment utiliser le nœud *Set*

L&#39;utilisation d&#39;un nœud Set est un peu particulière :

lorsque vous le déclarez, il n’est disponible que dans le graphique, ce qui, par défaut, n’est pas vraiment utile (après tout, vous pouvez déjà générer sa valeur avec des liens).

Par conséquent, vous devez déclarer cette nouvelle variable, en dehors de ce graphique.

pour ce faire, vous devez utiliser un nœud de séquence et effectuer les étapes suivantes :

* Lier le nœud de sortie réel à la « dernière » entrée du nœud de séquence
* Liez le nœud Set à l&#39;entrée « In » du nœud de séquence.
* Définir la séquence comme nœud de sortie

Lorsque vous aurez fait cela, la variable sera disponible dans l&#39;autre graphique de fonction du même nœud.

>[!WARNING]
>
> Lorsqu&#39;un nœud est traité par le moteur Substance, ses paramètres (et les fonctions qui pourraient les contrôler) sont lus de haut en bas. Par conséquent, un nœud Set ne peut être accessible que par les paramètres situés en dessous dans la pile de paramètres de nœud.

>[!NOTE]
>
> Si vous avez plusieurs variables à créer, répétez simplement l&#39;opération de création de nœuds *Set* et *Sequence* et définissez le dernier nœud de séquence comme nœud de sortie :
> 
> ![](../../../assets/image2015-12-18-18-43-8.png)
