---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/properties.html"
breadcrumb-title: ''
description: Utilisez le panneau Propriétés de Substance 3D Designer pour afficher et modifier les propriétés de nœud et les paramètres de graphique.
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Propriétés
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Propriétés

Cette page présente le panneau <b>Propriétés </b> de Substance 3D Designer, sa mise en page et les différents déploiements, catégories et paramètres disponibles. Il est axé sur les propriétés des [graphiques de Substance](../../compositing-graphs/substance-compositing-graphs.md). Les [graphiques fonctionnels](../../function-graphs/function-graphs.md) et les [graphiques FX-Map](../../function-graphs/fxmaps/fxmaps.md) ont des mises en page plus simples.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Vue d’ensemble

Le panneau <b>Propriétés</b>est un panneau contextuel qui change en fonction de votre sélection dans [la vue Graphique](../../interface/the-graph-view/the-graph-view.md) et la fenêtre [Explorateur](../the-explorer-window/the-explorer-window.md).

</td>
<td style="border: 0;" valign="top">

![Dock des propriétés](properties.resources/properties-01.png "Dock des propriétés")

</td>
</tr>
</table>

Il vous permet de modifier les propriétés des nœuds et des ressources sélectionnés. Avec [la vue Graphique](../../interface/the-graph-view/the-graph-view.md), il s&#39;agit probablement du deuxième panneau d&#39;interface utilisateur le plus utilisé dans Designer.

Le panneau Propriétés est divisé en plusieurs groupes de fonctions différents, en fonction de votre sélection, par exemple :

* <b>Paramètres de base</b> et <b>Paramètres d&#39;entrée</b> ou <b>Paramètres spécifiques</b> pour les nœuds
* <b>Attributs</b> et <b>Métadonnées</b> pour la plupart des nœuds et des packs

Une caractéristique essentielle de l&#39;écosystème de Substance, [Exposer les paramètres](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), se fait via le panneau Propriétés.

>[!NOTE]
>
> La plupart des champs numériques prennent en charge les *formules mathématiques de base* comme entrée, par exemple, `17+3.5`, `7/3`, `(4+2)*3`. Appuyez sur *Entrée* pour valider la formule. Le résultat sera saisi dans le champ. Si la formule n’est pas valide, le champ revient à sa valeur précédente.\
> Certains champs numériques d&#39;autres parties de l&#39;application, tels que la boîte de dialogue [Exposer le paramètre](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), prennent également en charge cette fonctionnalité.

## Nœuds et graphiques de Substance

Les nœuds et les [graphes de Substance](../../compositing-graphs/substance-compositing-graphs.md) ont un ensemble de catégories de propriétés qui se chevauchent légèrement et leur fonctionnalité est similaire.

Les <b>paramètres de base</b> et les <b>attributs</b> sont identiques entre les nœuds et les graphiques.

Les nœuds offrent <b>paramètres spécifiques</b> ou<b> paramètres d&#39;instance</b> (selon qu&#39;il s&#39;agit de [Noeuds atomiques](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) ou de [instances](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)), ainsi que des <b>valeurs d&#39;entrée</b> pour l&#39;utilisation de [valeurs](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

Les nœuds atomiques [d&#39;entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) et [de sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) sont des exceptions, car ils comportent des <b>attributs d&#39;intégration</b> et des <b>conditions</b> de visibilité. Ces deux ensembles de propriétés sont également accessibles de manière centralisée dans les propriétés Graph, sous Entrées et Sorties.

Les graphiques comportent quelques catégories supplémentaires. Les <b>paramètres d&#39;entrée</b> répertorient les [paramètres exposés](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), les <b>entrées</b> et les <b>sorties</b> répertorient toutes les propriétés des nœuds d&#39;entrée et de sortie. [Toutes les propriétés de graphique sont expliquées en détail sur une page dédiée.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## Ressources et packs

Le panneau Propriétés répond également aux modifications de sélection dans l&#39;[Explorateur](../the-explorer-window/the-explorer-window.md). Cela peut servir d&#39;autre moyen de sélectionner un graphique (au lieu de double-cliquer sur une zone vide), et vous permet également de modifier les propriétés du package et de la [ressource](../../resources/resources.md).

Les packages comportent des sections **Informations**, **Attributs** et **Métadonnées**. [Les métadonnées du package sont décrites sur une page dédiée.](../../package-metadata/package-metadata.md)

Les ressources ont des propriétés spécifiques à leur type, [détaillées sur des pages dédiées](../../resources/resources.md).
