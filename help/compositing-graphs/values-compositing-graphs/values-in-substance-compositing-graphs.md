---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/values-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Découvrez les types de valeur et le traitement des données dans les graphes de composition de Substances pour une création de matériau efficace.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Values in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Valeurs dans les graphes Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 2%

---


# Valeurs dans les graphes Substance

Depuis l&#39;introduction du Moteur [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) v7 dans la version 2019.1.0, il est désormais possible de traiter les valeurs dans le graphe de Substance de données, et[pas seulement dans les fonctions](../../function-graphs/function-graphs.md). Les données de valeur sont les mêmes que celles utilisées dans les fonctions (Entiers, Flottants et booléens, entre autres), ce qui les différencie nettement des données de couleur ou d’Image en niveaux de gris, qui représentent les valeurs de pixels pour une image entière. Plus précisément, lorsque vous mentionnez des données de valeurs, cela signifie *Entier 1, Entier 2, Entier 3 et Entier 4, Flottant 1, Flottant 2, Flottant 3 et Flottant 4 et Booléen*. Chacun possède un codage couleur distinct et n’est généralement pas interverti.

Il existe quelques cas d’utilisation pour cela, tels que :

* Renvoi et traitement de données autres que des images, telles que des propriétés de matériau à valeur unique ou des métadonnées supplémentaires. Par exemple, la valeur IOR d&#39;un matériau.
* Optimisation des calculs de graphe qui n&#39;ont pas besoin d&#39;être calculés par pixel (une alternative au [Processeur de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)). Par exemple, une couleur unie aléatoire.
* Lier les propriétés d&#39;un nœud à un autre en traitant les données d&#39;image en valeurs. Par exemple, les valeurs Minimum et Maximum d’une image pour ajuster les Niveaux avec.

## Nouveaux nœuds et entrées de valeur

Deux nouveaux Noeuds atomiques fonctionnent avec des valeurs :

|  |  |
| --- | --- |
| <div><img alt="icône de nœud de processeur de valeurs" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../assets/valueprocessor.png" title="icône de nœud de processeur de valeurs" width="100px"/></div>  <b>[Processeur de valeurs](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)</b> | Le [Processeur de valeurs](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) prend un nombre quelconque d&#39;entrées Niveaux de gris ou Couleur et vous permet de renvoyer une seule valeur à partir de calculs basés sur ces entrées. |
| <div><img alt="Icône Noeud d&#39;entrée de valeur" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../assets/inputnumeric.png" title="Icône Noeud d&#39;entrée de valeur" width="100px"/></div>  **[Entrée de valeur](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)** | L&#39;[Entrée de valeur](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)vous permet de créer un emplacement d&#39;entrée sur les sous-graphes qui est explicitement défini comme Valeur. |

En outre, d&#39;autres nœuds les traitent d&#39;une manière spécifique :

Le [nœud de sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) s&#39;ajuste automatiquement pour devenir une sortie Value si vous y connectez une connexion Value, comme auparavant avec les niveaux de gris et la couleur.

![Nœud de la valeur de sortie](../../assets/values-output.gif "Nœud de la valeur de sortie"){width="512px"}

Chaque nœud ([Atomic](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) et [Library](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)/Instance) comporte un nouvel onglet qui vous permet de définir des entrées de valeur.

![Ajout de valeurs d&#39;entrée sur le nœud](../../assets/values-inputs.gif "Ajout de valeurs d&#39;entrée sur le nœud")

## Utilisation des valeurs

L’utilisation de valeurs est légèrement différente du travail normal sur un graphique à Substances :

Les connexions de valeur peuvent uniquement être effectuées à partir d&#39;un [processeur de valeur](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), d&#39;une [entrée de valeur](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) ou d&#39;un [sous-graphique](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md). Cela signifie en fait qu&#39;un processeur de valeurs est la seule façon de créer une connexion Value à partir de zéro, il n&#39;y a pas de nœud « Valeur statique » ou quelque chose de similaire. Créez plutôt un processeur de valeurs, placez une valeur statique et définissez-la comme sortie pour obtenir le même résultat.

Le processeur de valeurs ne peut renvoyer qu&#39;une seule valeur. Si vous souhaitez renvoyer plusieurs valeurs, ensembles ou groupes de valeurs, vous devez créer un [sous-graphique](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).

Pour mettre en surbrillance l’emplacement où les valeurs sont affichées ou utilisées, tout nœud comportant des entrées de valeur ou des sorties de valeur est mis en surbrillance avec une bordure jaune épaisse :

![Utilisation des valeurs](../../assets/yellowhighlight.png "Utilisation des valeurs")
