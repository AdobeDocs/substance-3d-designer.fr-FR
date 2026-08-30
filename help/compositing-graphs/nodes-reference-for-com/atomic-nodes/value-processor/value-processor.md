---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ''
description: Utilisez le nœud Processeur de valeurs pour traiter et manipuler les valeurs de texture à l’aide d’opérations mathématiques pour des réglages personnalisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processeur de valeurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 4%

---


# Processeur de valeurs

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : processeur de valeur](value-processor.resources/comp_valueprocessor_1.png "Nœud atomique : processeur de valeur"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Calcule un [graphique de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) et génère son résultat.

Elle est comparable à un [processeur de pixels](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), à la différence qu&#39;elle ne calcule pas une fonction pour chaque pixel, mais plutôt une valeur unique et la rend [disponible dans un graphique de Substance](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

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
> Ce nœud est un bon point de départ pour en savoir plus sur les [graphiques de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> N&#39;oubliez pas non plus que l&#39;utilisation de ce type de graphique et l&#39;exécution d&#39;opérations mathématiques sont obligatoires pour obtenir n&#39;importe quoi de ce nœud.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Fonction de processeur de valeur</b> *Tout type de valeur disponible* | [graphe de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) évalué pour calculer la valeur de sortie. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Image d&#39;entrée #</b> *Niveaux de gris/Couleur* | Utilisez un nœud [Échantillon de couleur](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) ou [Échantillon de niveaux de gris](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) pour accéder aux valeurs dans l&#39;entrée de l&#39;index spécifié. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Tout type de valeur disponible* |  |

## Exemples

*Bientôt disponible.*
