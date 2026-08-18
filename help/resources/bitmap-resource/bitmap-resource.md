---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: Apprenez à importer, créer et utiliser des bitmaps dans Substance 3D Designer pour créer des textures.
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ressource bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---


# Ressource bitmap

Une ressource bitmap est une ressource contenue dans un pack de Substances. Il est différent du nœud bitmap atomique [. Le nœud bitmap atomique](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) est une représentation spécifique de ce bitmap à l&#39;intérieur[d&#39;un graphique de Substance](../../compositing-graphs/substance-compositing-graphs.md).

Les bitmaps font partie des ressources non graphiques les plus courantes dans Substance 3D Designer. Leur utilisation relève généralement de l’une des catégories suivantes :

* Une map bakée, [créée en interne par Designer](../../bakers/bakers.md) ou en externe par une autre application.
* Texture d’assistant, comme un motif, une texture usure/salissures ou une décalcomanie.
* Un simple masque en niveaux de gris pour la fusion, créé en interne à l&#39;aide du [nœud bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) ou avec une application externe.

## Stockage bitmap

Les bitmaps constituent généralement la plus grande ressource gérée par Designer. C’est pourquoi il est bon que vous compreniez comment Designer gère ces fichiers avec ses deux principaux types de fichiers.

### Dans les fichiers Substance 3D (SBS)

La façon dont les bitmaps sont stockés dans SBS dépend de si vous [liez ou importez-les, assurez-vous de bien connaître le concept au préalable.](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) Les bitmaps importés peuvent être modifiés à l&#39;aide des [outils de peinture bitmap](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

Contrairement aux ressources SVG (images vectorielles), les bitmaps sont toujours stockés en externe, même lorsqu’ils sont créés en tant que nouvelle ressource ou importés. Pour les nouveaux packs de Substances, ils sont conservés en mémoire jusqu’à ce que le fichier .SBS soit enregistré sur le disque. Une fois enregistrées sur le disque, les bitmaps sont stockées dans un dossier */resources* en regard du fichier SBS.

### Dans les ressources Substance 3D (SBSAR)

Dans les [fichiers SBSAR](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html), les bitmaps sont incorporés, ce qui signifie qu&#39;ils ont un impact important sur la taille finale des fichiers SBSAR. Pour en savoir plus sur l’impact sur la taille des fichiers, consultez cette page. Lorsque des fichiers SBSAR [sont publiés](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html), seules les images bitmap utilisées pour calculer la sortie d&#39;un graphique sont incorporées. Toutes les images bitmap inutilisées sont optimisées et exclues du package SBSAR final, sans effet sur la taille du fichier.

## Type de fichier, mode colorimétrique et résolution

Substance 3D Designer peut facilement modifier et réorganiser les données des bitmaps, mais il est préférable de garder à l’esprit les points suivants :

* Définissez vos résolutions pour qu&#39;elles soient conformes à la puissance 2, ce qui signifie que vous devez suivre la taille de texture standard en temps réel comme <b>256, 512, 1024 ,2048,</b> etc. Designer redimensionnera les textures en dehors de cette plage à la résolution correspondante la plus proche. Notez qu’il n’est pas nécessaire qu’elles soient dans des proportions carrées.
* De nombreux types de fichiers sont pris en charge, mais choisissez celui qui convient le mieux à votre cas d’utilisation. La compression <b>sans perte ou même non compressée</b> des types de fichiers tels que PNG ou TGA offrent une meilleure qualité que le JPG ou DDS.
* Assurez-vous de <b>configurer votre mode colorimétrique correctement</b>, selon que vous avez besoin d&#39;une couleur, de niveaux de gris ou d&#39;une couche alpha.

## Attributs bitmap

Les ressources bitmap d’un package possèdent un certain nombre d’attributs que vous pouvez personnaliser. La plupart des attributs n’ont pas d’objectif principal et sont destinés aux filtres de bibliothèque, bien qu’une minorité affecte la taille des fichiers.

| Nom de l’attribut | Objectif |
| --- | --- |
| Identifiant | Utilisé pour référencer la ressource bitmap dans un package, doit être unique. |
| Chemin d&#39;accès au fichier | Chemin d’accès sur le disque de l’image bitmap référencée par la ressource. |
| Description | Description affichée dans les info-bulles [Explorer](../../interface/the-explorer-window/the-explorer-window.md) et [Bibliothèque](../../interface/the-library/the-library.md) pour cette ressource. |
| Catégorie | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Libellé | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Auteur | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| URL de l&#39;auteur | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Balises | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Données utilisateur | Données supplémentaires facultatives, non utilisées sur les bitmaps. |
| Afficher dans la bibliothèque | Détermine si le bitmap doit être masqué dans [la vue Bibliothèque](../../interface/the-library/the-library.md). |
| Format bitmap | Raw ou Jpeg a un grand effet sur la taille des fichiers SBSAR. Consultez nos [directives de réduction de la taille des fichiers](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) pour en savoir plus. |
| Qualité de compression bitmap | N’a d’effet qu’avec la compression Jpeg, et détermine l’équilibre qualité/taille de fichier. |

## Réduction de la taille des fichiers

Consultez la page [Directives de réduction de la taille des fichiers](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) dans la section [Pratiques recommandées](../../best-practices/best-practices.md) pour nos recommandations concernant la réduction de la taille des fichiers des bitmaps incorporés dans [ressources Substance 3D publiées](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) (SBSAR).
