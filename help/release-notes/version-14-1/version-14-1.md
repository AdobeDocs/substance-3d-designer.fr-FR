---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-14-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 14.1 pour en savoir plus sur les outils de disposition des nœuds et les nouveaux nœuds Spline et Tracé.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 14.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 14.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 1%

---


# Version 14.1

Cette mise à jour introduit de nouvelles fonctionnalités pour améliorer votre utilisation quotidienne de Substance 3D Designer : des outils de disposition des nœuds pour améliorer rapidement la mise en page de votre graphique, le copier/coller de paramètres pour appliquer un ensemble de paramètres à un autre nœud et une épingle de pixel dans la vue 2D pour suivre un pixel spécifique lors du débogage de votre graphique. Il ajoute également du nouveau contenu, principalement pour compléter les jeux de nœuds Spline et Tracé.

*Date de publication : 14 janvier 2025*

![Dispersions splines sur splines](version-14-1.resources/version-14-1-01.png)

## Mises à jour des splines et des tracés

Les splines et les nœuds de tracé ont été introduits dans la version 13.0, et grâce à vos commentaires, nous avons effectué un ensemble initial d&#39;améliorations. Tout d&#39;abord, nous avons ajouté le nœud [splines de Dispersion sur splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-splines-splines/scatter-splines-on-splines.md), qui répartit les splines le long d&#39;une spline parent, offrant des options similaires à celles d&#39;un nœud de dispersion ordinaire. En outre, le nœud [Masquer les tracés](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) a été amélioré pour donner plus de contrôle sur la position du premier sommet sur le tracé. Nous avons également permis d&#39;introduire le caractère aléatoire dans le nœud [Spline Bridge List](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dispersion de la spline sur l&#39;animation de spline 1](version-14-1.resources/version-14-1-02.gif){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dispersions splines sur splines 2](version-14-1.resources/version-14-1-03.gif){zoomable="yes"}

</td>
</tr>
</table>

## Outils d’alignement des nœuds

