---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: Découvrez les concepts clés des graphiques de composition de Substances de données, notamment les nœuds, les connexions et les principes de base du workflow.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Concepts clés du graphe Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---


# Concepts clés du graphe Substance

Cette page répertorie les concepts importants à comprendre lors de l’utilisation de graphiques de Substances dans Substance 3D Designer.

## Sous-graphes/publication

[La publication d&#39;un graphique](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) ou la création d&#39;un sous-graphique sont deux concepts abstraits très similaires. Cela signifie que tout graphique ou réseau de nœuds peut être « assemblé » et transformé en une ressource réutilisable et autonome. La création de [sous-graphes](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) s&#39;effectue principalement au sein de l&#39;application afin de rendre certains contenus réutilisables dans un workflow efficace et intelligent, car cela évite de dupliquer un ensemble de nœuds à l&#39;infini. La publication implique une étape supplémentaire pour exporter au format [Substance 3D asset (SBSAR)](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html), ce qui rend votre graphique de réseau de nœuds utilisable en dehors de l’application, par exemple lorsque vous créez un matériau pour Unreal Engine.

Les entrées, les sorties et les paramètres exposés sont extrêmement importants pour ce concept, car ils sont les seuls moyens d’interagir avec le graphique une fois qu’il est utilisé comme sous-graphique ou comme ressource Substance 3D publiée. Les raisons sont les suivantes :

* Aucune sortie signifie que votre graphique <b>ne génère rien</b>, aucune donnée du tout.
* Aucun paramètre exposé signifie que votre graphique <b>ne peut pas être personnalisé</b> de quelque manière que ce soit. Vous ne pouvez pas définir des éléments tels que l’intensité d’un effet, l’opacité d’une image fusionnée, la couleur d’une zone spécifique, etc.
* L&#39;absence d&#39;entrée signifie que, dans certains cas, vous ne pourrez pas personnaliser le résultat d&#39;un graphique avec<b> vos propres données d&#39;image</b>, telles que des cartes de maillage bakées pour générer des effets, une image d&#39;entrée pour appliquer un flou ou un masque personnalisé pour isoler certaines zones d&#39;une image.

## Entrées et sorties

Une [sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)est un nœud qui génère un seul résultat 2D. Il s’agit d’une extrémité, d’une terminaison pour votre graphique, d’un résultat final. Seules les données connectées à une sortie peuvent être exportées en dehors de Designer, voire utilisées dans d’autres graphiques.

Voici quelques informations à connaître sur les sorties :

* Vous pouvez avoir autant de sorties que vous le souhaitez, mais vous devez en avoir <b>au moins une</b>.
* Une sortie peut être de <b>n&#39;importe quelle résolution</b> jusqu&#39;à 8 192 px de large ou de haut, elle peut être de<b> couleur ou en niveaux de gris</b> et peut être exportée vers n&#39;importe quel type de fichier pris en charge.
* Les sorties peuvent et doivent être <b>nommées de manière unique</b> pour les identifier, ce qui est utile lors de l&#39;exportation.
* Chaque connecteur sur le côté droit d’un nœud est en fait une sortie (voir « Sous-graphiques pour plus d’informations »)

Une [entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) est similaire à une sortie. Il s&#39;agit d&#39;un emplacement vide et ouvert auquel vous ou un autre utilisateur pouvez connecter vos propres données. Il permet de créer un graphique qui utilise des données d’image externes définies par l’utilisateur, telles qu’un filtre qui modifie une image d’entrée (un flou ou un réglage Contraste par exemple).

Voici quelques informations à connaître sur les entrées :

* Les entrées sont entièrement <b>facultatives</b>. Vous ne devez les ajouter qu&#39;en cas de besoin. Il n&#39;y a pas de montant minimum ou maximum.
* Les entrées ont une résolution définie (généralement liée au graphique) que vous définissez, ainsi que s’il s’agit de niveaux de gris ou de couleurs. Tout ce qui y est connecté sera converti pour correspondre à ceci.
* Les entrées peuvent être des fichiers bitmap de votre disque dur, d’autres graphiques, des calques de Painter ou Alchemist, etc.
* Chaque connecteur sur le côté gauche d’un nœud est une entrée (voir « Sous-graphiques pour plus d’informations »).

## Transmission

Au fur et à mesure que les images et les valeurs sont transmises des nœuds aux autres, certains *attributs* de ces images, c&#39;est-à-dire leurs <b>paramètres de base</b>, sont également *propagés* sur le graphique, tels que la résolution, la précision (c&#39;est-à-dire la profondeur de bit), la mosaïque et la vitesse aléatoire.

Cette propagation est définie par les [méthodes d&#39;héritage](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que chaque nœud applique pour ces attributs. En effet, les nœuds peuvent *hériter des attributs* d&#39;autres nœuds ou du graphique dans lequel ils se trouvent.\
Les méthodes d’héritage peuvent être :

* *Relative au parent*
* *Relative à l&#39;entrée*
* *Absolu* : aucun héritage

L&#39;héritage peut être abstrait et difficile à gérer. Nous vous recommandons donc vivement de consulter la [page dédiée](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) pour en discuter en détail.

## Exposition des paramètres

L&#39;exposition des paramètres est un concept qui peut aller très loin, mais qui peut se résumer à la sélection de certaines propriétés des nœuds dans votre graphique et à la création d&#39;un élément de contrôle d&#39;interface utilisateur dédié, qui est facilement disponible une fois le graphique utilisé comme sous-graphique ou s&#39;il est publié en tant qu&#39;archive. Étant donné que vous ne pouvez plus sélectionner rapidement ou facilement des nœuds et modifier leurs propriétés, l’objectif est de créer un autre panneau de configuration principal regroupant toutes les propriétés pertinentes pour ce graphique spécifique.

Voici quelques informations à connaître sur les paramètres exposés :

* Les paramètres exposés <b>déplacent un contrôle du nœud vers le graphique</b>, essentiellement vers le haut d&#39;un niveau de la hiérarchie.
* Les paramètres exposés ne peuvent donc plus être modifiés sur le nœud, seulement sur le graphique.
* Les paramètres exposés peuvent être entièrement personnalisés avec des noms, des étiquettes, des valeurs, le type d&#39;éditeur d&#39;interface utilisateur et peuvent même être masqués et affichés pour certaines conditions.

L&#39;exposition des paramètres est un concept abstrait et difficile pour les débutants[il existe davantage de documentation dédiée à ce sujet](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), mais il est recommandé de se familiariser entièrement avec d&#39;autres aspects de base du logiciel avant de se plonger dans l&#39;exposition des paramètres.
