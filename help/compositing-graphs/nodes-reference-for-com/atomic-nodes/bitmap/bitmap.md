---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: Utilisez le nœud Bitmap pour importer et utiliser des images bitmap en tant que textures dans des graphiques de composition de Substances.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 989234054615406114d2f7664ebee6f8c86f4bf2
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# Bitmap

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nœud atomique : Bitmap](bitmap.resources/comp_bitmap.png "Nœud atomique : Bitmap"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Charge une [ressource bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) dans le graphique.

Ce nœud est utilisé pour importer un [bitmap](../../../../glossary/glossary.md) dans votre graphique ou pour créer un bitmap à utiliser avec les [outils de peinture bitmap](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

Il existe plusieurs façons de créer ce nœud, et toutes nécessitent que vous compreniez[la différence entre lier et importer des ressources](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

</td>
</tr>
</table>

Vous pouvez soit créer le nœud à partir de zéro, soit déposer un [bitmap](../../../../glossary/glossary.md) dans un format pris en charge dans la vue Graphique.

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
> Les bitmaps 8 bits générés ou importés peuvent être peints à l&#39;aide des [outils de peinture bitmap](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) dans le dock [Vue 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Ce nœud dépend d&#39;une ressource externe, il y a donc quelques points à garder à l&#39;esprit lorsque vous travaillez avec eux :
> 
> * Les nœuds bitmap peuvent renvoyer une couleur ou une échelle de gris, mais la couleur est définie par défaut, même si la ressource est un bitmap en niveaux de gris. Cela peut affecter les performances et la complexité du graphique. Assurez-vous donc toujours de passer en [mode colorimétrique](#parameters) « Niveaux de gris » si nécessaire.
> * La suppression d&#39;un nœud bitmap ne supprime pas la [ressource Bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) dans votre [pack](../../../../glossary/glossary.md). Vous devez le faire manuellement dans l&#39;[Explorateur](../../../../interface/the-explorer-window/the-explorer-window.md).
> * D&#39;autre part, soyez prudent lorsque vous supprimez une [ressource Bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) dans l&#39;Explorateur : elle fonctionnera toujours dans le graphique pour cette session, car elle est conservée dans le cache, mais elle sera marquée comme manquante lors du prochain chargement du [package](../../../../glossary/glossary.md).
> * Lorsqu&#39;un graphique de Substance est [cuit](../../../../glossary/glossary.md), la résolution du bitmap est fixée à sa résolution dans le graphique et non en fonction de sa taille d&#39;origine. Il est recommandé de s&#39;assurer que le [paramètre de base](../../../../glossary/glossary.md) « Taille de sortie » d&#39;un nœud Bitmap utilise la [méthode d&#39;héritage](../../../../glossary/glossary.md) « Absolue » et que le nœud est suivi d&#39;un nœud [Transformation 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) défini sur « Relatif au parent » (c&#39;est-à-dire la résolution du graphique hôte).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Paramètres

</td>
<td style="border: 0;" valign="top">

### Outils de peinture bitmap

</td>
<td style="border: 0;" valign="top">

### Connecteurs de sortie

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Paramètres

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Détermine le type de sortie du nœud, à retourner en couleur ou en niveaux de gris. |
| <b>Chemin de ressource PKG</b> *Chaîne* | Chemin d&#39;accès à la [ressource Bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) référencée par le nœud.   Il est recommandé de ne pas taper manuellement, mais de copier une ressource de l&#39;explorateur et de la coller dans le champ de texte du paramètre, ou de glisser-déposer une ressource bitmap directement de l&#39;[Explorateur](../../../../interface/the-explorer-window/the-explorer-window.md) sur le nœud Bitmap dans le graphique. |
| <b>Méthode de redimensionnement</b> *Nombre entier* | Méthode de rééchantillonnage à utiliser lors de la mise à l’échelle supérieure ou inférieure d’un bitmap :<ul data-preserve-html="true"> <li data-preserve-html="true"><i>étire lisse :</i> appliquez [du filtrage bilinéaire](../../../../glossary/glossary.md) pour effectuer une interpolation sur les pixels source de l&#39;image étirée.</li> <li data-preserve-html="true"><i>étire le plus proche :</i> Étirez l&#39;image et utilisez la couleur du pixel source le plus proche telle quelle.</li> </ul> |

## Outils de peinture bitmap

Les bitmaps peuvent être modifiés dans Designer. En savoir plus sur les outils de modification dans [cette section](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris/Couleur* |  |

## Exemples

*Bientôt disponible.*
