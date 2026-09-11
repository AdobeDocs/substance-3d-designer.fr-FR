---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: Importez et utilisez des images vectorielles de SVG en tant que ressources dans Substance 3D Designer pour la création procédurale de matériaux.
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ressource d’images vectorielles (SVG)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 65a0ec6dc38e7595406c0c531be72ad1670dfb86
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 2%

---


# Ressource d’images vectorielles (SVG)

Substance 3D Designer prend en charge un nombre limité d’Images vectorielles, via le format Images vectorielles évolutives. Les fichiers du SVG peuvent être importés sous forme de ressources de différentes manières et utilisés comme ressources pour vos graphes.

Les fichiers de SVG [peuvent être créés ou modifiés via le nœud de SVG atomique](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md), ils peuvent également être créés par [le baker de SVG UV](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg).

>[!NOTE]
>
> Les fichiers Adobe Illustrator (**.ai**) *ne sont pas* actuellement pris en charge.

## stockage SVG

Le stockage dans un SVG dépend de s’ils sont liés ou importés. Les fichiers de SVG importés sont incorporés dans le fichier SBS, ne nécessitent [aucun fichier externe tel que des bitmaps](../../resources/bitmap-resource/bitmap-resource.md) et peuvent être modifiés à l&#39;aide des [outils d&#39;édition vectorielle](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Attributs du SVG

Les ressources de SVG d’un package ont un certain nombre d’attributs que vous pouvez personnaliser. La plupart des attributs n’ont pas d’objectif principal et sont destinés aux filtres de bibliothèque, mais une minorité affecte la qualité du rendu.

| Nom de l’attribut | Objectif |
| --- | --- |
| Identifiant | Utilisé pour référencer la ressource SVG dans un package, doit être unique. |
| Chemin d&#39;accès au fichier | Chemin d&#39;accès sur le disque du fichier SVG référencé par la ressource. |
| Description | Description affichée dans les info-bulles de l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md) et de la [Bibliothèque](../../interface/the-library/the-library.md) pour cette ressource. |
| Catégorie | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Libellé | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Auteur | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| URL de l&#39;auteur | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Balises | Utilisé pour [trier et organiser la ressource](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) dans la [bibliothèque](../../interface/the-library/the-library.md). |
| Données utilisateur | Données supplémentaires facultatives, non utilisées sur les images vectorielles. |
| Afficher dans la bibliothèque | Détermine si la ressource SVG doit être masquée dans [la vue Bibliothèque](../../interface/the-library/the-library.md). |
| qualité des Images vectorielles | Affecte la qualité de rendu. La plage n&#39;est pas linéaire et la meilleure qualité est atteinte à 0,5. |

## création de mots de SVG

Étant donné que seul un ensemble limité de fonctionnalités est pris en charge, le SVG de création est contraint.

En général, ce qui suit est vrai :

* Seules des formes et des tracés simples primitifs sont garantis pour dessiner correctement ;
* Le contour est pris en charge, mais ne donne qu’un contour d’une largeur de 1 pixel et le style du contour est ignoré ;
* Les styles de ligne en pointillés vont définitivement rompre ;
* Le texte doit être converti en tracés/contour à rendre ;
* [Les chemins composés](https://helpx.adobe.com/ie/illustrator/desktop/manage-objects/reshape-transform-objects/create-compound-paths.html) ne sont pas pris en charge ;
* Les fonctionnalités avancées telles que les dégradés ne sont pas prises en charge ;
* Les éléments de style pour les propriétés CSS ne sont pas pris en charge.

## Options d’exportation recommandées

Les options d’exportation sont légèrement différentes pour chaque application :

### Adobe Illustrator

[Illustrator](https://www.adobe.com/products/illustrator.html) offre un meilleur contrôle sur les exportations de votre SVG si vous tenez compte des options suivantes.

* Utilisez uniquement <b>Enregistrer sous</b>, *pas* Exporter sous !
* Le <b>profil de SVG</b> n&#39;a pas beaucoup d&#39;importance, bien que le profil Tiny utilise (principalement) par défaut des paramètres qui sont définitivement corrects ;
* <b>Les polices</b> doivent être définies sur <b>Convertir en contour</b> pour fonctionner ;
* Les <b>propriétés CSS</b> ne doivent *pas* être définies sur Éléments de style, toutes les autres options fonctionneront ;
* Décochez <b>Conserver les fonctionnalités de modification d&#39;Illustrator</b>;
* Décochez <b>Responsive</b>;
* Les contours ne fonctionneront pas bien. Utilisez <b>Objet > Tracé > Vectoriser le contour</b> pour les faire apparaître.

L’image de droite présente les options d’exportation recommandées. Cliquez dessus pour l’afficher en taille réelle.

>[!IMPORTANT]
>
> Les plans de travail peuvent affecter le résultat du fichier de SVG généré. Certains modèles de fichiers Illustrator présentent plusieurs plans de travail.\
> Essayez d’en avoir un seul, correctement recadré, et de le faire sélectionner dans la fenêtre Plan de travail lors de l’enregistrement en tant que SVG.

![Options d’exportation Illustrator SVG](vector-graphics-svg-resource.resources/svg-export-options-ai.jpg "Options d’exportation Illustrator SVG"){width="512px"}

### Inkscape

Inkscape est enregistré en mode natif en tant que SVG, mais avec moins de contrôle sur le format de fichier. Les fichiers Inkscape fonctionnent principalement en mode natif dans l’application, mais avec certaines limitations :

* Les contours ne s’affichent que sur une largeur de 1 px dans Substance 3D Designer. Pour les faire fonctionner, utilisez <b>Tracé > Contour sur tracé</b>.
* Le texte ne fonctionnera pas. Utilisez <b>Chemin > Objet vers chemin</b> pour que le texte fonctionne.

### Adobe Photoshop

Photoshop a un exporteur de SVG très limité (<b>Fichier > Exporter > Exporter sous..</b>) qui n’est actuellement pas en mesure de produire des résultats corrects pour Substance 3D Designer. Vous pouvez obtenir vos informations de forme et de tracé, mais le style est toujours enregistré en tant qu’éléments, ce qui est incompatible.

Il peut être utilisé pour les masques de forme simples en noir et blanc, où une solution consiste à extraire l&#39;Alpha du SVG à l&#39;aide de la [division d&#39;Alpha](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md).

Vous pouvez également [importer](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) un SVG exporté par Photoshop, ce qui vous permet de [modifier les informations de style en mode natif dans l’application.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)
