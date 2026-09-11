---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ''
description: Utilisez le nœud FX-Map pour appliquer des graphes de fonction aux textures de création de motifs et d’effets procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 2%

---


# FX-Map

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : FX-Map](fx-map.resources/fxmap.png "Noeud atomique : FX-Map"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Le FX-Map peut répliquer et subdiviser une image ou un motif saisi à plusieurs reprises, et contrôler la répartition de chaque motif grâce à des paramètres et des fonctions logiques.

C&#39;est l&#39;un des noeuds atomiques les plus puissants, ainsi que le nœud le plus complexe disponible dans l&#39;application.

</td>
</tr>
</table>

Comme pour le [Processeur de pixels](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), c&#39;est à vous de définir et de créer les fonctions qui déterminent le comportement et la sortie de ce nœud.

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

>[!TIP]
>
> Consultez le [guide dédié](../../../../function-graphs/fxmaps/fxmaps.md) pour en savoir plus sur le processus de FX-Map.

>[!IMPORTANT]
>
> Il est recommandé de bien connaître tous les aspects du logiciel et de ne pas rencontrer de problème lors de la création de [fonctions mathématiques](../../../../function-graphs/function-graphs.md) pour les paramètres avant de tenter d&#39;utiliser le nœud FX-Map.

## Exemples

## Paramètres

Gardez à l&#39;esprit que, contrairement à d&#39;autres nœuds, la majorité d&#39;un comportement de FX-Map n&#39;est pas déterminée par les paramètres, mais plutôt [par la modification des fonctions FX-Map](../../../../function-graphs/fxmaps/fxmaps.md) qu&#39;il contient.

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Permet de basculer entre une image en niveaux de gris et une image en couleur. La couleur sera beaucoup plus lente que les niveaux de gris. |
| <b>Arrière-plan</b> *Flottant/Flottant 4* | Définit la couleur de départ de l’arrière-plan sur laquelle composer les résultats. |
| <b>Zone de rendu</b> *Flottant4* | Permet de définir la plage de pixels de départ de chaque côté du FX-Map, ce qui produit un effet de étiré. |
| <b>Zone de Répétition</b> *Flottant4* | Permet de décaler la distance de répétition du FX-Map. |
| <b>Abattre à l&#39;extérieur</b> *Booléen* | Effectue une optimisation en [éliminant](../../../../glossary/glossary.md) les motifs qui se trouvent en dehors de la plage normale. |
| <b>Rugosité</b> *Flottant* | Fonctionne comme un multiplicateur de profondeur et d’opacité. Il applique un biais au processus de fusion FX-map. |
| <b>Opacité globale</b> *Flottant* | Définit l’opacité globale de la sortie du mappage FX. |

## Guide FX-Map

*Bientôt disponible.*

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Arrière-plan</b> *Niveaux de gris/Couleur* PRINCIPAL | Couleur d’arrière-plan de l’image de sortie. |
| <b>Image d&#39;entrée #</b> *Niveaux de gris/Couleur* |  |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

![](fx-map.resources/image2015-9-10-17-28-32.png)
