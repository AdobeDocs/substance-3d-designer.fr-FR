---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: Utilisez des instances de graphe et des sous-graphes pour créer des composants de graphe réutilisables et des workflows de matériau modulaire.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Instances de graphe et sous-graphes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# Instances de graphe et sous-graphes

![](graph-instances-sub-graphs.resources/sub-graph.png)

Les Instances de graphe sont des nœuds qui <b>font référence à un autre graphe</b>. Un graphe référencé par un instancier dans un graphe hôte peut être appelé <b>sous-graphe</b> du graphe hôte.

L’utilisation d’instances permet de rendre un graphe réutilisable plusieurs fois dans un ou plusieurs graphes, même entre différents packages.

## Pourquoi devrais-je utiliser des instances de graphe ?

<b>La division des graphes en plusieurs sous-graphes</b> vous permet de travailler *beaucoup* plus efficacement<b>.</b>

Chaque fois que vous dupliquez une chaîne de nœuds dans Designer, vous pouvez probablement la diviser en un sous-graphe pour faciliter sa réutilisation et sa mise à jour.

>[!NOTE]
>
> Un fichier de projet illustrant la configuration simple d&#39;un sous-graphe pour un filtre *personnalisé* est disponible dans la section [Exemples de graphes de Substance](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) de cette documentation.

### Comment créer une instance de graphe ?

Faites glisser un graphe A de l&#39;Explorateur vers un autre graphe B pour créer un instancier <b>référençant le graphe A</b>.

Les nœuds peuvent être rapidement divisés en un nouveau graphe en sélectionnant les nœuds et en utilisant l&#39;option « Créer un graphe à partir de la sélection » dans le menu contextuel. Vous êtes ensuite invité à définir l’identifiant du nouveau graphe, qui doit être unique.

Notez que si les nœuds sélectionnés étaient connectés à d&#39;autres nœuds du graphe, vous devez également créer des nœuds [Entrée](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) et [Sortie](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) dans le nouveau graphe pour reporter ces connexions sur le sous-graphe.

En outre, le remplacement des nœuds d&#39;origine par un instancier référençant le nouveau graphe doit être effectué manuellement par la suite.

Enfin, vous devez décider si le sous-graphe doit être exposé aux utilisateurs lorsque vous publiez votre projet sur un Fichier sbsar partageable. Voir le paramètre « Exposé dans SBSAR » dans les [propriétés du graphe](../../../compositing-graphs/graph-parameters/graph-parameters.md).

### Un mot sur l&#39;héritage

Un autre avantage des sous-graphes est que chaque instance d&#39;un sous-graphe peut <b>s&#39;adapter au contexte</b> dans lequel il est utilisé. En d’autres termes, deux instances d’un même graphe peuvent avoir des résolutions de sortie, des débits et des modes de répétition différents.

Il s&#39;agit d&#39;un <b>concept essentiel</b> de travail dans les graphes. Nous vous recommandons vivement d&#39;en savoir plus sur [l&#39;héritage dans les graphes de Substance](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) lorsque vous serez prêt à aller plus loin avec les instances.

Notez que si les concepts d&#39;instance de graphe et de sous-graphe s&#39;appliquent également aux graphes de fonction de Substance, l&#39;héritage décrit dans cette page ne s&#39;applique qu&#39;aux graphes de Substance.

### Puis-je ajouter mes propres instances de graphe à la bibliothèque de nœuds ?

<b>Oui, c&#39;est possible </b>mais cela nécessite une configuration spécifique. Pour en savoir plus, consultez la page [Gestion du contenu et des filtres personnalisés](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) de cette documentation.

### Pouvez-vous inspecter le graphe source d’une instance de graphe ?

![(coche)](graph-instances-sub-graphs.resources/check.svg) Oui, et *uniquement* pour les instances de graphes chargés à partir d&#39;un **fichier Substance 3D (SBS)**. Ces instanciers ont un libellé *rouge foncé*.\
Cliquez avec le bouton droit sur le nœud pour ouvrir son menu contextuel et sélectionnez l&#39;option **Ouvrir la référence**.

>[!NOTE]
>
> Lors de l&#39;inspection du graphe source, vous pouvez utiliser les données d&#39;entrée du graphe de l&#39;instance si l&#39;option **Modification contextuelle** est *cochée* dans la section **Graphe** des [Préférences](../../../interface/preferences-window/preferences-window.md).

![(moins)](graph-instances-sub-graphs.resources/forbidden.svg) Il n&#39;est *pas* possible d&#39;inspecter les graphes chargés à partir d&#39;instances de **ressources Substance 3D (SBSAR)**, car ceux-ci sont déjà compilés. Vous ne pouvez charger la ressource que dans le panneau **Explorateur** pour inspecter la liste des graphes exposés et leurs paramètres. Ces instanciers ont un libellé *vert*.\
Cliquez avec le bouton droit sur le nœud pour ouvrir son menu contextuel et sélectionnez l&#39;option **Charger le package**.

>[!NOTE]
>
> **Noeuds atomiques**
> 
> Les nœuds *atomiques* sont implémentés directement via le code dans le moteur de Substance de données et ne sont *pas* des instances de graphes, d&#39;où le nom atomic : ce sont les *plus petits composants* pour *tous* les autres nœuds dans [graphes de Substance de données](../../../compositing-graphs/substance-compositing-graphs.md).
