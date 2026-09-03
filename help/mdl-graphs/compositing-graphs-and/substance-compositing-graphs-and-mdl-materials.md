---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: Découvrez comment les graphiques de composition de Substances et les matériaux MDL fonctionnent ensemble dans Substance 3D Designer pour la création de matériaux.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graphiques de Substance et matériaux MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 1%

---


# Graphiques de Substance et matériaux MDL

Cette page décrit les synergies entre les [graphes en Substances](../../compositing-graphs/substance-compositing-graphs.md) et les graphes MDL, et explique comment connecter les textures des [sorties](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) des graphes en Substances aux entrées des graphes MDL.

## Vue d’ensemble

Les sorties des graphiques de Substance peuvent être *transmises aux paramètres exposés* des matériaux MDL de deux manières, décrites dans cette page.

Si le Matériau MDL actuellement appliqué dans la vue 3D comporte des paramètres exposés dont le type est *[variable](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)* - ce type peut être défini à l&#39;aide de l&#39;option <b>Modificateur de type</b> dans les propriétés du [paramètre exposé](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), ceux-ci peuvent être connectés à *textures* :

* un paramètre <b>Color</b> peut être connecté aux textures RGBA
* paramètre <b>Float</b> pour les textures en niveaux de gris

Dans ces cas, la valeur uniforme brute est remplacée par un échantillonneur de texture fournissant une valeur variable. Ces échantillonneurs ont un attribut <b>usage</b> défini dans le paramètre exposé, et cette utilisation permet à Designer de connecter les textures générées par les graphiques de Substance au paramètre approprié dans le matériau MDL, en *faisant correspondre les utilisations*.

## Graphes en Substance dans la vue 3D

Lorsque vous utilisez l&#39;option <b>Afficher les sorties en vue 3D</b> pour un graphique en Substances ou que vous faites glisser un graphique en Substances du panneau <b>Explorateur</b> vers la <b>vue 3D</b>, les sorties sont connectées aux paramètres exposés de *utilisations correspondantes* dans le matériau MDL actuellement affiché dans la vue 3D.

Les textures individuelles d&#39;un graphique de Substance peuvent être connectées à n&#39;importe lequel des paramètres de matériau MDL qui prennent en charge l&#39;échantillonnage de texture, quel que soit l&#39;identifiant, en appuyant sur RMB sur le nœud du graphique de Substance et en faisant glisser dans la vue 3D. Une liste des utilisations d’échantillonnage disponibles s’affiche et vous pouvez sélectionner l’utilisation cible pour la texture sélectionnée.

![Entrées de graphique MDL exposées](substance-compositing-graphs-and-mdl-materials.resources/substance-compositing-graphs-and-mdl-materials-01.png "Entrées de graphique MDL exposées")

*Les textures générées par un graphique en Substance sont connectées aux paramètres exposés d&#39;un graphique MDL dans la vue 3D*

## Graphiques de Substance dans les graphiques MDL

Les instances de graphiques de Substance peuvent être placées directement dans les graphiques MDL en les faisant glisser du panneau <b>Explorateur</b> vers le graphique MDL. Les graphiques de Substance provenant des <b>fichiers Substance 3D</b> (SBS) et des <b>fichiers de ressources Substance 3D</b> (SBSAR) peuvent être utilisés dans les graphiques MDL.

+++Graphique de Substance à partir d’un fichier Substance 3D (SBS)
![Graphique de Substance à partir du fichier SBS dans le graphique MDL](substance-compositing-graphs-and-mdl-materials.resources/substance-compositing-graphs-and-mdl-materials-02.png "Graphique de Substance à partir du fichier SBS dans le graphique MDL")



*[Instance de graphique de Substance](../../compositing-graphs/substance-compositing-graphs.md) à partir de [fichier Substance 3D](../../getting-started/overview/overview.md) (SBS) dans le graphique MDL*

+++

+++Graphique de Substance à partir d’un actif Substance 3D (SBSAR)
![Graphique de Substance à partir du fichier SBSAR dans le graphique MDL](substance-compositing-graphs-and-mdl-materials.resources/substance-compositing-graphs-and-mdl-materials-03.png "Graphique de Substance à partir du fichier SBSAR dans le graphique MDL")



*[Instance de graphique de Substance](../../compositing-graphs/substance-compositing-graphs.md) de [ressource Substance 3D](../../getting-started/overview/overview.md) (SBSAR) dans le graphique MDL*

+++

Lorsqu&#39;une instance de graphique de Substance est créée, elle s&#39;affiche comme un *nœud* avec les fonctionnalités suivantes :

* Connecteur de *sortie tapée* pour chacune des sorties du graphique. Les données de sortie sont saisies comme suit :
  * bitmaps RVBA : couleur (variable)
  * Images bitmap en niveaux de gris : flottantes (variables)
  * Valeurs : faites correspondre le type de valeur (variable)
* Une *entrée* de type Coordonnées UV pour spécifier les coordonnées UV qui doivent être utilisées pour mapper les textures produites par le graphique de Substance. Si cette option n’est pas sélectionnée, la valeur par défaut est un dégradé linéaire classique de 0 à 1 dans X et Y dans l’espace UV
* Le nœud est *étiqueté* après le libellé du graphique de Substance (ou l’identificateur si aucun libellé n’est défini) et sa première sortie bitmap sous forme de vignette

Les propriétés de nœud vous permettent de modifier *toutes les propriétés dynamiques* du graphique de Substance :

* Taille de sortie
* Graine aléatoire
* Paramètres d’entrée
* …

Les propriétés de nœud vous permettent également de définir des paramètres spécifiques à la façon dont les textures sont *mappées* dans le matériau MDL :

* Répétition
* Utiliser la Taille physique
* Format des normales
* Repère tangent

La sortie du nœud d&#39;instance de graphique de Substance peut être reliée à n&#39;importe quelle entrée de nœud de type correspondant dans le graphique MDL.

Veuillez noter que la modification de tout paramètre dans la section <b>Paramètres de base SBS</b> implique le recalcul d&#39;une ou plusieurs des sorties du graphique de Substance, qui utilise le <b>moteur de Substance</b> et implique une *surcharge de performances* en plus des calculs du graphique MDL. Attendez-vous à un impact sur les performances lorsque vous *modifiez un graphique de Substance* qui est instancié dans un graphique MDL appliqué dans la vue 3D.

>[!WARNING]
>
> Lors de l’utilisation d’un graphique de Substance dans un graphique MDL, l’exportation du graphique MDL implique la conversion des sorties du graphique de Substance en bitmaps qui seront exportés sous forme de textures fournies avec le fichier MDL exporté. Cela signifie que la nature paramétrique du graphique de Substance est *perdu* dans le fichier MDL exporté.
