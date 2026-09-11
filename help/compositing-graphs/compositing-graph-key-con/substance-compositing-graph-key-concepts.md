---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: Découvrez les concepts clés des graphes de composition de Substances, notamment les nœuds, les connexions et les fondamentaux du workflow.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Concepts clés du graphe Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%

---


# Concepts clés du graphe Substance

Cette page répertorie les concepts importants à comprendre pour l’utilisation des graphes de Substance dans Substance 3D Designer.

## Sous-graphes/Publication

[La publication d&#39;un graphe](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) ou la création d&#39;un sous-graphe sont deux concepts abstraits très similaires. Cela signifie que n&#39;importe quel graphe ou réseau de nœuds peut être « assemblé » et transformé en une ressource réutilisable et autonome. La création de [sous-graphes](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) s&#39;effectue principalement au sein de l&#39;application pour rendre certains contenus réutilisables dans un workflow efficace et intelligent, car cela évite de dupliquer un ensemble de nœuds à l&#39;infini. La publication implique une étape supplémentaire pour exporter au format SBSAR (Substance 3D Asset), ce qui rend votre graphe de réseau de nœuds utilisable en dehors de l’application, par exemple lorsque vous créez un matériau pour le Moteur irréel.

Les entrées, les sorties et les Paramètres exposés sont extrêmement importants pour ce concept, car ils sont les seuls moyens d’interagir avec le graphe une fois qu’il est utilisé comme sous-graphe ou comme actif Substance 3D publié. Les raisons sont les suivantes :

* Aucune sortie signifie que votre graphe <b>ne génère rien</b>, aucune donnée du tout.
* Aucun paramètre exposé signifie que votre graphe <b>ne peut pas être personnalisé</b> de quelque manière que ce soit. Vous ne pouvez pas définir des éléments tels que l’intensité d’un effet, l’opacité d’une image fusionnée, la couleur d’une zone spécifique, etc.
* L&#39;absence d&#39;entrée signifie que, dans certains cas, vous ne pourrez pas personnaliser le résultat d&#39;un graphe avec<b> vos propres données d&#39;image</b>, telles que des maps de maillage bakées pour générer des effets à partir de, une image d&#39;entrée pour appliquer un flou ou un masque personnalisé pour isoler certaines zones d&#39;une image.

## Entrées et sorties

Une [sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)est un nœud qui génère un seul résultat 2D. C&#39;est un point de terminaison, une terminaison pour votre graphe, un résultat fini. Seules les données connectées à une sortie peuvent être exportées en dehors de Designer, voire utilisées dans d’autres graphes.

Voici quelques informations à connaître sur les sorties :

* Vous pouvez avoir autant de sorties que vous le souhaitez, mais vous devez en avoir <b>au moins une</b>.
* Une sortie peut être de <b>n&#39;importe quelle résolution</b> jusqu&#39;à 8 192 px de large ou de haut, elle peut être de<b> couleur ou en niveaux de gris</b> et peut être exportée vers n&#39;importe quel type de fichier pris en charge.
* Les sorties peuvent et doivent être <b>nommées de manière unique</b> pour les identifier, ce qui est utile lors de l&#39;exportation.
* Chaque connecteur à droite d’un nœud est en fait une sortie (voir « Sous-graphes pour plus d’informations »).

Une [entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) est similaire à une sortie. Il s&#39;agit d&#39;un emplacement vide et ouvert auquel vous ou un autre utilisateur pouvez connecter vos propres données. Il permet de créer un graphe qui, dans des données d’image externes définies par l’utilisateur, modifie une image d&#39;entrée (un flou ou un réglage Contraste par exemple).

Voici quelques informations à connaître sur les entrées :

* Les entrées sont entièrement <b>facultatives</b>. Vous ne devez les ajouter qu&#39;en cas de besoin. Il n&#39;y a pas de montant minimum ou maximum.
* Les entrées ont une résolution définie (généralement liée au graphe) que vous définissez, ainsi que s’il s’agit de niveaux de gris ou de couleurs. Tout ce qui y est connecté sera converti pour correspondre à ceci.
* Les entrées peuvent être des fichiers bitmap de votre disque dur, d’autres graphes, des calques de Painter ou Alchemist, etc.
* Chaque connecteur à gauche d’un nœud est une entrée (voir « Sous-graphes pour plus d’informations »).

## Héritage

Au fur et à mesure que les images et les valeurs sont transmises des nœuds aux autres, certains *attributs* de ces images, c&#39;est-à-dire leurs <b>paramètres de base</b>, sont également *propagés* sur le graphe, tels que la résolution, la précision (c&#39;est-à-dire la profondeur de bit), la répétition et la vitesse aléatoire.

Cette propagation est définie par les [méthodes d&#39;héritage](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que chaque nœud applique pour ces attributs. En effet, les nœuds peuvent *hériter des attributs* d&#39;autres nœuds ou du graphe dans lequel ils se trouvent.\
Les méthodes d&#39;héritage peuvent être les suivantes :

* *Relatif au parent*
* *Relative à l&#39;entrée*
* *Absolu* : aucun héritage

L&#39;Héritage peut être abstrait et difficile à gérer, c&#39;est pourquoi nous vous recommandons vivement de consulter la [page dédiée](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) pour en discuter en détail.

## Exposition des paramètres

Exposer des paramètres est un concept qui peut aller très loin, mais il peut se résumer à la sélection de certaines propriétés des nœuds dans votre graphe et à la création d&#39;un élément de contrôle d&#39;interface utilisateur dédié pour eux, qui est facilement disponible une fois que le graphe est utilisé comme sous-graphe ou s&#39;il est publié comme archive. Étant donné que vous ne pouvez plus sélectionner rapidement ou facilement des nœuds et modifier leurs propriétés, l’objectif est de créer un autre panneau de configuration principal qui regroupe toutes les propriétés pertinentes pour ce graphe spécifique.

voici quelques informations à connaître sur les Paramètres exposés :

* Les paramètres exposés <b>déplacent un contrôle du nœud vers le graphe</b>, essentiellement vers le haut d&#39;un niveau de la hiérarchie.
* Les paramètres exposés ne peuvent donc plus être modifiés sur le nœud, seulement sur le graphe.
* Les paramètres exposés peuvent être entièrement personnalisés avec des noms, des étiquettes, des valeurs, le type d&#39;éditeur d&#39;interface utilisateur et même être masqués et affichés pour certaines conditions.

Exposer des paramètres est un concept abstrait et difficile pour les débutants[il existe davantage de documentation dédiée à ce sujet](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), mais il est recommandé de se familiariser entièrement avec d&#39;autres aspects de base du logiciel avant de se plonger dans l&#39;Expose de paramètres.
