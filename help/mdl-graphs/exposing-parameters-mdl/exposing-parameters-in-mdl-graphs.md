---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exposing-parameters-in-mdl-graphs.html"
breadcrumb-title: ''
description: Apprenez à exposer les paramètres dans des graphiques MDL pour rendre les matériaux personnalisables et réutilisables dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exposing parameters in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exposition de paramètres dans les graphiques MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# Exposition de paramètres dans les graphiques MDL

Cette page explique le processus d&#39;exposition des paramètres dans les graphiques MDL afin qu&#39;ils puissent être connectés aux valeurs et aux textures fournies par *d&#39;autres nœuds* du graphique ou par *des sources externes*.

![État exposé des entrées de nœud](../../assets/mdl-node-inputs-hl.png "État exposé des entrées de nœud")

*État exposé des entrées de nœud*

## Exposition des entrées de nœud

Dans la plupart des cas, les *connecteurs d&#39;entrée* des propriétés d&#39;un nœud peuvent être affichés afin que leur *valeur soit définie par d&#39;autres nœuds* dans le graphique. Il s&#39;agit d&#39;une partie *critique* de tout workflow dans les graphiques MDL et elle doit être bien comprise.

Lorsqu&#39;un nœud est sélectionné dans la <b>vue Graphique</b>, ses propriétés sont affichées dans le panneau <b>Propriétés</b>. La plupart des propriétés sont répertoriées avec un ensemble de boutons situés à droite de leur libellé :

* **![](../../assets/mdl-expose-new-node.png)Copier la valeur vers un nouveau nœud et la lier à ce paramètre** : crée un *connecteur d&#39;entrée* pour cette propriété et la connecte à un *nouveau nœud* qui génère la valeur actuelle de cette propriété
* **![](../../assets/mdl-expose-new-input.png)Créer une broche d&#39;entrée pour ce paramètre** : crée un *connecteur d&#39;entrée* pour cette propriété
* **![](../../assets/mdl-expose-reset.png)Réinitialisez ce paramètre à sa valeur par défaut** : lorsqu&#39;aucune valeur n&#39;est connectée au connecteur d&#39;entrée de cette propriété, réinitialise sa valeur à sa valeur par défaut

![](../../assets/mdl-expose-input.gif)

*Manipulation des entrées de nœud*

Si vous cliquez sur l&#39;un des deux premiers boutons, un *connecteur d&#39;entrée typé* est ajouté au nœud. Les propriétés du nœud réagissent à l&#39;*état de connexion* de ce connecteur :

* **Non connecté** : le paramètre peut toujours être modifié dans le panneau **Propriétés** et la valeur saisie dans ce panneau est *appliquée*
* **Connecté** : le paramètre ne peut plus être modifié dans le panneau **Propriétés**. La valeur entrée dans ce panneau est *remplacée* par la valeur reçue par le *connecteur d&#39;entrée*. La propriété ne peut pas être réinitialisée à sa valeur par défaut

Le connecteur d&#39;entrée peut être *supprimé* en cliquant à nouveau sur le bouton **Créer une broche d&#39;entrée pour ce paramètre**. À ce stade, la valeur de la propriété revient à la valeur définie dans le panneau **Propriétés**.

![Paramètres de nœud exposés](../../assets/mdl-exposed-float-hl.png "Paramètres de nœud exposés")

*Paramètres de nœud exposés*

## Exposition des entrées de graphique

Dans un graphique MDL, l’exposition d’un paramètre au niveau du graphique (c’est-à-dire qu’il s’affiche comme un paramètre d’entrée de matière MDL) s’effectue en exposant le nœud qui génère la valeur.

Les nœuds qui peuvent être exposés disposent d&#39;une option <b>Exposer</b> dans leur menu contextuel. Dans la plupart des cas, il s’agit de nœuds qui génèrent une valeur ou des données telles que les coordonnées Float, Color ou Texture.

Option ![« Exposer » dans le menu contextuel d&#39;un nœud](../../assets/mdl-expose-float-menu-hl.png "&quot;Option Exposer&quot; dans le menu contextuel d&#39;un nœud")

Option *« Exposer » dans le menu contextuel d&#39;un nœud*

Le paramètre exposé est configuré directement dans le *nœud exposé*, et non dans les propriétés du graphique. Les propriétés des paramètres exposés sont les suivantes :

* <b>Identificateur</b> : nom unique de ce paramètre d&#39;entrée dans le graphique actuel
* <b>Valeur par défaut</b> : valeur par défaut pour ce paramètre. Il peut également être utilisé comme *aperçu* de l&#39;aspect du paramètre d&#39;entrée dans Designer. Les propriétés <b>Nom d&#39;affichage</b>, <b>Dans le groupe</b> et <b>Plages</b> sont utilisées pour un aperçu le plus précis possible
* <b>Plages</b> :
  * *Plage souple* : définit la plage par défaut du widget utilisé pour afficher ce paramètre, par exemple un curseur. Cette propriété n&#39;existe qu&#39;à des fins d&#39;interface et les valeurs au-delà de la plage souple peuvent être saisies manuellement
  * *Plage fixe* : définit la plage des valeurs acceptées pour ce paramètre. Les valeurs inférieures à la plage sont verrouillées sur la valeur minimale, tandis que les valeurs supérieures à la plage sont verrouillées sur la valeur maximale. Les valeurs par défaut et de plage adoucie du paramètre sont *ajustées automatiquement* pour s&#39;adapter à cette plage.
* <b>Description</b> : description du paramètre
* <b>Dans le groupe</b> : groupe de paramètres auquel appartient ce paramètre d&#39;entrée. S’il n’est pas vide, le paramètre s’affiche dans Designer dans le cadre d’une section réductible nommée d’après le groupe
* <b>Nom d&#39;affichage</b> : nom du paramètre affiché dans l&#39;interface
* <b>Masqué</b> : lorsque ce paramètre est défini sur True, il n&#39;est pas visible dans les entrées de graphique et les propriétés de matière MDL
* <b>Type de gamma</b> : gamma qui doit être utilisé lors de l&#39;échantillonnage des valeurs d&#39;une texture connectée à ce paramètre
* <b>Visible par défaut</b> : définit la visibilité de ce paramètre dans les intégrations MDL dans les cas où certains paramètres peuvent être masqués
* <b>Modificateur de type</b> : définit si la valeur est uniforme ou variable. Lorsqu’il est défini sur auto, le paramètre hérite de cette propriété à partir de son entrée (par exemple, pour une valeur Float : uniforme lorsqu’il est connecté à un objet Float, variable lorsqu’il est connecté à une texture)
* <b>Utilisation de Sampler</b> : identifiant de l&#39;utilisation du paramètre, qui est utilisé pour *connecter la texture appropriée* s lorsque plusieurs sorties sont connectées à un matériau MDL à la fois. Par exemple, lors de la connexion d&#39;un [graphique en Substances](../../compositing-graphs/substance-compositing-graphs.md) à un matériau MDL dans la vue 3D, les textures sont connectées aux entrées correctes en fonction de leurs identifiants d&#39;utilisation.

>[!WARNING]
>
> Bien que les entrées de graphique soient configurées au niveau *nœud*, leur ordre est géré au niveau *graphique* dans la section **Entrée de graphique** des [propriétés de graphique](../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md).

![Exposition des nœuds dans les entrées de graphique](../../assets/mdl-expose-parameter.gif "Exposition des nœuds dans les entrées de graphique")

*Exposition des nœuds dans les entrées de graphique*
