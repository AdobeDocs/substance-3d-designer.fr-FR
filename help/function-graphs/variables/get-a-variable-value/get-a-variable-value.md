---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: Découvrez comment récupérer des valeurs de variable dans les graphiques fonctionnels Substance 3D Designer à l’aide du nœud Obtenir la variable.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Obtenir une valeur de variable
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Obtenir une valeur de variable

Pour utiliser une variable dans une fonction, vous devez l’« appeler », ce qui signifie que vous devez importer la valeur de la variable dans la fonction.

Pour ce faire, vous devez utiliser un nœud *Get* :

![](get-a-variable-value.resources/get-a-variable-value-01.png)

Il existe différents types de nœuds Get : choisissez le bon en fonction du type de valeur que vous souhaitez importer :

![](get-a-variable-value.resources/get-a-variable-value-02.png)

## Affectation d&#39;une variable à un nœud Get

Par défaut, un nœud get affichera un signe d&#39;avertissement : cela signifie qu&#39;il n&#39;est pas encore lié à une variable.

Pour lier une variable, accédez aux paramètres et choisissez une variable dans la liste « Variables/Get \*\*\* » (\*\*\*sera remplacé par le type de valeur que votre nœud Get peut appeler).

Le nom de la variable s’affiche dans le nœud :

![](get-a-variable-value.resources/get-a-variable-value-03.gif)

Notez que seules les variables qui proviennent du même type du nœud Get apparaîtront dans la liste.

>[!WARNING]
>
> Notez que les variables créées avec un nœud *Set* n&#39;apparaîtront pas dans une liste de nœuds *Get*.
> 
> Mais vous pouvez toujours obtenir la variable en écrivant manuellement le nom dans la liste.
> 
> N&#39;oubliez pas que vous pouvez simplement appeler une variable créée avec un nœud Set, si :
> 
> * Les nœuds Get et Set se trouvent dans des graphiques de fonction contrôlant les paramètres d&#39;un même nœud
> * Le paramètre contrôlé par le graphique de nœud *Get* est identique ou se trouve sous le paramètre du graphique de nœud *Set*, dans la pile de paramètres.
