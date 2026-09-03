---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: Apprenez à créer des graphiques de langage de définition de matériau dans Substance 3D Designer pour créer des matériaux personnalisés.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Création d’un graphique MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Création d’un graphique MDL

Cette page décrit le processus de création d’un graphique MDL pour créer des matériaux MDL dans Substance 3D Designer.

![Chemins de création de graphiques MDL](creating-an-mdl-graph.resources/creating-an-mdl-graph-01.png "Chemins de création de graphiques MDL")

*Méthodes de création d’un graphique MDL dans l’interface de Designer*

## Méthodes de création d’un graphique MDL

Vous pouvez créer un graphique MDL à l’aide de l’une des méthodes suivantes :

* Sélectionnez l&#39;option **Fichier > Nouveau > graphique MDL** dans la *barre de menus principale*
* Cliquez sur le bouton ![](creating-an-mdl-graph.resources/creating-an-mdl-graph-02.png) **Ajouter un graphique MDL** dans la *barre d&#39;outils principale*
* Cliquez avec le bouton droit de la souris sur un *pack existant* dans le panneau **Explorateur**, puis sélectionnez l&#39;option **Nouveau > graphique MDL**

La boîte de dialogue **Nouveau graphique MDL** s&#39;affiche, voir ci-dessous.

![Boîte de dialogue Nouveau graphique MDL](creating-an-mdl-graph.resources/creating-an-mdl-graph-03.png "Boîte de dialogue Nouveau graphique MDL")

*Boîte de dialogue Nouveau graphique MDL*

## Boîte de dialogue Nouveau graphique MDL

Quelle que soit la méthode utilisée pour créer un graphique MDL, la boîte de dialogue <b>Nouveau graphique MDL</b> s&#39;affiche toujours, vous permettant de configurer le nouveau graphique.

### Modèles

La section <b> modèles</b> vous permet de sélectionner un modèle de graphique, qui inclut des nœuds préconfigurés pour vous permettre de démarrer plus rapidement avec votre graphique. Les nœuds préconfigurés comprennent des nœuds de sortie, des nœuds simples pour transmettre des valeurs à ces sorties - par exemple, Couleur uniforme, et des nœuds d’entrée selon le modèle.

Pour partir d&#39;un graphique entièrement *vierge*, sélectionnez le modèle <b>Vide</b>.

L&#39;option <b>Projet</b> vous permet de filtrer la liste des modèles par fichier de projet. Cela facilite la recherche des modèles personnalisés dans les emplacements ajoutés sous la section <b>Général</b> des paramètres du projet pour le fichier de projet.

>[!WARNING]
>
> Si vous sélectionnez le mauvais modèle, vous *ne pouvez pas* passer à un autre modèle après avoir créé le graphique.\
> Pour importer votre graphique existant vers un autre modèle, vous pouvez créer un graphique à l’aide du modèle approprié et copier-coller le graphique vers le nouveau modèle. Reconnectez les nœuds selon les besoins, y compris le nœud [racine](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md).

La liste des modèles peut être affichée dans différents modes à l&#39;aide des *boutons* en regard de la zone de liste déroulante **Projet** :

* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-04.png)Afficher les modèles récemment utilisés** : filtre la liste pour afficher les derniers modèles utilisés dans l&#39;ordre *du plus récent au moins récent*, l&#39;élément supérieur étant le plus récent
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-05.png)Graphiques d&#39;affichage** : les modèles sont affichés selon leur *étiquette uniquement*, dans l&#39;ordre des fichiers [Substance 3D](https://www.adobe.com/fr/products/substance3d/3d-augmented-reality.html) dans le répertoire des modèles
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-06.png)Afficher les fichiers Substance 3D** : les modèles sont affichés selon leur étiquette en tant que *enfants du fichier Substance 3D auquel ils appartiennent*, dans l&#39;ordre des fichiers dans le répertoire des modèles
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-07.png)Répertoires d&#39;affichage** : les modèles sont affichés par leur étiquette en tant que *enfants du répertoire auquel ils appartiennent*, dans l&#39;ordre des fichiers dans le répertoire des modèles

### Propriétés

La section <b>Propriétés du graphique </b> vous permet de configurer des informations de base concernant le nouveau graphique. Vous pouvez toujours les modifier par la suite, mais il est judicieux de faire attention d’abord et de les configurer de manière appropriée pour votre cas d’utilisation.

* <b>Nom du graphique</b> : identifiant du graphique. Il doit être unique pour un package donné et ne peut pas inclure d’espaces ni de caractères spéciaux.
* <b>Créer un graphique dans le package</b> : vous pouvez utiliser cette zone de liste déroulante pour créer un *nouveau* package pour le nouveau graphique ou ajouter le nouveau graphique à tout *package* existant déjà chargé dans le panneau Explorateur.\
  Remarque : si le processus de création est démarré à l&#39;aide de la méthode <b>4</b> (voir ci-dessus), ce paramètre est *prédéfini* par rapport au package existant à partir duquel le processus a été démarré.
* <b>Détails du modèle</b> : cette section fournit un court texte expliquant les caractéristiques et l’objectif du modèle
