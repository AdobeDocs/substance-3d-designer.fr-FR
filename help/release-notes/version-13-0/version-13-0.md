---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/release-notes/version-13-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 13.0 pour en savoir plus sur les nouveaux nœuds, la Substance Engine 9.0 et les nœuds de portail.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 13.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1671'
ht-degree: 2%

---


# Version 13.0

Cette version 13.0.0 de Substance 3D Designer apporte beaucoup d’amour aux artistes matériau, avec une énorme quantité de nouveaux nœuds, la Substance Engine 9.0 introduisant des boucles pour la première fois et avec un grand ajout au graphe : le nœud portal. Et afin de plaire à plus d&#39;utilisateurs, nous introduisons un tout nouvel écran d&#39;accueil et fournissons des langues supplémentaires.

Comme indiqué dans la version précédente, cette version ne prend plus en charge les Graphes Substance models : cela signifie que vous ne pouvez plus ouvrir, modifier ou exporter ces graphes dans Designer. Vous trouverez toutes les raisons pour lesquelles nous avons pris cette décision dans ce [post](https://community.adobe.com/t5/substance-3d-designer-discussions/substance-model-graphs-end-of-life/td-p/13693731)sur notre forum de communauté.

*Date de publication : 6 juin 2023*

![Matériau à l’aide de tracés](version-13-0.resources/version-13-0-01.png "Matériau à l’aide de tracés")

*Illustration de [Celine Dameron](https://www.artstation.com/cline)*

## Nouveau contenu

Cette version 13.0 apporte beaucoup de nouveau contenu. Vous y trouverez principalement deux nouvelles collections de nœuds : les outils Outils spline et Tracé.

* Les [Outils spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md) sont une collection de nœuds permettant de générer et d&#39;ajuster des splines, ainsi que de les utiliser pour le mappage, la diffusion ou la déformation d&#39;images.
* Les [outils de tracé](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-tools.md) sont un autre ensemble de nœuds à extraire, sous la forme d&#39;une liste de segments, des contours d&#39;un masque, puis à les modifier et à les améliorer.

Tous ces nœuds offriront beaucoup de possibilités et ils auront certainement beaucoup d&#39;applications créatives. Consultez la section sur l&#39;[utilisation des tracés et des Outils spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/working-with-path-and-spl/working-with-path-and-spline-tools.md) pour découvrir les concepts importants à prendre en compte afin de vous familiariser avec cet ensemble d&#39;outils.

![Matériau à l&#39;aide de splines](version-13-0.resources/version-13-0-02.png "Matériau à l&#39;aide de splines")

*Illustration de [Louise Melin](https://www.artstation.com/troglodette)*

### Outils Spline

Les nouveaux nœuds dédiés aux splines peuvent être divisés en quatre catégories :

#### Créer

La première catégorie est bien sûr celle qui génère les splines :

* [Spline cubique](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md) : à partir de deux points et de deux tangentes ;
* [Poly quadratique spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) : à partir d&#39;un ensemble de points ;
* [Cercle spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-circle/spline-circle.md) : suivi d&#39;une forme circulaire.

Vous pouvez également créer des <b>ponts </b> entre les splines afin d&#39;avoir un ensemble complet de splines entre [2 splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines/spline-bridge-2-splines.md) ou [N splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline Cubique](version-13-0.resources/version-13-0-03.gif "Spline Cubique")

</td>
<td style="border: 0;" valign="top">

![Poly Quadratique Spline](version-13-0.resources/version-13-0-04.gif "Poly Quadratique Spline")

</td>
<td style="border: 0;" valign="top">

![Cercle spline](version-13-0.resources/version-13-0-05.gif "Cercle spline")

</td>
<td style="border: 0;" valign="top">

![Liste des ponts splines](version-13-0.resources/version-13-0-06.gif "Liste des ponts splines")

</td>
</tr>
</table>

#### Assembler

Dans certains cas, vous devrez traiter plusieurs splines comme une seule entité. Vous aurez donc besoin d&#39;outils pour gérer un ensemble de splines. La [liste de fusion de splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md) vous permet de fusionner toutes vos splines en une seule en connectant les extrémités dans l&#39;ordre. Le nœud [Spline Append](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-append/spline-append.md) vous permet d&#39;ajouter une liste de splines à une autre liste et, grâce au nœud [Spline Select](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-select/spline-select.md), vous pouvez filtrer et sélectionner des splines spécifiques à partir d&#39;une liste donnée.

#### Modifier

Nous fournissons également des outils pour retravailler et ajuster vos splines. Vous trouverez un nœud pour appliquer une [transformation 2D](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-2d-transform/spline-2d-transform.md), comme une rotation, une translation, une échelle et une autre à la [déformation](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-warp/spline-warp.md)<b> </b>la forme et deux autres nœuds pour modifier le [thickness](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-thickness/spline-sample-thickness.md)<b> </b>ou l&#39;[height](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-height/spline-sample-height.md) des splines.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Transformation 2D spline](version-13-0.resources/version-13-0-07.gif "Transformation 2D spline")

</td>
<td style="border: 0;" valign="top">

![Déformation de la spline](version-13-0.resources/version-13-0-08.gif "Déformation de la spline")

</td>
<td style="border: 0;" valign="top">

![Thickness d&#39;échantillon spline](version-13-0.resources/version-13-0-09.gif "Thickness d&#39;échantillon spline")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

#### Rendu

La dernière catégorie est celle qui permet de créer la forme ou le motif final en fonction de vos splines. La première idée qui vous viendra à l&#39;esprit sera de reproduire une forme donnée le long de la spline : le nœud [Dispersion sur la spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md) vous permet de le faire, avec beaucoup de paramètres pour contrôler parfaitement la répartition (rotation, mise à l&#39;échelle, décalage, couleurs, masques, etc.).

Merci pour le [remplissage spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-fill/spline-fill.md)<b> </b>nœud, vous pouvez facilement créer un motif à partir d&#39;une spline fermée. Et si vous souhaitez mapper n&#39;importe quelle texture sur vos splines, avec un degré élevé de contrôle et de précision, le nœud [Mappeur de splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md) est fait pour vous !

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dispersion en niveaux de gris spline](version-13-0.resources/version-13-0-10.gif "Dispersion en niveaux de gris spline")

</td>
<td style="border: 0;" valign="top">

![Remplissage spline](version-13-0.resources/version-13-0-11.gif "Remplissage spline")

</td>
<td style="border: 0;" valign="top">

![Couleur du mappeur de spline](version-13-0.resources/version-13-0-12.gif "Couleur du mappeur de spline")

</td>
<td style="border: 0;" valign="top">

![Mappeur de flux spline](version-13-0.resources/version-13-0-13.gif "Mappeur de flux spline")

</td>
</tr>
</table>

### Outils Path

Le nœud [Masquer sur tracés](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) vous permet d&#39;extraire la bordure d&#39;un motif en niveaux de gris, sous la forme d&#39;une liste de segments.

Vous pouvez ensuite traiter ces tracés avec les nœuds [Transformation 2D du tracé](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md) ou [Déformation des tracés](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) afin de les ajuster en fonction de vos besoins.  Et grâce au nœud [Tracés vers spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md), vous pouvez convertir votre tracé en spline, et ainsi profiter de tous les nœuds dédiés aux splines mentionnées précédemment, comme la diffusion.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Placer le masque sur les tracés](version-13-0.resources/version-13-0-14.gif "Placer le masque sur les tracés")

</td>
<td style="border: 0;" valign="top">

![Placer le masque sur les tracés 2](version-13-0.resources/version-13-0-15.gif "Placer le masque sur les tracés 2")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

Et pour vous aider à apprendre tous ces nouveaux nœuds, nous avons publié deux nouveaux tutoriels :

* [Présentation des nœuds splines](https://www.adobe.com/go/designer-tutorial-splines)
* [Présentation des nœuds de chemin d’accès](https://www.adobe.com/go/designer-tutorial-paths)

## Nouvelle Substance Engine v9

Tous les nouveaux nœuds répertoriés ci-dessus sont fondés sur la nouvelle version de la Substance Engine de données et ils tirent pleinement parti de sa nouvelle fonctionnalité principale : <b>boucles</b>.

Les boucles sont destinées à être utilisées uniquement à l&#39;intérieur des [graphiques de fonction de Substance](../../function-graphs/function-graphs.md). Vous êtes plus susceptible de les implémenter dans un [processeur de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), un [Fx-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) ou un [processeur de valeurs](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md). Les boucles vous permettront bien sûr de répéter facilement une fonction plusieurs fois, jusqu’à ce qu&#39;une condition soit respectée. Cela vous aidera à éclaircir beaucoup vos graphiques et à gagner en précision.

Ce [tutoriel](https://www.youtube.com/watch?v=Ggoy8G90oDI)dédié vous aidera à commencer à travailler avec les boucles.

La Substance Engine v9 apporte également les améliorations suivantes :

* Nouveau mode Solide dans l&#39;éditeur de dégradé du nœud [Courbe de transfert de dégradé](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) (c&#39;est-à-dire aucune interpolation)
* Nœud pow() atomique dans les graphiques de fonction de Substance
* Ajout d’options d’habillage de bordure (serrer sur le contour, répéter) dans les nœuds Sampler
* Échantillonnage le plus proche dans les nœuds [Déformation](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) et [Déformation directionnelle](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)

## Nœud de portail

Le nœud [Portal](../../interface/the-graph-view/graph-items/graph-items.md) est une nouvelle extension du nœud [Dot](../../interface/the-graph-view/graph-items/graph-items.md) avec la possibilité de masquer les connexions dans votre graphique.

Grâce à cette fonctionnalité, vous pouvez améliorer la lisibilité du graphique en masquant les connexions très longues et accéder rapidement aux nœuds clés où que vous soyez sur le graphique.

Cette nouvelle fonctionnalité est entièrement expliquée dans ce [tutoriel](https://www.adobe.com/go/designer-tutorial-portals) dédié.

![Nœud de portail](version-13-0.resources/version-13-0-16.gif "Nœud de portail")

## Écran d’accueil

Lorsque vous démarrez Designer, vous savez que vous avez accès à un tout nouvel [écran d&#39;accueil](../../interface/home-screen/home-screen.md), comme celui que vous avez dans d&#39;autres produits Adobe. À partir de cet écran, vous pouvez :

* Créer rapidement un graphique ;
* Consultez la liste de tous les fichiers récemment ouverts dans Designer, avec quelques détails tels que la taille, la date à laquelle il a été modifié pour la dernière fois ou le chemin d’accès complet ;
* Une page de formation où vous pouvez trouver des liens vers des ressources de formation, telles que des tutoriels pour vous présenter les nouvelles fonctionnalités ou découvrir des conseils rapides ;
* Liens directs vers l’écran Nouveautés, l’écran À propos, le site Web Substance 3D, le forum de la communauté d’assistance, etc.

![Écran d’accueil - Accueil](version-13-0.resources/version-13-0-17.png "Écran d’accueil - Accueil")

![Écran d’accueil - Formation](version-13-0.resources/version-13-0-18.png "Écran d’accueil - Formation")

## Nouvelles langues

Cette version comprend trois langues supplémentaires :

* espagnol (Espagne);
* Italien (Italie);
* Portugais (Brésil).

Pour rappel, si vous souhaitez modifier la langue dans Designer, il vous suffit d&#39;accéder aux [Préférences](../../interface/preferences-window/preferences-window.md) et la liste de toutes les langues disponibles se trouve dans la section Général.

## Notes de mise à jour

### 13.0.0

*(Publié le 6 juin 2023)*

### Ajouté

* [Graph] Nœud du portail
* [Intégration] Nouvel écran d’accueil
* [Content] Nœud spline (cubique)
* [Contenu] Nœud spline (polyquadratique)
* [Contenu] Nœud de cercle spline
* Nœud Liste de points [Contenu]
* [Content] Nœud Spline Bridge (2 splines)
* [Content] Nœud Spline Bridge (List)
* [Content] Nœud Spline Append
* [Contenu] Nœud de sélection de spline
* [Contenu] Nœud de la liste de fusion spline
* [Content] Nœud de transformation 2D spline
* [Contenu] Nœud de déformation de spline
* [Content] Nœud d&#39;Height d&#39;échantillon spline
* [Content] Nœud de Thickness d&#39;exemple de spline
* [Contenu] Nœud de rendu spline
* [Contenu] Dispersion sur le nœud Couleur de spline
* [Contenu] Dispersion sur le nœud Niveaux de gris spline
* [Content] Nœud Couleur du mappeur de spline
* [Contenu] Nœud Niveaux de gris du mappeur de spline
* [Content] Nœud de couleur du mappeur de pont spline
* [Content] Nœud Niveaux de gris du mappeur de pont spline
* [Content] Nœud du mappeur de flux spline
* [Contenu] Nœud de couleur du mappeur UV
* [Contenu] Nœud Niveaux de gris du mappeur UV
* [Contenu] Nœud Tracés vers splines
* [Contenu] Nœud Masques vers tracés
* [Contenu] Tracés 2D Transform nodenode
* [Contenu] Tracés Nœud Polygone
* [Contenu] Nœud Chemins d’accès d’aperçu
* [Contenu] Nœud Déformation des tracés
* [Contenu] Nœud de sélection des tracés
* [Content] Nœud Processeur de sommets de tracés
* [Contenu] Processeur de sommets de tracés Nœud simple
* [Contenu] Quad Transform sur le nœud de chemin
* [Contenu] Occlusion ambiante avec lancer de rayon v2
* [Contenu] Courbure Lancer De Rayon Normal v2
* [Contenu] Ombres vectorisées avec rayon v2
* [Moteur] Mise à jour vers la version 9
* [Moteur] Nœud de boucle dans les graphiques de fonction
* [Moteur] Ajouter le mode solide au dégradé
* [Moteur] Nœud Pow() atomique dans le graphique de fonctions
* [Moteur] Ajout d’options d’habillage de bordure (serrage sur le bord/répétition) dans le nœud Sampler
* [Moteur] Échantillonnage le plus proche dans le nœud Déformation et Déformation directionnelle
* [Moteur] Ajout d’un mode « alpha pénétrant » au filtre Netteté pour les entrées de couleur
* [Engine] FxMap : morphlet de l&#39;hémisphère
* [Engine] Opérations Get/Set atomiques dans les graphiques de fonction
* [Moteur] Fonctions : utiliser la fonction précise de log/log2/exp, 2pow - Unifier les fonctions entre le cuiseur et le moteur
* [Moteur] Ajoutez un paramètre « décalage d’intensité » au filtre Déformation directionnelle
* [API] Prise en charge de la gestion des paramètres prédéfinis pour la composition de graphiques
* [Fonctions] Modification du nom d&#39;entrée des fonctions nœuds atomiques
* [Localisation] Ajouter Portugais (Brésil), Italien (Italie) et Espagnol (Espagne)
* [Localisation] Respectez la règle « Langue (Pays) » dans la liste des langues
* [Paramètres prédéfinis] Désactiver les panneaux « Aperçu » et « Paramètres prédéfinis » dans les propriétés du graphique lors de l’utilisation de l’édition contextuelle
* [Graphique des modèles de Substance] Fin de la prise en charge des graphiques des modèles de Substance

### Correctifs

* [Vue 3D] L’affichage des chaînes longues dans les statistiques de scène est coupé (macOS uniquement)
* Le module [API] &#39;structure::Structure&#39; est toujours inclus dans la référence API
* [API] Les nœuds de point dans les graphiques MDL n&#39;ont aucune définition ni propriété
* [API] Comportement incorrect lors de la définition du paramètre des nœuds de fonction
* [Contenu] 3D Voronoi et 3D voronoi fractal nodes génèrent un avertissement de cuisson
* [Moteur] Le paramètre « Décalage de la carte d’intensité » n’a aucun effet sur les données en niveaux de gris dans le moteur SSE2
* [Explorer] L’e/s du graphique peut être supprimée
* [Graphique] Le bitmap est ignoré lorsqu’il est utilisé dans des instances
* [Graphique] Position de nœud de point incorrecte lors de la création d&#39;un nœud à partir d&#39;un nœud
* [Graphique] Focus incorrect dans la boîte de dialogue « Exposer le paramètre » lors de l’utilisation de la touche « Entrée »
* [Graphique] Résultat incorrect dans la numérisation d’histogramme avec un bitmap dans l’édition du contexte
* [Localisation] Correction de divers problèmes d’écrêtage
* [Paramètres] Blocage lors de la suppression d’un paramètre d’entrée
* [Publish] Les graphiques dans les dossiers sont déplacés à la racine dans le package publié
* [Ressources] Blocage lors de la mise à jour d’une ressource chargée sur le disque
* [VisibleIf] Correction de la régression dans l’évaluation de la visibilité conditionnelle
