---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Familiarisez-vous avec les avertissements dans les graphes de composition de Substances et découvrez comment résoudre les problèmes et erreurs courants.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avertissements dans les graphes Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 1%

---


# Avertissements dans les graphes Substance

Cette page répertorie les messages d&#39;avertissement et d&#39;erreur qui peuvent être déclenchés par les [graphes de Substance](../../compositing-graphs/substance-compositing-graphs.md) dans Substance 3D Designer, et propose des étapes de dépannage courantes pour chacun d&#39;eux.

Les avertissements sont affichés dans l&#39;info-bulle de l&#39;icône d&#39;avertissement pour la ressource graphe dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md), ainsi que dans le coin inférieur gauche de la [Vue du graphe](../../interface/the-graph-view/the-graph-view.md) si le graphe est chargé.

## ![(erreur)](warnings-in-substance-compositing-graphs.resources/error.svg) Aucun nœud de sortie défini

Le graphe n&#39;a pas de nœud [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).

Solution **![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg)**

Ajoutez un ou plusieurs nœuds [Sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) au graphe et connectez-y la sortie du dernier nœud d&#39;un flux.

>[!NOTE]
>
> Les modèles de graphe disponibles via la boîte de dialogue [Nouveau graphe](../creating-compositing-gra/creating-a-substance-compositing-graph.md) ont des nœuds de sortie prédéfinis prêts à être utilisés.

![Correction de l’avertissement « Aucun nœud de sortie défini »](warnings-in-substance-compositing-graphs.resources/warnings-comp-output.gif "Correction de l’avertissement « Aucun nœud de sortie défini »"){width="512px"}

### ![(erreur)](warnings-in-substance-compositing-graphs.resources/error.svg) La fonction du paramètre *[x]* comporte des avertissements

Le [graphe de fonction](../../function-graphs/function-graphs.md) appliqué au paramètre spécifié du nœud spécifié a au moins un avertissement.\
Le paramètre de nœud est spécifié entre crochets après le libellé du nœud, à la suite du modèle Node[Parameter].

E.g. Couleur uniforme[Couleur De Sortie], Processeur de pixels[Fonction Par Pixel]

Solution **![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg)**

Localisez le nœud qui émet l&#39;avertissement par son étiquette et son badge d&#39;avertissement dans la [Vue du graphe](../../interface/the-graph-view/the-graph-view.md), puis sélectionnez-le pour afficher ses propriétés dans le panneau [Propriétés](../../interface/properties/properties.md). Recherchez le paramètre émettant l&#39;avertissement et ouvrez sa fonction en cliquant sur le bouton **Modifier la fonction**.

Ensuite, évaluez les avertissements répertoriés dans le coin inférieur gauche de la Vue du graphe et résolvez les problèmes. Vous pouvez vous référer à la page [Avertissements dans les graphes de fonction](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md) pour la résolution des avertissements signalés dans les graphes de fonction.

![Correction de l’avertissement « La fonction de paramètre comporte des avertissements »](warnings-in-substance-compositing-graphs.resources/warnings-comp-param-function.gif "Correction de l’avertissement « La fonction de paramètre comporte des avertissements »")

### ![(erreur)](warnings-in-substance-compositing-graphs.resources/error.svg) Les données référencées comportent des avertissements

La ressource référencée par un nœud comporte un ou plusieurs avertissements. Voici quelques nœuds référençant une ressource :

* Un nœud [instance de graphe](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) référence un graphe
* Un nœud [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) référence une [ressource Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Un nœud [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) référence une [ressource SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Un nœud [Texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) référence une [ressource Police](../../resources/font-resource/font-resource.md)

Solution **![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg)**

Dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md), recherchez la ressource référencée et résolvez tous les avertissements déclenchés par la ressource :

* Pour les graphes, reportez-vous aux autres éléments de cette page
* Pour tout autre type de ressource, consultez la page [Avertissements des dépendances](../../resources/warnings-from-dep/warnings-from-dependencies.md)

![Correction de l’avertissement « Les données référencées comportent des avertissements »](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-data.gif "Correction de l’avertissement « Les données référencées comportent des avertissements »")

### Ressource de référence ![(erreur)](warnings-in-substance-compositing-graphs.resources/error.svg) introuvable

La ressource référencée par un nœud est introuvable dans le chemin d&#39;accès enregistré dans le fichier [Substance 3D](https://www.adobe.com/fr/products/substance3d/3d-augmented-reality.html) (SBS). Voici quelques nœuds référençant une ressource :

* Un nœud [instance de graphe](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) référence un graphe
* Un nœud [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) référence une [ressource Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Un nœud [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) référence une [ressource SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Un nœud [Texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) référence une [ressource Police](../../resources/font-resource/font-resource.md)

Solution **![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg)**

Pour [instance de graphe](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) nœuds

Vérifiez que le graphe source existe dans le package situé au chemin d&#39;accès enregistré dans leur attribut **Package**.\
Si ce n’est pas le cas, supprimez l’instancier et remplacez-le par un instancier faisant référence à un package valide. Vous pouvez également recréer le package et le graphe référencés par l&#39;instancier, puis recharger le package hôte en cliquant sur le RMB dessus dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md) et en sélectionnant l&#39;option **Recharger** dans le menu contextuel.

Pour les nœuds [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md), [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) ou [Texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

Recherchez les ressources référencées dans le panneau Explorateur et vérifiez qu&#39;elles existent à l&#39;emplacement enregistré dans leur attribut **Chemin d&#39;accès**.\
Si ce n&#39;est pas le cas, cliquez sur RMB sur l&#39;élément de ressource dans l&#39;Explorateur et sélectionnez l&#39;option **Redéfinir l&#39;emplacement...** dans le menu contextuel pour définir un nouveau fichier cible valide pour cette ressource.

![Correction de l’avertissement « Ressource de référence introuvable »](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-resource.gif "Correction de l’avertissement « Ressource de référence introuvable »")

### ![(erreur)](warnings-in-substance-compositing-graphs.resources/error.svg) Le nœud de texte utilise une police non valide

Un nœud [Texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) référence une police qui ne peut pas être chargée ou analysée correctement.

<b> ![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Solution</b>

Sélectionnez le nœud [Texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) et notez la valeur de sa propriété <b>Font</b>. Recherchez le fichier source de cette police sur votre système et assurez-vous qu&#39;il est *sain*, par exemple en l&#39;utilisant dans une autre application telle qu&#39;un éditeur de texte. Remplacez la police par un fichier de police saine si nécessaire ou changez le nœud Texte pour une autre police.
