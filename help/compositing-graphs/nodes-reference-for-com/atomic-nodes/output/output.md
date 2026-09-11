---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sortie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 31d4d930c789d693362ef3a16c72016bd030a89b
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%

---


# Sortie

<table>
<tr style="border: 0;">
<td style="border: 0; width: 30%; vertical-align: top">

![Noeud atomique : Sortie](output.resources/comp_output_1.png "Noeud atomique : Sortie"){width="200px"}

</td>
<td style="border: 0; vertical-align: top">

Le nœud Output spécifie le <b>résultat</b> d&#39;un graphe de Substance de données ou l&#39;un de ses résultats si plusieurs nœuds Output y sont présents.

L&#39;image ou la valeur connectée au nœud de sortie d&#39;un graphe est générée par n&#39;importe quel [instancier](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) représentant ce graphe et peut [être exportée en tant que sortie du graphe](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md).

</td>
</tr>
</table>

De même, lorsqu&#39;un [Fichier sbsar publié](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) inclut ce graphe, ce fichier peut générer cette image dans n&#39;importe quelle intégration ou plug-in qui consomme le fichier.

Il dispose d&#39;un seul emplacement d&#39;entrée qui est indépendant du type, ce qui signifie qu&#39;il saisit lui-même après le type de données qui lui est connecté.

Il n&#39;a pas de paramètres, mais plutôt des attributs qui sont d&#39;une grande importance pour étiqueter correctement la sortie et la mettre à son usage prévu.

Chaque graphe de Substance doit avoir *au moins un* nœud de sortie. Si aucune sortie n&#39;existe, le graphe ne peut jamais renvoyer de résultat réel et un [avertissement](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md) est déclenché.

## Attributs

|                             |                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Identifiant</b> *Chaîne* | Identifiant unique de la sortie. Cette propriété ne peut pas rester vide et ne peut pas contenir de caractères spéciaux ou d&#39;espaces.   L&#39;identifiant est utilisé car le libellé du nœud est la propriété « Label » laissée vide. Il peut également être utilisé pour nommer [textures exportées](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). |
| <b>Description</b> *Chaîne* | Description facultative utilisée comme info-bulle de la sortie : graphes de Substance. |
| <b>Libellé</b> *Chaîne* | Il est utilisé comme libellé pour le nœud de sortie et son connecteur correspondant dans [instanciers](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) représentant ce graphe. L’étiquette peut contenir des espaces et des caractères spéciaux. |
| <b>Données utilisateur</b> *Chaîne* | Métadonnées facultatives pouvant être utilisées pour des opérations de filtrage spécifiques. [Substance 3D Painter](https://www.adobe.com/products/substance3d/apps/painter.html) utilisez ces données pour [piloter certaines fonctionnalités](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/content/creating-custom-effects/user-data).. |
| <b>Groupe</b> *Chaîne* | Attribut utilisé pour regrouper les sorties afin de [lier les modes de création](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) de Designer.   Les sorties avec un attribut « Group » identique sont présentées comme une connexion unique dans le mode de création de lien « Compact Matériau ». |

## Attributs d&#39;intégration

Ce sont des attributs destinés à être utilisés par des intégrations/plug-ins qui consomment le graphe dans un [Fichier sbsar publié](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).

En tant que tels, ils n&#39;ont aucun impact sur le format des [exportations bitmap](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). En outre, seul l&#39;attribut <b>Utilisation</b> est utilisé dans Designer. Pour plus d&#39;informations, voir ci-dessous.

+++ Utilisation

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Composant</b> *Chaîne* | Utilisé pour mapper certains canaux de texture aux entrées de shader SVBRDF appropriées dans les workflows AxF. |
| <b>Utilisation</b> *Chaîne* | Définit le type et l&#39;utilisation du nœud de sortie. Cette propriété est importante car elle entraîne :<ul data-preserve-html="true"> <li data-preserve-html="true">Connexion des nœuds dans les graphes de Substance lors de l&#39;utilisation de [modes de création de liens](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) </li> <li data-preserve-html="true">Connexion des textures aux shaders dans la vue 3D (voir ci-dessous : &#39;[À propos du rôle des utilisations dans la vue 3D](#about-the-role-of-usages-in-the-3d-view)&#39;)</li> <li data-preserve-html="true">Connexion de textures aux matériaux dans les intégrations/plug-ins</li> </ul> |
| <b>Espace colorimétrique</b> *Chaîne* | Définit l’espace colorimétrique dans lequel cette sortie doit être interprétée. Est utilisé par certaines intégrations dans d’autres applications et n’a aucun impact sur Designer. |

+++

### A propos du rôle des usages dans la vue 3D

Les sorties du graphe étant souvent destinées à être le résultat final d&#39;un canal de texture spécifique, les sorties peuvent être automatiquement envoyées à l&#39;échantillonneur approprié du shader utilisé dans la vue 3D.

En effet, une sortie dont la propriété <b>Utilisation</b> *correspond à une utilisation d&#39;échantillonnage* dans la vue 3D sera connectée à cet échantillonnage. Par exemple, une sortie avec une utilisation `basecolor` sera connectée à l&#39;échantillonneur `basecolor` du shader vue 3D. (En savoir plus : [Afficher les données en vue 3D](../../../../interface/3d-view/3d-view.md#view-data-in-3d-view))

Cliquez sur RMB dans une zone vide de la [Vue du graphe](../../../../interface/the-graph-view/the-graph-view.md) et sélectionnez l&#39;option <b>Afficher les sorties en vue 3D</b> dans le menu contextuel pour connecter toutes les sorties à des échantillonneurs vue 3D avec *utilisations correspondantes*.

>[!IMPORTANT]
>
> Si plusieurs utilisations sont configurées pour, par exemple, attribuer des utilisations aux canaux dans une texture compactée, seule la *première utilisation* de la liste sera connectée à la vue 3D. Il s’agit d’une limitation connue.

## Sortie par défaut

Lorsqu’un graphe a plusieurs sorties, l’une d’elles peut être définie comme sortie par défaut pour ce graphe. Cette option spécifie laquelle des sorties doit être utilisée pour :

* La vignette de tout instancier représentant ce graphe
* Affichage de ces instanciers dans la vue 2D
* Vignette de ce graphe dans la bibliothèque (apprenez à ajouter vos propres ressources [ici](../../../../interface/preferences-window/project-settings/project-settings.md))

Cette fonction vous permet d&#39;organiser les sorties du graphe dans n&#39;importe quel ordre, indépendamment de la façon dont le graphe sera visualisé en tant que nœud.

Pour définir un nœud de sortie comme sortie par défaut d’un graphe :

* Cliquez avec le bouton droit sur un nœud Sortie et sélectionnez l’action « Définir comme sortie par défaut » dans le menu contextuel.
* Dans les propriétés du nœud de sortie, utilisez le bouton « Définir par défaut » dans l&#39;en-tête de la section « Attributs ».

Voici un exemple d’instanciers avant et après la définition d’une sortie par défaut :

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="output.resources/defaultouput2.png" alt="defaultouput2">
      <br><i>Avant</i>
    </td>
    <td style="border: 0">
      <img src="output.resources/defaultouput1.png" alt="defaultouput1">
      <br><i>Après</i>
    </td>
  </tr>
</table>
