---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: Découvrez comment les graphes et les Matériaux MDL de composition de Substances fonctionnent ensemble dans Substance 3D Designer pour la création de matériaux.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: graphes et Matériaux MDL de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 1%

---


# graphes et Matériaux MDL de Substance

Cette page décrit les synergies entre les [graphes de Substance](../../compositing-graphs/substance-compositing-graphs.md) et les Graphes MDL, et comment connecter des textures du graphe de Substance [sorties](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) aux entrées de Graphe MDL.

## Vue d’ensemble

Les sorties des graphes de Substance peuvent être *transmises aux paramètres exposés* des Matériaux MDL de deux manières, décrites dans cette page.

Si le Matériau MDL actuellement appliqué dans la vue 3D comporte des paramètres exposés dont le type est *[variable](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)* - ce type peut être défini à l&#39;aide de l&#39;option <b>Modificateur de type</b> dans les propriétés du [paramètre exposé](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), ceux-ci peuvent être connectés à *textures* :

* un paramètre <b>Color</b> peut être connecté aux textures RGBA
* un paramètre <b>Flottant</b> pour les textures en niveaux de gris

Dans ces cas, la valeur uniforme brute est remplacée par un échantillonneur de texture fournissant une valeur variable. Ces échantillonneurs ont un attribut <b>usage</b> défini dans le paramètre exposé, et cet usage permet à Designer de connecter les textures issues des graphes de Substance de données au paramètre approprié dans le Matériau MDL, en *faisant correspondre les utilisations*.

## graphes de Substance dans la vue 3D

Lorsque vous utilisez l&#39;option <b>Afficher les sorties en vue 3D</b> pour un graphe de Substance ou que vous faites glisser un graphe de Substance du panneau <b>Explorateur</b> vers la <b>vue 3D</b>, les sorties sont connectées aux paramètres exposés de *utilisations correspondantes* dans le Matériau MDL actuellement affiché dans la vue 3D.

Les textures individuelles d&#39;un graphe de Substance peuvent être connectées à l&#39;un des paramètres de Matériau MDL qui prennent en charge l&#39;échantillonnage de texture, quel que soit l&#39;identifiant, en appuyant sur RMB sur le nœud de graphe de Substance et en faisant glisser dans la vue 3D. Une liste des utilisations d’échantillonnage disponibles s’affiche et vous pouvez sélectionner l’utilisation cible pour la texture sélectionnée.

![Entrées de Graphe MDL Exposées](../../assets/mdl-graph-inputs-samplers.png "Entrées de Graphe MDL Exposées")

*Les Textures issues d&#39;un graphe de Substance sont connectées aux paramètres exposés d&#39;un Graphe MDL dans la vue 3D*

## graphes de Substance dans les Graphes MDL

Les instances de graphe de Substance peuvent être placées directement dans les Graphes MDL en les faisant glisser du panneau <b>Explorateur</b> vers le Graphe MDL. Les graphes de Substance provenant des <b>fichiers Substance 3D</b> (SBS) et des <b>fichiers de ressources Substance 3D</b> (SBSAR) peuvent être utilisés dans les Graphes MDL.

+++graphe de Substance à partir du fichier Substance 3D (SBS)
![graphe de Substance à partir du fichier SBS dans Graphe MDL](../../assets/mdl-sbs-instance-hl.png "graphe de Substance à partir du fichier SBS dans Graphe MDL")



Instance de *[graphe de Substance](../../compositing-graphs/substance-compositing-graphs.md) à partir de [fichier Substance 3D](../../getting-started/overview/overview.md) (SBS) dans Graphe MDL*

+++

+++graphe de Substance à partir d’un actif Substance 3D (SBSAR)
![graphe de Substance du Fichier sbsar dans le Graphe MDL](../../assets/mdl-sbsar-instance-hl.png "graphe de Substance du Fichier sbsar dans le Graphe MDL")



Instance de *[graphe de Substances](../../compositing-graphs/substance-compositing-graphs.md) à partir de [ressources Substance 3D](../../getting-started/overview/overview.md) (SBSAR) dans Graphe MDL*

+++

Lorsqu&#39;une instance de graphe de Substance est créée, elle apparaît sous la forme d&#39;un *nœud* avec les fonctionnalités suivantes :

* Un connecteur de *sortie tapée* pour chacune des sorties du graphe. Les données de sortie sont saisies comme suit :
  * bitmaps RVBA : couleur (variable)
  * Images bitmap en niveaux de gris : Flottant (variable)
  * Valeurs : faites correspondre le type de valeur (variable)
* Une *entrée* de type coordonnées d&#39;UV pour spécifier les coordonnées d&#39;UV qui doivent être utilisées pour mapper les textures produites par le graphe de Substance. Si cette option n’est pas sélectionnée, la valeur par défaut est un dégradé linéaire classique 0-1 en X et Y dans l’espace UV
* Le nœud est *étiqueté* après l&#39;étiquette de graphe de Substance (ou identifiant si aucune étiquette n&#39;est définie) et sa première sortie bitmap sous forme de vignette

Les propriétés de nœud vous permettent de modifier *toutes les propriétés dynamiques* du graphe de Substance :

* Taille de sortie
* Graine aléatoire
* Paramètres d&#39;entrée
* …

Les propriétés de nœud vous permettent également de définir des paramètres spécifiques à la façon dont les textures sont *mappées* dans le Matériau MDL :

* Répétition
* Utiliser la Taille physique
* Format des normales
* Repère tangent

La sortie du nœud d&#39;instance de graphe de Substance peut être reliée à n&#39;importe quelle entrée de nœud de type correspondant dans le Graphe MDL.

Veuillez noter que la modification de tout paramètre dans la section <b>Paramètres de base SBS</b> implique le recalcul d&#39;une ou plusieurs des sorties du graphe de Substance, qui utilisent le <b>moteur de Substance</b> et impliquent une *surcharge de performances* au-dessus des calculs de Graphe MDL. Attendez-vous à un impact sur les performances lorsque *modifiez un graphe de Substance* qui est instancié dans un Graphe MDL appliqué dans la vue 3D.

>[!WARNING]
>
> Lors de l’utilisation d’un graphe de Substance dans un Graphe MDL, l’exportation du Graphe MDL implique de baker les sorties du graphe de Substance en bitmaps qui seront exportés en tant que textures fournies avec le fichier MDL exporté. Cela signifie que la nature paramétrique du graphe de Substance est *perdu* dans le fichier MDL exporté.
