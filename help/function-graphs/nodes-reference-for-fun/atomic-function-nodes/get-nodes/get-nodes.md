---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: Accédez aux nœuds Get dans les graphes de fonction Substance 3D Designer pour récupérer les valeurs et les données des variables.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 6%

---


# Variables

Les variables permettent de <b>stocker des valeurs</b> pour les récupérer ultérieurement (<b>Get</b>) et/ou les modifier (<b>Set</b>).

![graphe de fonction de Substance - Get float](get-nodes.resources/assign-getfloat.gif "graphe de fonction de Substance - Get float"){zoomable="yes"}

Ce que fait essentiellement un nœud Get, c&#39;est d&#39;attraper une variable dynamique, et de la retourner à partir de la sortie des nœuds Get pour l&#39;utiliser dans une fonction. Ces nœuds Get constituent le lien entre les Paramètres d&#39;entrée définis dans les [paramètres de graphe](../../../../compositing-graphs/graph-parameters/graph-parameters.md) et les [fonctions de paramètre](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).

Chaque fois que vous utilisez un nœud Get, vous devez choisir une valeur disponible dans le menu déroulant. Les nœuds Get <b>récupèrent une valeur du type correspondant</b>. Cela signifie que vous ne verrez que les options valides dans le menu d&#39;un nœud Get, vous ne pouvez jamais choisir une option non valide. Si une variable n’est pas disponible, cela signifie qu’il existe une incompatibilité de type

Il existe un certain nombre de <b> « Variables système »</b> : variables spéciales prédéfinies que vous ne pouvez pas déclarer vous-même. Ceux-ci sont très importants, et pour les nœuds ci-dessous, il est indiqué quelles variables système sont disponibles.

Lorsqu&#39;un paramètre est [exposé](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), il consiste à lui appliquer une fonction de paramètre qui inclut uniquement un nœud Get du type approprié.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Obtenir

</td>
<td style="border: 0;" valign="top">

### Définir

</td>
<td style="border: 0;" valign="top">

### Est défini

</td>
</tr>
</table>

## Obtenir

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Obtenir float2 - Icône](get-nodes.resources/fn_variables_getfloat2.png "Obtenir float2 - Icône"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Ces nœuds vous permettent de récupérer la valeur d&#39;une variable qui existe *dans l&#39;étendue actuelle*.

Le nom de la variable en cours de récupération est défini dans le dock Propriétés.

</td>
</tr>
</table>

Les nœuds &#39;Get&#39; présentent des limitations dont vous devez tenir compte :

* <b>Ils sont tapés</b>. Vous devez donc vous assurer que la variable contient une valeur du même type que le nœud. Les incohérences de type sont signalées dans la console.
* <b>Ils ne vérifient pas l&#39;existence de la variable</b> dans l&#39;étendue actuelle. Des variables introuvables sont signalées dans la console.
* Dans les fonctions complexes utilisant des nœuds de flux de contrôle tels que Séquence, soyez attentif à l&#39;<b>ordre dans lequel vous définissez et obtenez des variables</b>. Lorsque Designer détecte un cas de paramètre « Obtenir avant ensemble », il est signalé dans la console.

>[!NOTE]
>
> Variables intégrées
> 
> Plusieurs nœuds « Get » offriront des variables intégrées pour accéder aux valeurs existantes en fonction du contexte actuel - par exemple : la position actuelle des pixels dans un Processeur de pixels, le mode de répétition actuel d&#39;un nœud, ...
> 
> Toutes les variables intégrées sont répertoriées dans [cette page dédiée](../../../../function-graphs/variables/system-variables/system-variables.md).

### Obtention des nœuds

+++Flottants
![Obtenir le flottement - Icône](get-nodes.resources/fn_variables_getfloat.png "Obtenir le flottement - Icône"){width="200px"}



Obtenir flottant

![Obtenir float2 - Icône](get-nodes.resources/fn_variables_getfloat2.png "Obtenir float2 - Icône"){width="200px"}



Obtenir flottant2

![Obtenir float3 - Icône](get-nodes.resources/fn_variables_getfloat3.png "Obtenir float3 - Icône"){width="200px"}



Obtenir Flottant3

![Obtenir float4 - Icône](get-nodes.resources/fn_variables_getfloat4.png "Obtenir float4 - Icône"){width="200px"}



Obtenir flottant4

+++

+++Entiers
![Obtenir Un entier - Icône](get-nodes.resources/fn_variables_getint.png "Obtenir Un entier - Icône"){width="200px"}



Obtenir entier

![Obtenir entier 2 - Icône](get-nodes.resources/fn_variables_getint2.png "Obtenir entier 2 - Icône"){width="200px"}



Obtenir entier2

![Obtenir entier 3 - Icône](get-nodes.resources/fn_variables_getint3.png "Obtenir entier 3 - Icône"){width="200px"}



Obtenir entier3

![Obtenir entier 4 - Icône](get-nodes.resources/fn_variables_getint4.png "Obtenir entier 4 - Icône"){width="200px"}



Obtenir entier4

+++

+++Autres
![Obtenir booléen - Icône](get-nodes.resources/fn_variables_getboolean.png "Obtenir booléen - Icône"){width="200px"}



Obtenir booléen

![Obtenir la chaîne - Icône](get-nodes.resources/fn_variables_getstring.png "Obtenir la chaîne - Icône"){width="200px"}



Obtenir chaîne

+++

## Définir

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Définir : icône de nœud](get-nodes.resources/fn_variables_set.png "Définir : icône de nœud"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Texte

</td>
</tr>
</table>

## Est défini

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Est défini : icône de nœud](get-nodes.resources/fn_variables_isdefined.png "Est défini : icône de nœud"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Texte

</td>
</tr>
</table>
