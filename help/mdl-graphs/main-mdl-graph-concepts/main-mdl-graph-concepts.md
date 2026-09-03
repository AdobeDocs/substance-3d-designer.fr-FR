---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/main-mdl-graph-concepts.html"
breadcrumb-title: ''
description: Découvrez les principaux concepts des graphiques de langage de définition de matériau dans Substance 3D Designer pour la création de matériaux.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Main MDL graph concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Concepts principaux du graphique MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---


# Concepts principaux du graphique MDL

Cette page présente les concepts principaux qui sont *spécifiques* aux [graphiques MDL](../../mdl-graphs/mdl-graphs.md) et qui doivent être bien compris pour tirer le meilleur parti de ce type de graphique dans Substance 3D Designer.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Iray

Les matériaux MDL utilisent une description destinée aux solutions de rendu physiques. , prise en charge par le rendu [Iray](../../interface/3d-view/iray/iray.md) intégré à Designer. Par conséquent, l&#39;affichage du résultat d&#39;un graphique MDL *nécessite la sélection du rendu Iray* dans un panneau [Vue 3D](../../interface/3d-view/3d-view.md) actif.

</td>
<td style="border: 0;" valign="top">

[![Logo NVIDIA Iray](main-mdl-graph-concepts.resources/main-mdl-graph-concepts-01.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>
</table>

Lors de la création ou du chargement d&#39;un graphique MDL, le premier panneau d&#39;affichage 3D [déverrouillé](../../interface/customizing-your-wor/customizing-your-workspace.md) trouvé par Designer *bascule automatiquement* vers le rendu [Iray](../../interface/3d-view/iray/iray.md). Si aucune vue 3D n’est disponible, un *nouveau* panneau de vue 3D sera créé et basculé vers le rendu Iray pour héberger le rendu de la matière MDL en cours de modification.

Lorsque le rendu Iray est sélectionné dans un panneau d’affichage 3D, le menu Matières de ce panneau vous permet de basculer entre les matières MDL disponibles, qui incluent les matières chargées dans le panneau Explorateur et les matières de la bibliothèque MDL de Designer. Pour en savoir plus sur l&#39;utilisation des matériaux MDL dans Iray, consultez la section [Iray](../../interface/3d-view/iray/iray.md) de cette documentation.

## Nœud racine

Le résultat d&#39;un graphique MDL est défini par le nœud <b>racine</b>. N&#39;importe quel nœud du graphique peut être défini comme racine à condition qu&#39;il génère des données de type <b>matériau</b>, c&#39;est-à-dire une *définition de matériau*. Un graphique MDL peut avoir *un seul* nœud racine.

En général, un nœud qui peut être défini comme Root peut être *autonome*, car il contient déjà une définition de matériau qui peut être personnalisée en transmettant des données à ses *entrées*.\
Par exemple, si vous souhaitez travailler sur un matériau de type verre, vous pouvez utiliser une définition de matériau verre comme nœud racine comme point de départ, mais cela n&#39;est *pas obligatoire*. De nombreux nœuds de matériau sont modélisés et peuvent être transformés en n&#39;importe quel matériau complexe à l&#39;aide de la longue liste de nœuds MDL.

Le nœud racine comprend une vignette affichant un aperçu de sa sortie actuelle.

![Nœud racine du graphique MDL](main-mdl-graph-concepts.resources/main-mdl-graph-concepts-02.png "Nœud racine du graphique MDL")

*Nœud racine dans un graphique MDL et ses propriétés affichées dans le [panneau Propriétés](../../interface/properties/properties.md)* *4}*

## Connecteurs et types

Les types de données étant beaucoup plus nombreux dans les graphiques MDL que dans les autres graphiques de Designer, il se peut que vous assistiez à des apparitions uniques de connecteurs de nœuds. Les concepts importants à comprendre sont énumérés ci-dessous.

Forme du connecteur

La *forme du connecteur* indique si le type de données est *uniforme* (cercle) ou *variable* (carré).

« Une variable de type uniforme ne peut être définie que sur une valeur uniforme. Une variable de type variable peut être définie sur une valeur variable ainsi que sur une valeur uniforme. La valeur résultante dans la variable est alors toujours considérée comme variable. » (Source : section 6.3 de la [spécification MDL](https://raytracing-docs.nvidia.com/mdl/specification/MDL_spec_1.7.2_17Jan2022.pdf))

En voici quelques exemples :

* un échantillon de <b>texture</b> est *variable*, car les valeurs sont affectées par le pixel échantillonné
* une valeur de <b>couleur</b> est *uniforme*, car elle est transmise de manière égale quel que soit le contexte
* a <b>BRDF</b> est *variable*, car les valeurs sont affectées par l&#39;angle d&#39;incidence
* une valeur <b>float</b> ou <b>booléenne</b> est *uniforme* car elle est transmise de manière égale quel que soit le contexte

Couleur du connecteur

Le *type de données* provenant d&#39;un connecteur de sortie ou attendu par un connecteur d&#39;entrée est codé par couleur et affiché entre parenthèses après l&#39;identificateur/le libellé lors du survol du connecteur avec la souris.

>[!WARNING]
>
> Seuls les connecteurs de *types de données correspondants* peuvent être liés entre eux. Le seul objectif du codage couleur est d’améliorer la lisibilité en ce qui concerne le type de données transmises dans le graphique et les connecteurs pouvant être liés entre eux.

![Types de connecteurs de nœuds MDL](main-mdl-graph-concepts.resources/main-mdl-graph-concepts-03.png "Types de connecteurs de nœuds MDL"){width="512px"}

*L&#39;aspect des connecteurs varie en fonction du type de valeur d&#39;E/S, qui s&#39;affiche entre parenthèses après l&#39;identificateur d&#39;E/S*

## Création de nœuds filtrée

Vous pouvez ajouter tout nœud disponible dans la catégorie <b>mdl</b> de la <b>bibliothèque</b> dans le graphique en *faisant glisser le nœud* de la <b>vue Bibliothèque</b> vers la <b>vue Graphique</b> ou en appuyant sur la <b>barre d&#39;espace</b> pour ouvrir le <b>menu Nœud</b> dans la vue Graphique lorsque *rien n&#39;est sélectionné*. Dans ce cas, une liste de nœuds *non filtrés* s&#39;affiche.

Cependant, il existe des cas où la liste des nœuds dans le menu Nœud est filtrée pour afficher uniquement les nœuds du type de données correspondant pour l’entrée ou la sortie cible :

* si un *nœud est sélectionné* dans la vue Graphique et si la <b>barre d&#39;espace</b> est enfoncée
* si vous cliquez sur <b>LMB</b>, maintenez et *faites glisser* un lien hors d&#39;un *connecteur de nœud*

Vous pouvez garder à l&#39;esprit les *règles* appliquées pour le filtrage :

* si le menu Nœud s&#39;affiche en appuyant sur <b>barre d&#39;espace</b> lorsqu&#39;un *nœud unique* est sélectionné, la liste inclut les nœuds dont le type de données de la *première entrée* correspond au type de données *sortie* du nœud sélectionné
* si le menu Nœud s&#39;affiche en appuyant sur la <b>barre d&#39;espace</b> lorsque *plusieurs* nœuds sont sélectionnés, la liste inclut les nœuds dont le type de données de la *première entrée* correspond au type de données de la *dernière sortie* nœud sélectionné&#x200B;**
* si le menu Nœud s&#39;affiche en *faisant glisser un lien* hors d&#39;un connecteur *output*, la liste inclut les nœuds pour lesquels le type de données *première entrée* correspond au type de données *output* sélectionné
* si le menu Nœud s&#39;affiche en *faisant glisser un lien* depuis un connecteur *d&#39;entrée*, la liste inclut les nœuds dont le type de données *output* correspond au type de données *input* sélectionné

![Création de nœud filtrée](main-mdl-graph-concepts.resources/main-mdl-graph-concepts-04.gif "Création de nœud filtrée")

*Création de nœuds filtrée dans Graphe MDL, notez que la liste change en fonction du type de valeur pour le connecteur*

## Entrées et textures du graphe

Les matériaux MDL peuvent recevoir des données de sources externes, sous la forme de valeurs et de textures par exemple. Pour ce faire, <b>exposez un nœud</b>, contrairement au [graphe de Substance](../../compositing-graphs/substance-compositing-graphs.md) où des noeuds d&#39;entrée dédiés existent à cet effet.

Les données peuvent être transmises au nœud exposé selon son *type*. Par exemple, des valeurs de Flottant peuvent être transmises à un nœud <b>flottant</b> exposé et une texture peut être transmise à un nœud <b>couleur</b> exposé (dans ce cas, les valeurs RVBA du pixel échantillonné sont transmises en tant que valeur de couleur).

![Entrées de graphe Exposées](main-mdl-graph-concepts.resources/main-mdl-graph-concepts-05.png "Entrées de graphe Exposées")

*Les nœuds Exposés créent des entrées de graphe qui sont à la fois des entrées de valeur brute et des échantillonneurs pour les textures*
