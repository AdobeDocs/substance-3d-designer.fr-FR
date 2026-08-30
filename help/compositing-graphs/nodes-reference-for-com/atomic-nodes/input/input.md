---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/input.html"
breadcrumb-title: ''
description: Utilisez le nœud Entrée pour définir les paramètres d’entrée des graphiques de Substances pouvant être affichés et ajustés par les utilisateurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entrée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Entrée

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nœud atomique : couleur d&#39;entrée](input.resources/comp_inputcolor_1.png "Nœud atomique : couleur d&#39;entrée"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![Nœud atomique : Niveaux de gris d&#39;entrée](input.resources/comp_inputgrayscale_1.png "Nœud atomique : Niveaux de gris d&#39;entrée"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![Nœud atomique : valeur d&#39;entrée](input.resources/comp_inputnumeric_1.png "Nœud atomique : valeur d&#39;entrée"){width="200px"}

</td>
</tr>
</table>

Les nœuds d’entrée sont un type spécial de nœud qui crée un emplacement dynamique dans votre graphique, ce qui permet de connecter n’importe quelle entrée une fois que votre graphique est utilisé dans un autre contexte.

Contrairement aux [nœuds de sortie](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), vous devez explicitement placer une entrée Couleur, Niveaux de gris ou Valeur. Il n’est pas possible de créer vos propres entrées « agnostiques » qui changent de type en fonction de ce qui y est connecté.

Les nœuds d&#39;entrée ne sont pas aussi essentiels que les [nœuds de sortie](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) : vous pouvez avoir des graphiques avancés qui fonctionnent parfaitement et qui n&#39;ont pas besoin d&#39;une entrée. Les entrées ne sont utilisées que lorsque vous souhaitez baser le résultat de votre instance de graphique ou de nœud sur une entrée externe, par exemple lors de la création d&#39;[instance](../../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)ou d&#39;un [filtre](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/effects/filter) pour Substance 3D Painter.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## PARAMÈTRES

</td>
<td style="border: 0;" valign="top">

### ATTRIBUTS

</td>
<td style="border: 0;" valign="top">

### HÉRITAGE

</td>
<td style="border: 0;" valign="top">

### ATTRIBUTS D’INTÉGRATION

</td>
</tr>
</table>

## Paramètres

Par défaut, la couleur d’entrée ou les niveaux de gris renvoient du noir si aucun élément n’est connecté. Vous pouvez soit définir une valeur par défaut différente, soit faire glisser une [ressource bitmap](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) existante de l&#39;[Explorateur](../../../../interface/the-explorer-window/the-explorer-window.md) vers le nœud d&#39;entrée de votre graphique, pour prévisualiser ces données dans l&#39;emplacement. Cela ne fonctionne que pour les entrées Couleur et Niveaux de gris. La valeur par défaut est persistante lorsqu’elle est utilisée dans d’autres contextes, le bitmap d’aperçu est ignoré partout ailleurs.

Si vous voulez le voir avec les sorties d&#39;un autre Graphe, vous devrez soit exporter ce Graphe en Bitmap pour la méthode ci-dessus, soit utiliser l&#39;édition « In-Context ».

|  |  |
| --- | --- |
| <b>Chemin de ressource PKG</b> *Chaîne* | Pointe vers une ressource bitmap personnalisée pour prévisualisation. |
| <b>Valeur par défaut</b> *Couleur/Niveaux De Gris/Valeur* | Permet d&#39;utiliser une autre valeur que le noir comme entrée par défaut, si rien n&#39;est connecté à cet emplacement. |

## Attributs

