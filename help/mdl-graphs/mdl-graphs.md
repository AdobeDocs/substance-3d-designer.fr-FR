---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: Apprenez à créer et à utiliser des graphiques de langage de définition de matériau dans Substance 3D Designer pour des workflows de matériaux avancés.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graphiques MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---


# Graphiques MDL

Cette page présente des graphiques MDL dans Substance 3D Designer, qui vous permettent de créer des matériaux MDL et de prévisualiser leur comportement en temps réel.

![Matériau MDL malachite](../assets/mdl-malachite-example.jpg "Matériau MDL malachite")

*Du malachite avec chrysocolle, matériau MDL de [Mark Foreman](https://www.artstation.com/oggyart)* *disponible sur notre [Substance share héritée](https://share-legacy.substance3d.com/libraries/4043)* *plateforme*

>[!WARNING]
> 
> Les graphiques MDL et toutes les fonctionnalités associées ont été supprimés de Designer dans la version 16.0.0.
> 
> En savoir plus ici : [Fin de vie du graphique MDL et de l&#39;iray](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++Table des matières

* [Concepts principaux du graphique MDL](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [Création d’un graphique MDL](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [Bibliothèque MDL](/help/mdl-graphs/mdl-library/mdl-library.md)
* [Exposition de paramètres dans les graphiques MDL](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [Graphiques de Substance et matériaux MDL](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [Exportation de contenu MDL](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [Avertissements dans les graphiques MDL](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [Ressources d’apprentissage MDL](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## Vue d’ensemble

MDL est l&#39;acronyme de [Materials Definition Language](http://www.nvidia.com/object/material-definition-language.html) : « une technologie développée par [NVIDIA](https://www.nvidia.com/) pour définir des matériaux basés physiquement pour des solutions de rendu basées physiquement ». (Source : [Documentation NVIDIA MDL](https://raytracing-docs.nvidia.com/mdl/index.html))

Grâce à ce langage, une définition complète de la matière est transférable et peut donc être utilisée dans toutes les applications et tous les moteurs de rendu pour une sortie cohérente. Substance 3D Designer est actuellement la *seule* application proposant la création de nœuds basée sur des graphiques de matériaux MDL, en exposant les fonctions et les types de valeur MDL en tant que nœuds dans un graphique MDL.

Lors de la création de matériaux, vous pouvez utiliser le propre moteur de rendu [Iray](../interface/3d-view/iray/iray.md) de NVIDIA, intégré à Designer et disponible dans le panneau [Vue 3D](../interface/3d-view/3d-view.md), pour prévisualiser le comportement du matériau *de manière interactive*.

Les graphiques MDL sont complémentaires des [graphiques de Substance](../compositing-graphs/substance-compositing-graphs.md), car ces derniers produisent des *textures* qui peuvent être *échantillonnées* par le matériau MDL pour modifier son comportement et son apparence.

Nous vous suggérons de parcourir les sections de cette documentation *dans l’ordre* pour un parcours d’apprentissage guidé, en commençant par les propriétés d’une ressource de graphique MDL, juste en dessous.\
Envie d&#39;intervenir ? Commencez à utiliser les graphiques MDL dans la section [Ressources d&#39;apprentissage MDL](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/first-steps-with-mdl-145654095.html) !

>[!NOTE]
>
> Vous pouvez en savoir plus sur la mise en œuvre technique du langage de définition de matériau dans la [documentation NVIDIA MDL](https://raytracing-docs.nvidia.com/mdl/index.html), qui comprend des liens vers la spécification MDL et le [manuel MDL](http://mdlhandbook.com/), tous créés et gérés par NVIDIA.

![Propriétés de graphique MDL](../assets/mdl-main.png "Propriétés de graphique MDL")

*Propriétés de graphique MDL dans le panneau [Propriétés](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)*

## Propriétés de graphique MDL

### Attributs

Cette section contient des informations concernant le matériel MDL à des fins d’identification, de classification et d’établissement de la paternité.

* <b>Identificateur</b> : nom de cette ressource, qui doit être unique sous son parent dans le package
* <b>Nom d&#39;affichage</b> : nom du matériau MDL affiché dans l&#39;interface
* <b>Icône</b> : image utilisée comme vignette pour ce graphique dans la bibliothèque de Designer
* <b>Masqué\*</b> : lorsqu&#39;il est défini sur* Vrai*, le matériau MDL n&#39;est pas visible dans une bibliothèque MDL, mais existe toujours en interne et peut être référencé
* <b>Afficher dans la bibliothèque</b> : lorsque cette option est définie sur *Vrai*, le graphique MDL s&#39;affiche dans la bibliothèque de Designer
* <b>Description</b> : description du matériau MDL, qui peut être affichée dans l&#39;info-bulle des nœuds d&#39;instance faisant référence à ce graphique
* <b>Catégorie\*</b> : catégorie à laquelle appartient le graphique MDL. Actuellement, cela n’a aucun impact sur le tri du graphique dans la [bibliothèque](../interface/the-library/the-library.md) Designer
* <b>Dans le groupe\*</b> : groupe de bibliothèque auquel appartient le matériau MDL
* <b>Auteur\*</b> : auteur de la documentation MDL
* <b>Contributeurs\*</b> : les contributeurs du matériel MDL autres que l’auteur
* <b>Mots-clés\*</b> : mots-clés pouvant être utilisés pour trouver le contenu MDL dans une recherche de bibliothèque
* <b>Avis de copyright\*</b> : avis de copyright relatif à l’auteur et à l’utilisation du contenu MDL

Remarque : les propriétés marquées d&#39;un astérisque (\*) sont des annotations MDL à utiliser par les intégrations de bibliothèques MDL et n&#39;ont* aucun impact* dans Designer.

### Entrées du graphe

Cette section répertorie les paramètres interactifs connectés aux [paramètres exposés](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/exposing-a-parameter-145654033.html) du graphique MDL et définit leurs *valeurs par défaut*. Ils peuvent être *modifiés* et *réorganisés* à tout moment.

L&#39;interface et le comportement de ces entrées sont définis par le *type de valeur* et les *plages* des paramètres exposés auxquels elles sont connectées. Par exemple :

* Une valeur exposée de type <b>Float</b> définie sur une plage souple de [0.0,4.0] s&#39;affichera sous la forme d&#39;un *curseur unique* compris entre 0.0 et 4.0
* Une valeur exposée de type <b>Couleur</b> s&#39;affichera sous la forme d&#39;un *widget de couleur*, qui comprend un dégradé de sélection et une vignette de couleur

Pour réorganiser les entrées du graphique, placez le curseur sur la *poignée sombre* à gauche du paramètre, cliquez et *maintenez* <b>LMB</b>, puis faites glisser le curseur vers le haut ou vers le bas. Cet ordre personnalisé sera utilisé pour afficher les propriétés du matériau MDL dans les contextes suivants :

* Nœuds d&#39;instance référençant le graphique MDL pour ce matériau
* Propriétés du matériau dans la [vue 3D](../interface/3d-view/3d-view.md)
* Intégrations MDL tierces
