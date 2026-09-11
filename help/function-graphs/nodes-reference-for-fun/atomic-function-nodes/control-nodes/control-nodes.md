---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/control-nodes.html"
breadcrumb-title: ''
description: Accès aux nœuds de contrôle dans les graphes de fonction Substance 3D Designer pour contrôler le flux et la logique d’exécution.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Contrôle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 1%

---


# Nœuds de contrôle

Cette page décrit les nœuds des [graphes de fonction](../../../../function-graphs/the-function-graph/the-function-graph.md) dont l&#39;objectif est de contrôler le *flux d&#39;exécution*.

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud If...Else](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/IfElse_Node.jpg "Nœud If...Else")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## If...Else

Comme pour les langages de programmation, l&#39;Id... Le nœud Else introduit la possibilité de filtrer le résultat selon des conditions prédéfinies.

</td>
</tr>
</table>

Vous utiliserez ce nœud conjointement avec les [nœuds logiques](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) et les [nœuds de comparaison](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) qui vous aideront à créer la condition à vérifier.

+++Connecteurs d’entrée
<b>Condition</b> *Booléen*\
Condition qui contrôle la sortie du nœud.

<b>Si</b> *Type de variable* La valeur sortie par le nœud si <b>Condition</b> est *True*.

<b>Sinon</b> *Type de variable* La valeur sortie par le nœud si <b>Condition</b> est *False*.

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud de séquence](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/Sequence_Node.jpg "Nœud de séquence")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Séquence

Permet de s’assurer qu’une partie du graphe est calculée avant une autre.

</td>
</tr>
</table>

Ceci est essentiel pour contrôler l&#39;état des variables si elles sont créées, lues et mises à jour.

Pour en savoir plus sur le nœud Séquence, consultez la page [Utilisation des nœuds Set/Sequence](../../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) de cette documentation.

+++Connecteurs d’entrée
<b>Entrée</b> *Type de variable*\
Partie du graphe qui doit être calculée en premier

<b>Dernier</b> *Type de variable*\
Partie du graphe qui doit être calculée en dernier

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud de boucle entière](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/WhileLoop-Node.jpg "Nœud de boucle entière")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Boucle While

Exécute la branche <b>Init</b> une fois, puis itère sur le <b>Cond. de sortie</b>. et les branches <b>Corps en boucle</b> jusqu&#39;à la <b>Cond. de sortie</b> la branche renvoie *True*.

Une fois la boucle terminée, le nœud génère le résultat de la dernière itération du <b>corps de boucle</b>.

</td>
</tr>
</table>

Les boucles ont un nombre maximum implicite d&#39;itérations qui peuvent être désactivées en le réglant à -1.

Les variables conservent leur valeur entre les itérations et sont accessibles dans la condition de sortie (Cond. de sortie).\
Cela signifie que vous pouvez ajouter à une valeur d&#39;index chaque itération et vérifier sa valeur dans la condition de sortie pour contrôler le nombre de boucles dont vous avez besoin.

>[!IMPORTANT]
>
> Nœuds connectés au <b>conteneur de sortie</b> et les branches <b>Corps de boucle</b> ne peuvent pas être connectées à d&#39;autres branches du graphe.

+++Connecteurs d’entrée
<b>Init.</b> *Type de variable*\
Partie du graphe calculée avant la première itération, c&#39;est-à-dire le début de la boucle.

<b>Quitter Cond.</b> *Booléen*\
Condition devant être vraie pour que la boucle s&#39;arrête. Il est recalculé sur chaque itération.\
*Remarque :* le nombre maximal d&#39;itérations est toujours limité au paramètre <b>itérations maximales</b>.

<b>Corps en boucle</b> *Type de variable*\
Le graphe qui bénéficie de la boucle. Il est recalculé sur chaque itération.

+++

+++Paramètres
<b>Max. itérations</b> *Entier*\
Nombre maximal d&#39;itérations effectuées par le nœud.\
Le nœud arrête l&#39;itération lorsque l&#39;un des critères suivants est rempli en premier : ce nombre maximal est atteint ou la condition de sortie devient vraie.\
Ce maximum peut être désactivé en définissant la valeur sur *-1*. À ce stade, seule la condition de sortie peut arrêter les itérations.

Paramétrage de &#39;Max. L&#39;itération de -1 améliore les performances dans les petites boucles, car il y a un compteur de moins pour suivre et mettre à jour.

Cependant, gardez à l&#39;esprit la façon dont le nœud est configuré, car il est possible de produire une <b>boucle infinie</b> qui peut empêcher Designer de répondre.

+++

Consultez ce tutoriel sur le nœud While Loop :
