---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/the-function-graph.html"
breadcrumb-title: ''
description: Découvrez les graphes de fonction de Substance dans Designer pour créer des fonctions personnalisées et des réseaux de nœuds réutilisables.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs > The Substance function graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graphe de la fonction Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Similitudes avec un graphe de Substance

À première vue, le graphe de fonction de Substance est très similaire à un graphe de Substance et le workflow est presque identique.

![graphe de fonction de Substance](the-function-graph.resources/image2015-12-18-11-29-28.png "graphe de fonction de Substance")

## La navigation est similaire

Dans le graphe de fonction Substance, vous pouvez créer et organiser vos nœuds de la même manière que dans un graphe Substance.

vous pouvez accéder aux nœuds de la même manière :

* À partir de la bibliothèque
* en appuyant sur la barre d’espace ou la touche de tabulation
* en cliquant avec le bouton droit et en utilisant le menu Ajouter un nœud

### Le workflow est similaire

Comme dans le graphe Substance, vous construirez votre fonction en enchaînant des séries de nœuds, chacun d&#39;eux utilisant le résultat généré par le(s) précédent(s).

La sortie définit soit la valeur d&#39;un paramètre, soit la sortie du nœud de processeur de pixels.

## Différences avec un graphe de Substance

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Nœuds

Les nœuds disponibles dans le graphe de fonction de Substance sont complètement différents de ceux que vous rencontreriez dans un graphe de Substance.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Liste des nœuds de graphe de fonction de Substance](the-function-graph.resources/image2015-12-18-13-46-55.png "Liste des nœuds de graphe de fonction de Substance")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### La sortie

Contrairement aux graphes de Substance, une fonction ne peut avoir qu&#39;une seule sortie.

Autre point à noter : il n’y a pas de nœud de sortie spécifique où vous branchez votre résultat final. Au lieu de cela, vous pouvez marquer directement comme sortie le nœud qui génère le résultat attendu :

</td>
<td style="border: 0;" valign="top">

![Nœud de sortie du graphe de fonction de Substance](the-function-graph.resources/image2015-12-18-13-49-43.png "Nœud de sortie du graphe de fonction de Substance")

</td>
</tr>
</table>

#### Comment définir le nœud de sortie ?

Pour définir la sortie, cliquez avec le bouton droit de la souris sur le nœud qui génère la sortie attendue, puis cliquez sur *Définir comme nœud de sortie :*

![Définition du nœud de sortie](the-function-graph.resources/setoutputnode.gif "Définition du nœud de sortie")

>[!WARNING]
>
> <b>Vérifiez deux fois le type de résultat généré</b>
> 
> Si vous remarquez que *Définir comme nœud de sortie* est grisé, cela signifie que la valeur générée par le nœud est différente de la valeur attendue par le paramètre ou le processeur de pixels.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

En ce qui concerne les graphes de Substance, vous pouvez importer des fonctions créées dans un autre graphe. Vous pouvez ouvrir le graphe de référence en cliquant dessus avec le bouton droit de la souris, puis en choisissant « Ouvrir la référence » :

</td>
<td style="border: 0;" valign="top">

![Ouvrir le graphe de fonction de Substance référencé](the-function-graph.resources/image2017-6-27-10-44-55.png "Ouvrir le graphe de fonction de Substance référencé")

</td>
</tr>
</table>

Si vous avez un sbs contenant plusieurs fonctions, vous pouvez le glisser-déposer directement dans un graphe de fonction de Substance et choisir la fonction que vous souhaitez importer dans la liste qui apparaît :

![Supprimer le graphe de fonction de Substance du package](the-function-graph.resources/sbsdrag.gif "Supprimer le graphe de fonction de Substance du package")