|  |  |
| --- | --- |
| <b>Identifiant</b> *Chaîne* | Le seul attribut unique et obligatoire. Ne peut pas contenir d&#39;espaces.   Celui-ci est utilisé pour étiqueter les entrées si aucun libellé n&#39;est configuré et pour différencier les sorties. Ne les laissez pas simplement à « input\_1 » ! |
| <b>Description</b> *Chaîne* | Description facultative utilisée dans la bibliothèque Designer et l’étagère Painter. |
| <b>Libellé</b> *Chaîne* | Libellé de l’interface utilisateur utilisé pour un étiquetage agréable dans l’interface utilisateur de Designer et Painter. Peut contenir des espaces.   Il est recommandé de définir un nom similaire à l’Identifiant, avec des barres d’espace au lieu des traits de soulignement. |
| <b>Données utilisateur</b> *Chaîne* | Données utilisateur supplémentaires et facultatives pouvant être utilisées pour des opérations de filtrage spécifiques. Il s’agit essentiellement d’un champ de données personnalisé, générique. |
| <b>Groupe</b> *Chaîne* | Attribut de groupe utilisé pour regrouper les entrées afin de créer des [modes de création de liens](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) Designer.   Les entrées dotées d’un attribut de groupe identique (sensible à la casse) seront présentées comme une connexion unique dans Compact Mode de matériau. |

## Transmission

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Lorsque plusieurs entrées sont présentes, vous devez faire attention à la façon dont le graphique [héritera de ses paramètres de base](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) à partir de ces entrées.\
Les paramètres de base incluent, entre autres, la <b>taille de sortie</b>, le <b>format de sortie</b> et le <b>mode de mosaïque</b>.

</td>
<td width="33.33%" style="border: 0;" valign="top">

[![Entrée principale dans le graphique de Substance](input.resources/node-primary-input.png)](https://helpx.adobe.com/Primary%20input%20in%20Substance%20graph)

</td>
</tr>
</table>

Une entrée peut être définie comme [entrée principale](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Cette entrée pilote ensuite les attributs de toutes les entrées dont la méthode d&#39;héritage est définie sur *Relative au parent*. Il s&#39;agit de la méthode d&#39;héritage *définie par défaut* sur les nœuds d&#39;entrée.

Vous pouvez définir un nœud d&#39;entrée comme entrée principale d&#39;un graphique en cliquant sur *RMB* sur le nœud et en sélectionnant l&#39;option <b>Définir comme entrée principale</b> dans le menu contextuel.\
L&#39;entrée Primary d&#39;un nœud est marquée d&#39;un *petit point sombre dans le connecteur* (entouré en rouge dans l&#39;exemple à côté de cette section).

Sinon, toute entrée définie sur la méthode d&#39;héritage *Relative à l&#39;entrée* héritera des attributs du nœud auquel elle est connectée, *indépendamment* de l&#39;entrée Primary.

Enfin, vous pouvez remplacer n&#39;importe quelle valeur pour un attribut donné en définissant sa méthode d&#39;héritage sur *Absolue*.

>[!TIP]
>
> Pour en savoir plus sur l&#39;héritage, accédez à la page [Héritage dans les graphiques de Substances](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) de cette documentation.

>[!IMPORTANT]
>
> La méthode d&#39;héritage *Relative à l&#39;entrée* pour les nœuds d&#39;entrée n&#39;est *pas prise en charge* dans [Actifs Substance 3D (SBSAR)](https://helpx.adobe.com/substance-3d-assets.html). Définissez toutes les méthodes d&#39;héritage des nœuds d&#39;entrée sur *Relative au parent* avant de publier votre package.

## Attributs d&#39;intégration

Les entrées ne sont pas directement envoyées à la vue 3D, mais leurs attributs d&#39;utilisation sont utilisés par [Substance 3D Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home) pour remplir automatiquement les emplacements avec certains mappages (principalement utilisés avec des [filtres](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/effects/filter)).

En outre, les attributs Utilisation sont également utilisés avec les [modes de création de lien](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md), pour correspondre aux emplacements d&#39;entrée et de sortie corrects.

<b>Utilisation</b>

|  |  |
| --- | --- |
| <b>Composant</b> *Chaîne* | Cela détermine quelles couches sont réellement dans l’entrée résultante.   Il s’agit d’un paramètre hérité qui n’est plus utilisé par les intégrations et les graphiques. |
| <b>Utilisation</b> *Chaîne* | Définissez un type ou une utilisation pour cette entrée. Elle indique comment les autres nœuds doivent se connecter à cette entrée. |
| <b>Espace colorimétrique</b> *Chaîne* | Définit l’espace colorimétrique dans lequel cette entrée doit être interprétée. |
