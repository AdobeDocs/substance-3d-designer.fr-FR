---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor-simple.html"
breadcrumb-title: ''
description: Utilisez le nœud Simple du processeur de Vertex de tracés pour traiter les vertex de tracés avec des options de transformation simplifiées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor Simple
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processeur de Vertex Paths Simple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Processeur de Vertex Paths Simple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/paths-vertex-processor-simple-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique une transformation sur la position des sommets de l&#39;entrée <b>Tracés</b>.

1. Modifier la fonction du paramètre <b>Fonction par sommet</b> ;
1. Utilisez un nœud <b>Get Flottant 2</b> dans la variable *vertex.pos* ;
1. Effectuez certaines opérations sur cette valeur (par exemple, multipliez-la pour mettre à l’échelle les tracés) ;
1. Définissez le résultat de votre calcul en tant que sortie.

</td>
</tr>
</table>

Vous pouvez utiliser des images d&#39;entrée et les échantillonner à partir de la fonction. Vous devez d&#39;abord connecter une entrée pour pouvoir l&#39;échantillonner à partir de la fonction. (Attention, la première entrée est *Image 1* !)\
Vous pouvez également accéder aux variables *vertex.corner* (bool) et *path.id* (float).

>[!TIP]
>
> Pour les utilisateurs avancés, la [spécification de format des chemins](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) explique comment les données des chemins sont codées dans des images couleur et fournit des conseils pour manipuler ces données directement.

>[!NOTE]
>
> Voir aussi [Processeur de Vertex Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre nœud de traitement de tracé. |
| <b>Entrée #</b> <i>Couleur/Niveaux De Gris</i> | Entrées pour les images qui doivent être échantillonnées dans la fonction de paramètre <b>Fonction par sommet</b>. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Les tracés transformés. Vous pouvez utiliser [Prévisualiser les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) pour vous faire une idée de ce que le résultat représente, utiliser un autre nœud de traitement des tracés ou l&#39;entrer dans un [Tracés de la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour continuer à le traiter en tant que splines. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Nombre d&#39;entrées d&#39;image</b> <i>Nombre entier</i> | Nombre de connecteurs d&#39;entrée <b>Entrée #</b> visibles pour connecter des images qui doivent être échantillonnées dans la fonction de paramètre <b>Fonction par sommet</b>.<br>Une fois que vous avez terminé de configurer tous les échantillons souhaités, vous pouvez masquer les épingles inutilisées en réduisant la valeur de ce paramètre à 0.<br>Si vous avez besoin de plus d&#39;entrées, utilisez plutôt le [processeur de Vertex Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). |
| <b>Fonction par sommet</b> <i>Float2</i> | Fonction appliquée à chaque sommet. Doit renvoyer la nouvelle position du sommet.<br>Consultez la section <b>Description</b> de cette page pour plus d&#39;informations. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/PathsVertexProcessor-Demo2.gif "Exemple de nœud 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
