---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ''
description: Utilisez le nœud FX-Map pour appliquer des graphiques de fonction aux textures afin de créer des motifs et des effets procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 2%

---


# FX-Map

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : FX-Map](fx-map.resources/fx-map-01.png "Nœud atomique : FX-Map"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

La FX-Map peut répliquer et subdiviser une image ou une entrée de motif encore et encore, et contrôler la distribution de chaque motif grâce à des paramètres et des fonctions logiques.

C&#39;est l&#39;un des nœuds atomiques les plus puissants, ainsi que le nœud le plus complexe disponible dans l&#39;application.

</td>
</tr>
</table>

Comme pour le [processeur de pixels](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), il vous appartient de définir et de créer les fonctions qui déterminent le comportement et la sortie de ce nœud.

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
> Consultez le [guide dédié](../../../../function-graphs/fxmaps/fxmaps.md) pour en savoir plus sur le processus FX-Map.

>[!IMPORTANT]
>
> Il est recommandé de bien connaître tous les aspects du logiciel et d&#39;éviter tout problème lors de la création de [fonctions mathématiques](../../../../function-graphs/function-graphs.md) pour les paramètres avant de tenter d&#39;utiliser le nœud FX-Map.

## Exemples

## Paramètres

Gardez à l&#39;esprit que contrairement aux autres nœuds, la majorité du comportement d&#39;un FX-Map n&#39;est pas déterminée par les paramètres, mais plutôt [par la modification des fonctions FX-Map](../../../../function-graphs/fxmaps/fxmaps.md) qu&#39;il contient.

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Permet de basculer entre une image en niveaux de gris et une image en couleur. La couleur sera beaucoup plus lente que les niveaux de gris. |
| <b>Arrière-plan</b> *Float/Float4* | Définit la couleur de départ de l’arrière-plan sur laquelle composer les résultats. |
| <b>Zone de rendu</b> *Float4* | Permet de définir la plage de pixels de départ de chaque côté de la FX-Map, ce qui produit un effet d’étirement. |
| <b>Zone de mosaïque</b> *Float4* | Permet de décaler la distance de mosaïque du FX-Map. |
| <b>Abattre à l&#39;extérieur</b> *Booléen* | Effectue une optimisation en [éliminant](../../../../glossary/glossary.md) les motifs qui se trouvent en dehors de la plage normale. |
| <b>Rugosité</b> *Flotter* | Fonctionne comme un multiplicateur de profondeur et d’opacité. Il applique un biais au processus de fusion FX-map. |
| <b>Opacité globale</b> *Flotter* | Définit l’opacité globale de la sortie du mappage FX. |

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

![](fx-map.resources/fx-map-02.png)
