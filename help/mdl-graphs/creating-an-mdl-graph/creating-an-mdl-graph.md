---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: Apprenez à créer des graphes Matériau Definition Language dans Substance 3D Designer pour créer des matériaux personnalisés.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Création d’un Graphe MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Création d’un Graphe MDL

Cette page décrit le processus de création d’un Graphe MDL de création de Matériaux MDL dans Substance 3D Designer.

![Chemins de création de Graphe MDL](../../assets/mdl-new-graph-hl.png "Chemins de création de Graphe MDL")

*Méthodes de création d’un nouveau Graphe MDL dans l’interface de Designer*

## Méthodes de création d’un Graphe MDL

Vous pouvez créer un Graphe MDL à l’aide de l’une des méthodes suivantes :

* Sélectionnez l&#39;option **Fichier > Nouveau > Graphe MDL** dans la *barre de menus principale*
* Cliquez sur le bouton ![](../../assets/mdl-new-graph-icon.png) **Ajouter un Graphe MDL** dans la *barre d&#39;outils principale*
* Cliquez avec le bouton droit sur un *pack existant* dans le panneau **Explorateur**, puis sélectionnez l&#39;option **Nouveau > Graphe MDL**

La boîte de dialogue **Nouveau Graphe MDL** s&#39;affiche, voir ci-dessous.

![Boîte de dialogue Nouveau Graphe MDL](../../assets/mdl-templates.png "Boîte de dialogue Nouveau Graphe MDL")

*Boîte de dialogue Nouveau Graphe MDL*

## Boîte de dialogue Nouveau Graphe MDL

Quelle que soit la méthode utilisée pour créer un nouveau Graphe MDL, la boîte de dialogue <b>Nouveau Graphe MDL</b> s&#39;affiche toujours, vous permettant de configurer le nouveau graphe.

### Modèles

La section <b> modèles</b> vous permet de sélectionner un modèle de graphe, qui inclut des nœuds préconfigurés pour vous permettre de démarrer plus rapidement votre graphe. Les nœuds préconfigurés comprennent des nœuds de sortie, des nœuds simples pour transmettre des valeurs à ces sorties - par exemple, la Couleur uniforme et les Noeuds d&#39;entrée selon le modèle.

Pour partir d&#39;un graphe entièrement *vide*, sélectionnez le modèle <b>vide</b>.

L&#39;option <b>Projet</b> vous permet de filtrer la liste des modèles par fichier de projet. Cela facilite la recherche des modèles personnalisés dans les emplacements ajoutés sous la section <b>Général</b> des paramètres du projet pour le fichier de projet.

>[!WARNING]
>
> Si vous sélectionnez le mauvais modèle, vous *ne pouvez pas* passer à un autre modèle après avoir créé le graphe.\
> Pour transférer votre graphe existant vers un autre modèle, vous pouvez créer un nouveau graphe à l’aide du modèle approprié, puis copier-coller votre graphe vers le nouveau modèle. Reconnectez les nœuds selon les besoins, y compris le nœud [racine](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md).

La liste des modèles peut être affichée dans différents modes à l&#39;aide des *boutons* en regard de la zone de liste déroulante **Projet** :

* **![](../../assets/mdl-template-recent-icon.png)Afficher les modèles récemment utilisés** : filtre la liste pour afficher les derniers modèles utilisés dans l&#39;ordre *du plus récent au moins récent*, l&#39;élément supérieur étant le plus récent
* **![](../../assets/mdl-template-graphs-icon.png)graphes d&#39;affichage** : les modèles sont affichés par leur *étiquette uniquement*, dans l&#39;ordre des fichiers [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) dans le répertoire des modèles
* **![](../../assets/mdl-template-packages-icon.png)Afficher les fichiers Substance 3D** : les modèles sont affichés selon leur étiquette en tant que *enfants du fichier Substance 3D auquel ils appartiennent*, dans l&#39;ordre des fichiers dans le répertoire des modèles
* **![](../../assets/mdl-template-directory-icon.png)Répertoires d&#39;affichage** : les modèles sont affichés par leur étiquette en tant que *enfants du répertoire auquel ils appartiennent*, dans l&#39;ordre des fichiers dans le répertoire des modèles

### Propriétés

La section <b>Propriétés du Graphe </b> vous permet de configurer des informations de base concernant le nouveau graphe. Vous pouvez toujours les modifier par la suite, mais il est judicieux de faire attention d’abord et de les configurer de manière appropriée pour votre cas d’utilisation.

* <b>Nom du Graphe</b> : identifiant du graphe. Il doit être unique pour un package donné et ne peut pas inclure d’espaces ni de caractères spéciaux.
* <b>Créer un graphe dans le pack</b> : vous pouvez utiliser cette zone de liste déroulante pour créer un *nouveau* pack pour le nouveau graphe ou ajouter le nouveau graphe à un *pack* existant déjà chargé dans le panneau Explorateur.\
  Remarque : si le processus de création est démarré à l&#39;aide de la méthode <b>4</b> (voir ci-dessus), ce paramètre est *prédéfini* par rapport au package existant à partir duquel le processus a été démarré.
* <b>Détails du modèle</b> : cette section fournit un court texte expliquant les caractéristiques et l’objectif du modèle
