---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/the-library/managing-custom-content-and-filters.html"
breadcrumb-title: ''
description: Découvrez comment gérer le contenu et les filtres personnalisés dans la bibliothèque Substance 3D Designer pour un accès organisé aux ressources.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Library > Managing custom content and filters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gestion de contenu et de filtres personnalisés
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# Gestion de contenu et de filtres personnalisés

Cette page explique la méthode de création de catégories et de filtres pour gérer le contenu personnalisé dans la bibliothèque. Il contient également des suggestions de workflows basés sur des projets.

## Vue d’ensemble

Après avoir [ajouté du contenu personnalisé à la bibliothèque](../../../interface/preferences-window/project-settings/project-settings.md), vous devez le rendre *détectable*.

La bibliothèque utilise un certain nombre de *points de données* pour identifier le contenu, afin de le filtrage et de le faire apparaître dans les recherches. Ces points de données sont les suivants :

* Nom
* Extension
* URL (c.-à-d. *nom de fichier*)
* Attributs

Vous pouvez organiser votre <b>bibliothèque</b> en catégories contenant des filtres spécifiques et l&#39;adapter aux besoins de votre projet.\
En effet, les catégories et les filtres personnalisés peuvent être *spécifiques à un projet* et être enregistrés dans [fichiers de projet](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbsprj). Ces fichiers peuvent ensuite être assemblés en [fichiers de configuration](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbscfg) et distribués à une équipe afin que les artistes puissent tous utiliser les* mêmes catégories de <b>bibliothèques</b>* pour un projet donné.

Cela signifie qu&#39;avec un ou plusieurs fichiers de projet, vous pouvez définir les dossiers dont le contenu doit être ajouté à la <b>bibliothèque</b>, ainsi que les catégories et les filtres qui trieront et organiseront ce contenu.

![Contenu personnalisé dans la bibliothèque](../../../assets/library-filters.png "Contenu personnalisé dans la bibliothèque")

## Attributs du graphe

Les graphes contenus dans les fichiers [SBS](../../../getting-started/overview/overview.md) et [SBSAR](../../../getting-started/overview/overview.md) peuvent être *filtrés et recherchés* dans la bibliothèque à l&#39;aide de l&#39;ensemble de données de la section [Attributs](../../../compositing-graphs/graph-parameters/graph-parameters.md) des propriétés du graphe. Certains de ces attributs peuvent également être définis sur d&#39;autres [types de ressources](../../../resources/resources.md).

## Filtres et dossiers personnalisés

Les filtres sont de simples paramètres de recherche booléens (Vrai/Faux) qui entraînent l&#39;affichage d&#39;une ressource dans la bibliothèque lorsque ce <b>Filtre</b> est sélectionné. Les ressources peuvent être tout ce qui est conservé à l&#39;intérieur d&#39;un paquet. Gardez les points suivants à l’esprit :

* Un <b>filtre</b> correspondra à toutes les ressources, sous *tous les chemins suivis*.
* Un <b>filtre</b> peut contenir plusieurs conditions, *toutes doivent avoir la valeur True* (condition AND) pour que la ressource s&#39;affiche sous ce filtre.
* Une [ressource](../../../resources/resources.md) peut apparaître sous plusieurs filtres, elle n&#39;est *pas exclusive* à un filtre.
* Une [ressource](../../../resources/resources.md) d&#39;un chemin surveillé est *toujours disponible* dans la <b>bibliothèque</b>, même si elle n&#39;est *pas* sous un <b>filtre</b>, à l&#39;aide de la fonction <b>Rechercher</b>.

### Création de filtres et de dossiers

Les catégories (c’est-à-dire les dossiers) et les filtres sont créés et modifiés à l’aide des boutons suivants :

<b>![](../../../assets/library-icon-new-folder.png) Ajouter un dossier :</b> Crée un dossier extensible dans la vue Bibliothèque. Vous *ne pouvez pas* créer de sous-dossiers.

<b>![](../../../assets/library-icon-new-filter.png) Ajouter un filtre :</b> ajoute un nouveau filtre dans le dossier sélectionné. Vous *ne pouvez pas* ajouter de filtres aux dossiers par défaut existants.

<b>![](../../../assets/library-icon-edit.png) Modifier l&#39;élément :</b> Modifie le dossier ou le filtre actuellement sélectionné. Vous *ne pouvez pas* modifier les propriétés des dossiers et filtres par défaut.

