---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: Importez et utilisez des ressources de polices dans Substance 3D Designer pour ajouter du texte et de la typographie à vos matières.
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ressource de police
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Ressource de police

Les ressources de police sont destinées à être utilisées avec le [nœud de texte atomique](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md). Ils vous permettent d’utiliser des polices qui ne sont pas installées sur votre système, en référençant un fichier de polices n’importe où sur le disque.

>[!NOTE]
>
> **Polices dans SBSAR**
> 
> Les polices sont toujours incorporées dans un fichier SBSAR, que ce soit à partir d’une ressource liée ou en utilisant une police installée sur le système. L’avantage de cette méthode est qu’il n’est pas nécessaire de l’installer et que, lors de l’exportation d’un fichier SBS avec des dépendances, vous pouvez être sûr que les fichiers de polices sont fournis.

## Utilisation de ressources de polices personnalisées

* Cliquez avec le bouton droit de la souris sur un pack, puis sélectionnez <b>Lien > Police</b>
* Sélectionnez un fichier .otf ou .ttf.
* Placez un [nœud de texte](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) dans votre [graphique](../../compositing-graphs/substance-compositing-graphs.md).
* Sous la propriété <b>Police </b>, toutes les ressources de police se trouvent en haut de la liste.

Notez que la liste des polices n’est pas automatiquement actualisée avec les propriétés ouvertes. Vous devrez passer à une autre fenêtre de propriété et revenir à un nœud Texte pour voir les polices nouvellement liées.
