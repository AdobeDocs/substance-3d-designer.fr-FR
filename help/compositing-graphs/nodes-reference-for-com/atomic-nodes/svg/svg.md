---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ""
description: Utilisez le nœud SVG pour importer et rendre des images vectorielles de SVG en tant que textures de création d’éléments graphiques évolutifs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---

# SVG

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Noeud atomique : SVG](svg.resources/comp_svg_1.png "Noeud atomique : SVG"){width="100%"}

<b>Entrée :</b> Noeuds atomiques

</td>
<td style="border: 0;" valign="top">

Effectue le rendu d&#39;une [image SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) sous forme d&#39;image bitmap. En d’autres termes, mappe les formes vectorielles aux pixels.

Il existe plusieurs façons de créer ce nœud, et toutes nécessitent que vous compreniez[la différence entre lier et importer des ressources](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="svg.resources/svg-tooltip.gif" alt="info-bulle svg" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Vous pouvez soit créer le nœud à partir de zéro, soit déposer un fichier de SVG dans la Vue du graphe de données.


>[!TIP]
>
> Les images SVG générées ou importées peuvent être modifiées à l&#39;aide des [outils d&#39;édition vectorielle](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) dans le dock [Vue 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Ce nœud dépend d&#39;une ressource externe, il y a donc quelques points à garder à l&#39;esprit lorsque vous travaillez avec eux :
> 
> * Les nœuds SVG peuvent renvoyer une couleur ou des niveaux de gris, mais la couleur par défaut est sélectionnée même si la ressource est un vecteur en niveaux de gris. Cela peut affecter les performances et la complexité du graphe. Assurez-vous donc toujours de passer en [mode colorimétrique](#parameters) « Niveaux de gris » si nécessaire.
> * La suppression d&#39;un nœud de SVG ne supprime pas la [ressource de SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) dans votre [package](../../../../glossary/glossary.md). Vous devez le faire manuellement dans l&#39;[Explorateur](../../../../interface/the-explorer-window/the-explorer-window.md).
> * Les formes SVG sont [tesselées](../../../../glossary/glossary.md) en géométrie/polygones, puis *pixellisées* afin d&#39;être utilisées dans les graphes de Substance en tant qu&#39;images bitmap. La technologie utilisée pour ces opérations ne prend pas en charge plusieurs propriétés vectorielles, telles que les contours. En savoir plus sur ces limitations [ici](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

>[!WARNING]
>
> Les formes SVG sont [tesselées](../../../../glossary/glossary.md) en géométrie/polygones, puis *pixellisées* afin d&#39;être utilisées dans les graphes de Substance en tant qu&#39;images bitmap.
> 
> La technologie utilisée pour ces opérations ne prend pas en charge plusieurs propriétés vectorielles, telles que les contours.
> 
> En savoir plus sur ces limitations [ici](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).


## Paramètres

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Détermine le type de sortie du nœud, à retourner en couleur ou en niveaux de gris. |
| <b>Couleur d&#39;arrière-plan</b> *Couleur/Niveaux De Gris* | Définit la couleur d’arrière-plan de l’image de sortie à utiliser sur les zones non couvertes par une forme vectorielle.   *Est remplacé par l&#39;entrée &#39;[Arrière-plan](#inputs)&#39; lorsque cette entrée est connectée.* |
| <b>Chemin de ressource PKG</b> *Chaîne* | Chemin d&#39;accès à la [ressource SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) référencée par le nœud.   Il est recommandé de ne pas taper manuellement, mais de copier une ressource de l&#39;explorateur et de la coller dans le champ de texte du paramètre, ou de glisser-déposer une ressource bitmap directement de l&#39;[Explorateur](../../../../interface/the-explorer-window/the-explorer-window.md) sur le nœud SVG dans le graphe. |

## Outils d’édition vectorielle

Les formes vectorielles peuvent être modifiées dans Designer. En savoir plus sur les outils de modification dans [cette section](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Arrière-plan</b> *Niveaux de gris/Couleur* PRINCIPAL | Définit la couleur d’arrière-plan de l’image de sortie à utiliser sur les zones non couvertes par une forme vectorielle.   *Remplace le paramètre &#39;[Couleur d&#39;arrière-plan](#parameters)&#39; lors de la connexion.* |


## Exemples

*Bientôt disponible.*
