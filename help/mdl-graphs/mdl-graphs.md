---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: Découvrez comment créer et utiliser des graphes Matériau Definition Language dans Substance 3D Designer pour les workflows de matériau avancés.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graphiques MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# Graphiques MDL

Cette page présente des graphiques MDL dans Substance 3D Designer, qui vous permettent de créer des matériaux MDL et de prévisualiser leur comportement en temps réel.

![Matériau MDL de malachite](../assets/mdl-malachite-example.jpg "Matériau MDL de malachite")

*Malachite à la chrysocolle, Matériau MDL de [Mark Foreman](https://www.artstation.com/oggyart)* *disponible sur notre [plateforme](https://share-legacy.substance3d.com/libraries/4043)* *héritée*

>[!WARNING]
> 
> La version 16.0.0 de Designer a supprimé les graphes MDL et toutes les fonctionnalités associées.
> 
> En savoir plus ici : [Fin de vie du graphique MDL et de l&#39;iray](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++Table des matières

* [Concepts principaux du graphique MDL](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [Création d’un graphique MDL](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [Bibliothèque MDL](/help/mdl-graphs/mdl-library/mdl-library.md)
* [Exposer des paramètres dans les Graphes MDL](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [Graphiques de Substance et matériaux MDL](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [Exportation de contenu MDL](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [Avertissements dans les graphiques MDL](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [Ressources d’apprentissage MDL](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## Vue d’ensemble

MDL est l&#39;acronyme de [Matériau Definition Language](http://www.nvidia.com/object/material-definition-language.html) : « une technologie développée par [NVIDIA](https://www.nvidia.com/) pour définir des matériaux basés physiquement pour des solutions de rendu basées physiquement ». (Source : [Documentation NVIDIA MDL](https://raytracing-docs.nvidia.com/mdl/index.html))

Grâce à ce langage, une définition de matériau complète est transférable et peut donc être utilisée dans toutes les applications et tous les systèmes de rendu pour une sortie cohérente. Substance 3D Designer est actuellement la *seule* application proposant la création de nœuds de Matériaux MDL basée sur le graphe, en exposant les fonctions et les types de valeur MDL en tant que nœuds dans un Graphe MDL.

Lors de la création de matériaux, vous pouvez utiliser le propre moteur de rendu [Iray](../interface/3d-view/iray/iray.md) de NVIDIA, intégré à Designer et disponible dans le panneau [Vue 3D](../interface/3d-view/3d-view.md), pour prévisualiser le comportement du matériau *de manière interactive*.

Les graphes MDL sont complémentaires avec les [graphes de Substance](../compositing-graphs/substance-compositing-graphs.md) en ce sens que ces derniers génèrent des *textures* qui peuvent être *échantillonnées* par le Matériau MDL pour affecter son comportement et son apparence.

Nous vous suggérons de parcourir les sections de cette documentation *dans l’ordre* pour un parcours d’apprentissage guidé, en commençant par les propriétés d’une ressource de Graphe MDL, juste en dessous.\
Envie d&#39;intervenir ? Commencez à utiliser les Graphes MDL de la section Ressources d’apprentissage MDL !

>[!NOTE]
>
> Vous pouvez en savoir plus sur la mise en œuvre technique du langage de définition de Matériau dans la [documentation NVIDIA MDL](https://raytracing-docs.nvidia.com/mdl/index.html), qui comprend des liens vers la spécification MDL et le [manuel MDL](http://mdlhandbook.com/), tous créés et gérés par NVIDIA.

![propriétés du Graphe MDL](../assets/mdl-main.png "propriétés du Graphe MDL")

*Propriétés de Graphe MDL dans le panneau Propriétés*

## propriétés du graphe MDL

### Attributs

Cette section contient des informations concernant le Matériau MDL aux fins d’identification, de classification et d’établissement de la paternité.

* <b>Identifiant</b> : nom de cette ressource, qui doit être unique sous son parent dans le package
* <b>Nom d&#39;affichage</b> : nom du Matériau MDL affiché dans l&#39;interface
* <b>Icône</b> : image utilisée comme vignette pour ce graphe dans la bibliothèque de Designer
* <b>Masqué\*</b> : lorsque cette option est définie sur* Vrai*, le Matériau MDL n&#39;est pas visible dans une bibliothèque MDL, mais existe toujours en interne et peut être référencé
* <b>Afficher dans la bibliothèque</b> : lorsque cette option est définie sur *Vrai*, le Graphe MDL s&#39;affiche dans la bibliothèque de Designer
* <b>Description</b> : description du Matériau MDL, qui peut être affichée dans l&#39;info-bulle des instanciers faisant référence à ce graphe
* <b>Catégorie\*</b> : catégorie à laquelle appartient le Graphe MDL. Actuellement, cela n&#39;a aucun impact sur le tri du graphe dans la [bibliothèque](../interface/the-library/the-library.md) de Designer
* <b>Dans le groupe\*</b> : groupe de bibliothèques auquel appartient le Matériau MDL
* <b>Auteur\*</b> : auteur du Matériau MDL
* <b>Contributeurs\*</b> : les contributeurs du Matériau MDL autres que l’auteur
* <b>Mots-clés\*</b> : mots-clés pouvant être utilisés pour rechercher le Matériau MDL dans une recherche de bibliothèque
* <b>Avis de copyright\*</b> : avis de copyright relatif à l’auteur et à l’utilisation du Matériau MDL

Remarque : les propriétés marquées d&#39;un astérisque (\*) sont des annotations MDL à utiliser par les intégrations de bibliothèques MDL et n&#39;ont* aucun impact* dans Designer.

### Entrées du graphe

Cette section répertorie les paramètres interactifs connectés aux paramètres exposés du Graphe MDL et définit leurs *valeurs par défaut*. Ils peuvent être *modifiés* et *réorganisés* à tout moment.

L&#39;interface et le comportement de ces entrées sont définis par le *type de valeur* et les *plages* des paramètres exposés auxquels elles sont connectées. Par exemple :

* Une valeur exposée de type <b>Flottant</b> définie sur une plage souple de [0.0,4.0] s&#39;affichera sous la forme d&#39;un *curseur unique* compris entre 0.0 et 4.0
* Une valeur exposée de type <b>Couleur</b> s&#39;affichera sous la forme d&#39;un *widget de couleur*, qui comprend un dégradé de sélection et une vignette de couleur

Pour réorganiser les entrées de graphe, placez le curseur sur la *poignée sombre* à gauche du paramètre, cliquez et *maintenez* <b>LMB</b>, puis faites glisser le curseur vers le haut ou vers le bas. Cet ordre personnalisé sera utilisé pour afficher les propriétés du Matériau MDL dans les contextes suivants :

* Instanciers faisant référence au Graphe MDL de ce matériau
* Propriétés de matériau dans [vue 3D](../interface/3d-view/3d-view.md)
* Intégrations MDL tierces