Pour *supprimer* un dossier ou un filtre, *cliquez avec le bouton droit* dessus et sélectionnez l&#39;option <b>Supprimer</b> dans le menu contextuel.

### Modification des filtres et des dossiers

Les <b>dossiers</b> et les <b>filtres</b> sont identifiés par les données suivantes :

* <b>Nom</b> affiché dans l&#39;arborescence de la bibliothèque.
* [Fichier de configuration du projet (SBSPRJ)](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) dans lequel cet élément est stocké.

>[!WARNING]
>
> Il est *très* important de les configurer correctement, pour vous assurer de modifier le *projet correct* !

![Édition de filtre personnalisée](../../../assets/library-filters-edit.png "Édition de filtre personnalisée")

Les **filtres** doivent généralement avoir *conditions* configurées pour atteindre leur objectif de filtrage. Ces conditions sont configurées en utilisant les critères suivants :

* **Type de ressource** : définit un [type de ressource](../../../resources/resources.md) spécifique, tel que [Graphes](../../../compositing-graphs/substance-compositing-graphs.md)
* **Attribut** auquel appliquer la condition : voir la liste ci-dessus
* **Logique de condition** : permet au filtre d&#39;inclure des résultats avec des correspondances positives, négatives, partielles et entières
* **Mot-clé de condition :** la chaîne par rapport à laquelle les critères **Attribut** et **Logique de condition** sont testés. Si cette option est vide, toute ressource correspondant à ces deux critères est incluse

Vous pouvez *ajouter ou supprimer* des conditions à l&#39;aide des boutons &#39;**+**&#39; et &#39;**x**&#39; situés à l&#39;extrême droite du mot-clé Condition.

>[!NOTE]
>
> Un filtre sans condition configurée entraîne l&#39;affichage du contenu de *la* **bibliothèque**.

## Bonnes pratiques

### Recommandations

* La règle générale pour la bibliothèque par défaut est que le <b>dossier</b> est répertorié dans l&#39;attribut <b>Catégorie</b>, tandis que le nom du <b>filtre</b> est déterminé par l&#39;attribut <b>Balise</b>
* Ne créez pas de nœuds personnalisés qui se mélangent à la bibliothèque par défaut, sauf si vous *le souhaitez explicitement*. Vos nœuds *apparaîtront* sous les filtres par défaut s&#39;ils correspondent. Vous devrez donc vous assurer d&#39;utiliser un *système de balisage/dénomination différent* pour éviter cela
* Utilisez des identifiants *uniques*, *par projet*. Ils peuvent être placés où vous le souhaitez (comme <b>Description</b>, <b>Catégorie</b> ou <b>Données utilisateur</b>), à condition d&#39;*être cohérents* entre tous les projets. Cela facilite considérablement la recherche et le filtrage de contenu *par projet*
* Utilisez l&#39;attribut <b>Auteur</b> pour suivre la personne initialement responsable du contenu, sans avoir à parcourir les enregistrements de Gestion de versions
* Un moyen efficace de créer des <b>icônes</b> consiste à utiliser l&#39;option <b>Générer</b> de l&#39;attribut de graphe [Icône](../../../compositing-graphs/graph-parameters/graph-parameters.md) ou à créer un [modèle](../../../interface/preferences-window/project-settings/project-settings.md) de graphe pour les générer. De cette façon, vous pouvez assurer la cohérence et économiser le travail de création. Toutes les icônes de bibliothèque par défaut ont été créées dans Designer de cette façon !

### Gestion de contenu de portée variable

* Vous pouvez ajouter des ressources à *catégories existantes* si cela est plus logique. La gestion et la maintenance des filtres s&#39;en trouveront facilitées et vous pouvez utiliser un style d&#39;icône spécial pour *les différencier*.
* Vous pouvez définir vos dossiers et filtres dans un [fichier de configuration de projet](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) *global* (au niveau du studio), puis y ajouter du contenu en ajoutant simplement des chemins d&#39;accès contrôlés à partir de *fichiers de projet[* consécutifs](../../../interface/preferences-window/project-settings/project-settings.md)
* Vous pouvez définir des dossiers et des filtres spécifiques pour *chaque projet* afin de les séparer
* Vous pouvez combiner et faire correspondre et utiliser les méthodes des trois méthodes ci-dessus : utiliser les filtres existants, définir de nouveaux filtres globaux et en créer des uniques par projet
