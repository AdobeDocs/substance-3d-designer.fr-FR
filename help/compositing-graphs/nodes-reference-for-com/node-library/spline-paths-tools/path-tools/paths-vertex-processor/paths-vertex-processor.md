---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: Utilisez le nœud Processeur de Vertex de tracés pour transformer et manipuler des vertex de tracés avec des options avancées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processeur de Vertex des chemins d’accès
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---


# Processeur de Vertex des chemins d’accès

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](paths-vertex-processor.resources/paths-vertex-processor-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique une transformation sur la position des vertex de l&#39;entrée <b>Tracés</b>.

Le nœud doit être utilisé comme suit :

1. Modifier la fonction de paramètre <b>Fonction par sommet </b>;
1. Utilisez les nœuds <b>Get Flottant 2</b> à acquérir ; les variables *vertex.pos*, *prev.pos* et/ou *next.pos*
1. Effectuez certaines opérations sur ces valeurs (par exemple, multipliez-les pour mettre à l’échelle les tracés) ;
1. Définissez le résultat de votre calcul en tant que sortie.

</td>
</tr>
</table>

Assurez-vous de définir les valeurs <b>vertex précédents consultés</b> et <b>vertex suivants consultés</b> appropriées avant d&#39;interroger *prev.pos* ou *next.pos*\
Vous pouvez également ajouter des images d&#39;entrée et les échantillonner à partir de la fonction. Vous devez d&#39;abord connecter une entrée pour pouvoir l&#39;échantillonner à partir de la fonction. (Attention, la première entrée est *Image 1* !)\
Vous pouvez également accéder aux variables *prev[2].pos* (Flottant 2), *next[2].pos* (Flottant 2), *vertex.corner* (bool) et *path.id* (float).

>[!TIP]
>
> Pour les utilisateurs avancés, la [spécification de format des chemins](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) explique comment les données des chemins sont codées dans des images couleur et fournit des conseils pour manipuler ces données directement.

>[!NOTE]
>
> Voir aussi [Processeur de Vertex Paths Simple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md).

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Liste des chemins d’accès des segments codés. Connectez cette entrée au résultat d&#39;un [masque sur les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou à un autre *nœud de traitement des tracés*. |
| <b>Entrée #</b> <i>Couleur/Niveaux De Gris</i> | Entrées pour les images qui doivent être échantillonnées dans la fonction de paramètre <b>Fonction par sommet</b>. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Tracés</b> <i>Couleur</i> | Les Tracés transformés. Vous pouvez utiliser [Prévisualiser les tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) pour vous faire une idée de ce que le résultat représente, utiliser un autre nœud de traitement des tracés ou l&#39;entrer dans un [Tracés de la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour continuer à le traiter en tant que splines. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Accès aux Vertex précédents</b> <i>Entier</i> | L&#39;utilisation de ce paramètre vous permettra d&#39;obtenir la position du vertex précédent le long du chemin (*prev.pos*) et du vertex précédent (*prev[2].pos*) à l&#39;aide des nœuds <b>Get</b> dans la fonction de paramètre <b>Fonction par sommet</b>. |
| <b>Vertex suivants consultés</b> <i>Entier</i> | L&#39;utilisation de ce paramètre vous permettra d&#39;obtenir la position du vertex suivant le long du chemin (*next.pos*) et du vertex suivant (*next[2].pos*) à l&#39;aide des nœuds <b>Get</b> dans la fonction de paramètre <b>Fonction par sommet</b>. |
| <b>Nombre d&#39;entrées d&#39;image</b> <i>Entier</i> | Nombre de connecteurs d&#39;entrée <b>Entrée #</b> visibles pour connecter des images qui doivent être échantillonnées dans la fonction de paramètre <b>Fonction par sommet</b>.<br>Une fois que vous avez terminé de configurer tous les échantillons souhaités, vous pouvez masquer les épingles inutilisées en réduisant la valeur de ce paramètre à 0. |
| <b>Fonction par sommet</b> <i>Flottant 2</i> | Fonction appliquée pour chaque vertex. Doit renvoyer la nouvelle position de vertex.<br>Consultez la section <b>Description</b> de cette page pour plus d&#39;informations. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 2](paths-vertex-processor.resources/PathsVertexProcessor-Demo2.gif "Exemple de nœud 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
