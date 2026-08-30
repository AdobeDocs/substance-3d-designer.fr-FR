---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ''
description: Utilisez le nœud de réorganisation des couches pour réorganiser les couches de couleur dans les textures afin de créer des effets de couleur et des permutations de couche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Permutation de canaux
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# Permutation de canaux

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : réorganisation des canaux](channel-shuffle.resources/comp_shuffle.png "Nœud atomique : réorganisation des canaux"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Réorganise les canaux de couleur d’une ou deux images d’entrée dans l’image de sortie.

C’est-à-dire qu’il prend deux entrées et vous permet de renvoyer une sortie dans laquelle l’une des couches Rouge, Vert, Bleu et Alpha est permutée ou définie sur l’une des couches à partir de l’entrée.

Il vous permet essentiellement de compresser et d&#39;échanger les canaux de RGB de n&#39;importe quelle manière possible. Les entrées de niveaux de gris sont traitées comme si elles étaient en couleur : le rouge, le vert, le bleu et l’Alpha renvoient tous les mêmes valeurs.

</td>
</tr>
</table>

La fonctionnalité Réorganisation des canaux offre des options de base, mais dans la plupart des cas de packing de canal ou d’entrelacement et de définition de canaux Alpha, il est plus rapide d’utiliser la [fusion RVBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), le [fractionnement RVBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), la [fusion Alpha](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md) et le [fractionnement Alpha](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md). Ils sont configurés pour effectuer des actions par défaut qui ne nécessitent pas de modifier plusieurs paramètres et de convertir ensuite en niveaux de gris. Si vous recherchez une version plus avancée avec davantage d&#39;options de fusion, consultez le [Mélangeur de couches](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md).

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
| <b>Canal rouge</b> *Nombre entier* | Choisissez la couche source à insérer dans la couche Rouge de l’image de sortie. |
| <b>Canal vert</b> *Nombre entier* | Choisissez la couche source à insérer dans la couche verte de l’image de sortie. |
| <b>Canal bleu</b> *Nombre entier* | Choisissez la couche source à insérer dans la couche bleue de l’image de sortie. |
| <b>canal Alpha</b> *Nombre entier* | Sélectionnez la couche source à insérer dans la couche Alpha de l’image de sortie. |

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée 1</b> *Couleurs/Niveaux de gris* PRINCIPAUX | Image d’entrée principale. |
| <b>Entrée 2</b> *Couleur/Niveaux De Gris* | Image d’entrée secondaire. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
