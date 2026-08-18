---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: Utilisez le nœud Processeur de pixels pour traiter des pixels individuels à l’aide d’expressions personnalisées pour une manipulation de texture avancée.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processeur de pixels
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Processeur de pixels

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : processeur de pixels](../../../../assets/comp_pixelprocessor_1.png "Nœud atomique : processeur de pixels"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Génère une image où la valeur de chaque pixel est le résultat du [graphique de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) spécifié.

Le processeur de pixels vous permet d’exécuter une fonction personnalisée pour chaque pixel renvoyé en sortie, sur une entrée facultative.

C&#39;est de loin le nœud le plus polyvalent, car il permet d&#39;exécuter n&#39;importe quelle opération mathématique et de retourner des résultats à l&#39;intérieur de votre graphique.

</td>
</tr>
</table>

Comme pour [FX-Map](../../../../function-graphs/fxmaps/fxmaps.md), il nécessite la configuration de la fonctionnalité interne pour effectuer toute opération. Le processeur de pixels diffère de FX-Map en ce sens qu’il ne se concentre pas sur le placement de motifs, plusieurs fonctions contrôlant la forme et le placement des motifs. Au lieu de cela, une seule fonction est exécutée en parallèle pour chaque pixel, chaque pixel ignorant les résultats de calcul de ses voisins.

Le processeur de pixels est similaire au [processeur de valeurs](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), qui s&#39;exécute sur des valeurs uniques et peut fournir une optimisation agréable par rapport au processeur de pixels.

Pour toute personne habituée à créer des fonctions de [shader](../../../../glossary/glossary.md) dans des éditeurs basés sur les nœuds, le processeur Pixel doit offrir un environnement familier.

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
> Un fichier de projet annoté démontrant les utilisations simples du nœud de processeur Pixel est disponible dans la section [Exemples de graphiques de Substance](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) de cette documentation.
> 
> Le nœud [Value processor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) est un bon point de départ pour découvrir les [graphiques de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> N&#39;oubliez pas non plus que l&#39;utilisation de ce type de graphique et l&#39;exécution d&#39;opérations mathématiques sont obligatoires pour obtenir n&#39;importe quoi de ce nœud.
> 
> Nous vous recommandons également de vous familiariser avec le concept d&#39;[UV](../../../../glossary/glossary.md), d&#39;[échantillonnage de texture](../../../../glossary/glossary.md) et les vecteurs.

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
| <b>Mode colorimétrique</b> *Booléen* | Permet de basculer entre une image en niveaux de gris et une image en couleur. |
| <b>Par fonction de pixel</b> *Float/Float4* | [Graphique de fonction de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) évalué par pixel dans l&#39;image de sortie.   Utilisez le nœud [Get Float2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) défini sur la variable <b>$pos</b> pour accéder à la position [normalisée](../../../../glossary/glossary.md) du pixel actuel. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Image d&#39;entrée #</b> *Niveaux de gris/Couleur* | Utilisez un nœud [Échantillon de couleur](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) ou [Échantillon de niveaux de gris](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) pour accéder aux valeurs dans l&#39;entrée de l&#39;index spécifié. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
