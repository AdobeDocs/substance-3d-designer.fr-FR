---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ""
description: Utilisez le nœud de Processeur de valeurs pour traiter et manipuler les valeurs de texture à l’aide d’opérations mathématiques pour des réglages personnalisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processeur de valeurs
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%
---

# Processeur de valeurs

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![Noeud atomique : Processeur de valeurs](value-processor.resources/comp_valueprocessor_1.png "Noeud atomique : Processeur de valeurs"){width="100%"}

</td>
<td style="border: 0;" valign="top">

Calcule un [graphe de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) et génère son résultat.

Elle est comparable à un [Processeur de pixels](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), à la différence qu&#39;elle ne calcule pas une fonction pour chaque pixel, mais plutôt une valeur unique et la rend [disponible dans un graphe de Substance](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="value-processor.resources/value-processor-tooltip.gif" alt="info-bulle value-processor" /></div>


>[!TIP]
>
> Ce nœud est un bon point de départ pour découvrir les [graphes de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Considérez également que travailler avec ce type de graphe et effectuer des opérations mathématiques est obligatoire pour obtenir quoi que ce soit de ce nœud.


## Paramètres

|  |  |
| --- | --- |
| <b>Fonction de Processeur de valeurs</b> *Tout type de valeur disponible* | [graphe de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) évalué pour calculer la valeur de sortie. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Image d&#39;entrée #</b> *Niveaux de gris/Couleur* | Utilisez un nœud [Échantillon de couleur](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) ou [Échantillon de niveaux de gris](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) pour accéder aux valeurs dans l&#39;entrée de l&#39;index spécifié. |


## Exemples

*Bientôt disponible.*