Si vous souhaitez conserver un graphique propre et lisible, les [outils d&#39;alignement des nœuds](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md) sont faits pour vous et ont été complètement remaniés ! Il est désormais possible d&#39;espacer uniformément les nœuds (horizontalement ou verticalement) et l&#39;alignement des nœuds évite tout chevauchement en les empilant soigneusement. Cerise sur le gâteau : les deux fonctionnalités prennent en compte la taille réelle des nœuds !

![Aligner les nœuds](version-14-1.resources/version-14-1-04.gif){zoomable="yes"}

## Copier/coller les paramètres

Il est désormais possible de [copier les paramètres d&#39;un nœud et de les coller sur un autre](../../compositing-graphs/manage-parameters/manage-parameters.md), afin que tous les paramètres correspondants dans le nœud cible soient mis à jour vers les valeurs du nœud source. Ceci est très utile si, par exemple, vous souhaitez reporter les paramètres d’un nœud de couleur sur sa version en niveaux de gris, ou inversement. (par exemple, le nœud Tile Sampler)

## Épingler un pixel dans la vue 2D

Le nouvel [outil Sampler des couleurs](../../interface/2d-view/color-sampler/color-sampler.md) dans la vue 2D vous permet de suivre la valeur d&#39;un pixel sélectionné en y déposant une épingle. Cela permet de s’assurer que les informations d’un même pixel sont toujours affichées sur plusieurs nœuds d’un graphique. Ouvrez le panneau Informations pour accéder à l’outil et l’essayer !

![Échantillonneur de couleur : utilisation de l&#39;outil](version-14-1.resources/version-14-1-05.gif "Échantillonneur de couleur : utilisation de l&#39;outil"){width="640px" zoomable="yes"}

## Améliorations de la recherche

L&#39;outil [Node Finder](../../interface/the-graph-view/node-finder/node-finder.md) a été légèrement amélioré :

* Vous pouvez désormais activer un mode récursif pour une recherche plus approfondie ;
* Le mode flou peut être désactivé si vous souhaitez rechercher un terme exact ;
* Le focus est automatiquement mis sur le champ de recherche lors de l&#39;activation de l&#39;outil de recherche de nœuds ;
* La disposition de la barre d’outils a été repensée pour économiser de l’espace.

![Barre d&#39;outils de recherche](version-14-1.resources/version-14-1-06.png){width="640px"}

## Vidéos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![splines de dispersion vidéo sur les splines](version-14-1.resources/version-14-1-07.png)](https://www.youtube.com/watch?v=aUUWV1dYQdI)

</td>
<td style="border: 0;" valign="top">

[![fonctionnalités de l’expérience utilisateur vidéo](version-14-1.resources/version-14-1-08.png)](https://www.youtube.com/watch?v=LwexybAEjaI)

</td>
</tr>
</table>

## Notes de mise à jour

### 14.1.0

*(Publié le 14 janvier 2025)*

### Ajouté

* [Vue 2D] Ajout d’un affichage en pixels épinglés dans le panneau Informations
* [API] Afficher la taille de la zone des nœuds dans la scène Vue graphique
* [Contenu] « Fusion d’Height de matière » : ajouter une sortie « Masque d’Height »
* [Contenu] &#39;Processeur de sommets de tracé&#39; : utilisez le bouton &#39;Modifier la fonction&#39; pour le paramètre &#39;Fonction par sommet&#39;
* [Contenu] Niveaux automatiques : nettoyage des paramètres inutilisés, ajustement des libellés et de l’info-bulle
* [Contenu] Masquage sur tracés v2
* [Content] Nouvelle moyenne du nœud de moindre écart (MLV)
* [Contenu] Nouveau nœud de filtre médian
* [Contenu] Quantifier la couleur : ajoutez une option de filtrage « Au plus près »
* [Content] Liste des ponts splines : ajout aléatoire de paramètres de décalage de spline
* [Contenu] Outils spline : nouveau nœud spline (quadratique)
* [Contenu] Triangle Grid : modification de la méthode de triangulation et utilisation de boucles
* [Contenu] Nouvelles splines de Dispersion sur le nœud Splines
* [Cooker] Exposer le paramètre de base « Pixel ratio » comme variable statique « $pixelratio »
* [CrashReport] Intégrer une nouvelle fenêtre de rapport d’incident
* [Engine] Ajoutez la version Vulkan/Metal du moteur de fusion
* [Graphique] Mode matière : permet à la connexion d’entrer des données sans utilisation lorsqu’un seul lien est sélectionné
* [Graphique] Lien de matériau : autorise les connexions standard lorsque la connexion n’est pas ambiguë.
* [Graphique] Outils d’alignement des nœuds : ajoutent des distributions horizontales/verticales, des alignements gauche/droite/haut/bas et prennent en charge les nœuds empilés
* [Bibliothèque] Correction de la couleur du texte dans les menus contextuels
* [Paramètres] Copie des paramètres d&#39;un nœud vers un autre
* [Propriétés] « Tout réinitialiser » : Supprimer la fenêtre contextuelle de confirmation
* [Ressources] Définissez le format sur « Tous les formats » dans la boîte de dialogue « Lier Bitmap »
* [Search] Ajouter un moyen d&#39;activer/désactiver un mode récursif
* [Search] Ajouter un moyen d&#39;activer/désactiver la recherche floue
* [Recherche] Toujours afficher et définir le focus sur le champ de terme de recherche lors de l’activation du Finder de nœuds à l’aide de son raccourci clavier
* [Rechercher] Retravailler l’option de filtre
* [Raccourcis] Autoriser l’attribution des touches « V », « H » et « S »
* [Tiers] Mise à niveau vers Qt 6.5.7
* [UX] Les boîtes de dialogue modales ne doivent pas être réduites au minimum
* [UX] Supprimer le défilement horizontal sur la boîte de dialogue d’alerte

### Correctifs

* [Contenu] Biseau : le format normal n’est pas affecté par la préférence globale
* [Contenu] Le nœud de couleur à masquer n’ignore pas les caractères alpha
* directional distance [Contenu] : résultat incorrect lorsque l’entrée a un rapport d’image vertical
* Mappeur de Flood Fill [Content] : Avertissement déclenché pour la variable absente
* [Contenu] Histogramme Calculer : le résultat est 16 fois supérieur à ce qu’il devrait être
* [Contenu] RT caustics ne fonctionne pas en résolution non carrée
* [Content] Liste des ponts splines : résultat incorrect lors de l&#39;utilisation des décalages de début/fin
* [Content] Spline Select : la quantité de spline de sortie peut être supérieure à la quantité de spline d&#39;entrée
* [Content] La déformation spline produit un résultat noir avec le moteur SSE
* Triangle Grid [Contenu] : le motif ne s’affiche pas correctement
* Triangle Grid [Contenu] : la mosaïque est rompue dans un cas spécifique
* [Données] Blocage lors de la modification de l’identifiant d’entrée du graphique dans un cas spécifique
* [Graphique de fonction] Les valeurs longues apparaissent chevauchées sur les nœuds &#39;Float&#39;
* [Fx-Map] Blocage lors de l’affichage des propriétés du nœud de quadrant
* [Graphique] [UDIM] Avoir une barre de défilement dans la liste UDIM donne 1..1 1..2 entrées
* [Graphique]&#x200B;[Raccourcis] Le nœud créé à l’aide d’un raccourci n’est pas placé sur le lien existant après la duplication du nœud
* [Propriétés] Affichage incorrect des paramètres lorsque la valeur n’est pas valide
* [Publish] Les dépendances réciproques entraînent une boucle infinie lors de la publication d’un pack
* [Publish] Échec silencieux lors de l’utilisation de l’action « Publish » sur un pack avec une dépendance déchargée
* [UI] Le widget « Taille du gabarit » ne s’affiche pas correctement lorsqu’il est développé et peut bloquer l’interface (macOS uniquement)
* [UI] Dans certains cas, la fenêtre principale se trouve derrière d’autres applications (Windows uniquement)
