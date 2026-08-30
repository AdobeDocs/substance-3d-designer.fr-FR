---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-15-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 15.1 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 15.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---


# Version 15.1

La Substance Designer 15.1 offre une fenêtre de création de graphique entièrement repensée avec un accès direct à l’échantillon, des nœuds de bruit améliorés pour de plus grandes possibilités de création, des catégories organisées dans le menu des nœuds, et bien plus encore.

*Date de publication : 11 décembre 2025*

![Bannière Designer 15.1](version-15-1.resources/bannerweb.png)

## Amélioration de la création de graphiques

Dans cette version, la [fenêtre de création de graphique](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) a été <b>entièrement repensée</b> pour améliorer l&#39;expérience utilisateur initiale dans Substance 3D Designer. L’objectif principal de cette mise à jour est de rationaliser le processus de sélection des modèles, ce qui permet aux utilisateurs d’identifier efficacement le modèle le mieux adapté à leurs besoins.

Les vignettes offrent des <b>références visuelles</b> instantanées pour les types de matériaux prévus, tandis que les info-bulles détaillées fournissent toutes les informations pertinentes. Pour une meilleure organisation, les modèles sont désormais classés dans des <b>catégories</b> spécifiques, telles que les matériaux, les filtres et le traitement de numérisation.

Bien que l’interface principale ait été mise à niveau, les utilisateurs continuent d’avoir accès aux affichages précédents, y compris les options de liste, de packages et de répertoires.

[En savoir plus](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)

![reconcevoir la nouvelle fenêtre graphique](version-15-1.resources/newgraph.png){zoomable="yes"}

## Échantillons incorporés

Avec le lancement de notre fenêtre de création de graphiques repensée, nous avons ajouté une variété de [<b>matériaux d&#39;exemple</b>](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) directement dans le logiciel. Cette amélioration fait suite à votre demande d&#39;un meilleur accès aux ressources d&#39;apprentissage.

![Nouvelle fenêtre de création de graphique pour les échantillons](version-15-1.resources/GraphSample.png){zoomable="yes"}

Pour répondre à ce besoin, nous avons inclus des échantillons de matériaux tels que les tissus (y compris le cuir et le satin), le bois, le métal, le plastique, la céramique et plus encore. Ces exemples ont pour but de vous aider à démarrer vos projets en toute simplicité et à vous familiariser avec les principaux nœuds de la famille disponibles dans Substance 3D Designer

Chaque graphique est <b>annoté</b>, soigneusement organisé et contient un nombre minimal de nœuds pour le rendre aussi facile à comprendre que possible.

Vous pouvez accéder aux échantillons dans la catégorie « Échantillons de matière » lors de la création d’un graphique de Substance, ou directement depuis l’écran d’accueil à l’aide du bouton pratique « Accéder aux échantillons ».

Outre ces documents fondamentaux, nous avons également fourni des <b>échantillons avancés</b> pour montrer comment utiliser plus efficacement les fonctionnalités de <b>FX-map et de processeur de pixels</b>.

[En savoir plus](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)

![échantillon de bois dans substance designer](version-15-1.resources/samplegraph.png){zoomable="yes"}

## Nouveaux bruits

Les bruits jouent un rôle essentiel dans la majorité des graphiques. C’est pourquoi nous nous sommes concentrés sur plusieurs améliorations clés de cette version, afin d’en améliorer la fonctionnalité et la convivialité.

Avec cette mise à jour, nous avons introduit <b>une meilleure prise en charge des scénarios sans carrelage</b>, en veillant à ce que les modèles de bruit se comportent comme prévu sans carrelage obligatoire. Auparavant, les nœuds de bruit étaient soit forcés de mosaïquer, soit produisaient des résultats incorrects lorsque la mosaïque était désactivée.

La plupart des bruits incluent désormais de <b>nouveaux paramètres</b>, ce qui offre aux utilisateurs un meilleur contrôle créatif. Ces options supplémentaires permettent aux auteurs de graphiques d’affiner l’apparence et le comportement du bruit dans leurs workflows.

Enfin, la profondeur de bits <b>n&#39;est plus verrouillée en mode 16 bits</b>. Vous pouvez désormais remplacer le paramètre de profondeur de bit sur des instances de nœud individuelles, ce qui vous permet d’obtenir des détails plus détaillés et une plage dynamique plus élevée si nécessaire, ou d’optimiser vos graphiques pour les performances.

Consultez la liste complète des bruits mis à jour dans les [notes de mise à jour](#release-notes) ci-dessous.

Exemples : [Cellules 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) [Nuages 2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md) [Rayures directionnelles](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-scratches/directional-scratches.md) [Bruit d&#39;humidité 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

![bruit de désordre directionnel](version-15-1.resources/directionaldisorder.gif){zoomable="yes"}

## Hiérarchie dans le menu des nœuds

Pour relever le défi de localiser des nœuds spécifiques dans la vaste bibliothèque, nous avons introduit des catégories dans le menu Nœud.

Le grand nombre de nœuds disponibles peut rendre difficile la recherche rapide du nœud souhaité. Pour rationaliser ce processus, un nouvel attribut [<b>Groupe</b>](../../compositing-graphs/graph-parameters/graph-parameters.md) a été implémenté au niveau du graphique. Lorsque cet attribut est défini, il est utilisé pour organiser et trier les résultats de la recherche.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![recherche de nœud avec catégorie 1](version-15-1.resources/search1-2.png){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![recherche de nœud avec catégorie 2](version-15-1.resources/search2.png){zoomable="yes"}

</td>
</tr>
</table>

## Sortie par défaut

Lorsqu&#39;un nœud a plusieurs [sorties](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), il n&#39;est pas possible de les afficher simultanément dans la vue 2D ou en tant que miniature de nœud. La directive dominante dans de tels scénarios est d&#39;utiliser la première broche connectée ou, si aucune broche n&#39;est connectée, la première sortie par défaut.

Cependant, cette approche peut ne pas toujours donner des résultats optimaux. Par exemple, dans certains nœuds Spline, la première broche connectée représente souvent les données de coordonnées de la spline, ce qui ne convient pas à la prévisualisation.

Pour résoudre ce problème, un attribut de sortie par défaut a été introduit. Cette fonctionnalité permet à l&#39;auteur du graphique de <b>spécifier quelle sortie doit être affichée par défaut</b>, ce qui améliore l&#39;intuitivité de l&#39;utilisation des nœuds et facilite une meilleure compréhension du graphique créé.

Jouez avec l’image ci-dessous pour voir la différence avant et après la définition de sortie par défaut.

[En savoir plus](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

<table>
  <tr>
    <td>
      <img src="version-15-1.resources/defaultouput2.png" alt="defaultouput2">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="version-15-1.resources/defaultouput1.png" alt="Avec la sortie par défaut, les vignettes sont toujours pertinentes.">
      <br><i>Après</i>
    </td>
  </tr>
</table>

## Nœud &#39;Is defined&#39;

Lorsque vous travaillez avec des graphiques de fonctions, vous devrez peut-être déterminer s&#39;il existe une [variable](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) dans le graphique.

Par exemple, la détection de l’absence d’une variable vous permet de fournir une valeur de secours, en veillant à ce que la fonction se comporte comme prévu sans que chaque entrée doive être explicitement définie. C&#39;est pourquoi nous avons ajouté le nœud [&#39;Is defined&#39;](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md).

[En savoir plus](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)

![Nœud défini](version-15-1.resources/isdefined.png){zoomable="yes"}

## Notes de mise à jour

### 15.1.0

*(Publié le 11 décembre 2025)*

### Ajouté

* [Nouveau graphique] Modification de la fenêtre du nouveau graphique
* [NewGraph] Ajout d’échantillons de matériaux et d’échantillons avancés
* [NewGraph] Ajouter un nouvel attribut pour le graphique pour les données du modèle (catégorie et sous-titre)
* [NewGraph] Option Supprimer le format de sortie
* [Contenu] Ajout de fonctions de hachage
* [Contenu] Ajout de mappeurs de tonalité à features.sbs
* [Contenu] Bruit anisotrope v2 : ajout du format de sortie par défaut, ajout de désordre
* [Content] Appliquer la casse de la phrase aux étiquettes de nœuds et de paramètres
* [Contenu] Points BnW 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Points BnW 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Points BnW 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Content] Cellules 1,2,3,4 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques, options de désordre
* [Contenu] Clouds 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Clouds 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Clouds 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Couleur au masque v2
* [Contenu] Bruit directionnel 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Bruit directionnel 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Bruit directionnel 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Bruit directionnel 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Rayures directionnelles v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 5 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dégradé de Dirt v2 : ajout du format de sortie par défaut, nouvelles options de désordre
* [Content] Somme fractale Base v2 : ajout du format de sortie par défaut, désordre, pas de prise en charge des mosaïques
* [Content] Somme fractale 1,2,3,4 v2 : ajout du format de sortie par défaut
* [Contenu] Bruit gaussien v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Taches gaussiennes 1&amp;2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Fibres désordonnées 1,2,3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions, options de désordre
* [Contenu] Bruit d’humidité v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Nouveau nœud « Bruit d&#39;humidité 2 »
* [Contenu] Bruits : mettre à jour pour ajouter le format de sortie par défaut
* [Contenu] Bruit de perlin v2 : ajout du format de sortie par défaut, pas de prise en charge de la juxtaposition
* [Contenu] Mappeur de formes : ajouter un mode de filtrage
* [Contenu] Mappeur UV : ajouter un mode de filtrage
* [Contenu] Forme d’onde 1 v2 : utilisation du format de sortie par défaut + nouvelles options
* [Contenu] Bruit blanc v2 : utilisation du format de sortie par défaut, ajout d’options de distribution
* [Boulangers] Afficher uniquement les UV du maillage sélectionné
* [Bakers] Ajoutez une option pour sélectionner la méthode de correspondance de la géométrie par nom
* [Boulangers] Sélectionner le boulanger le plus proche lorsqu’un boulanger est supprimé
* [Boulangers] UDIM : définissez une liste de tuiles UV à cuire
* [Bakers] Mise à jour du kit de développement de bake vers la version 3.15.4
* [3D View/SceneBrowser] Évitez de sélectionner un élément UsdPrimitive lorsque vous effectuez un clic droit dessus
* [ColorManagement] Prise en charge d&#39;ACES 2.0
* [Graphique de composition] Autoriser à définir un nœud de sortie comme « Sortie par défaut »
* [Cooker] Supprimer l&#39;avertissement sur les entrées non connectées des instances de fonction¬†
* [Fonctions] Opérateur Add isDefined
* [Graphique] Regrouper les éléments par attribut « groupe » dans le menu du nœud
* [Graphique] Amélioration du rendu des vignettes

### Correctifs

* [Vue 3D] La texture en niveaux de gris L16 s’affiche avec une teinte rouge lorsqu’elle est connectée à l’environnement ou à la baseColor
* [Vue 3D] La modification de la liaison de matière d’une scène sans matière crée une nouvelle matière par défaut
* [Vue 3D] Les normales calculées ne sont pas correctes pour des maillages OBJ spécifiques
* [Vue 3D] L’environnement personnalisé de SBSSCN n’est pas visible lors du chargement dans le traceur de chemin
* [Vue 3D] Erreurs dans la console lors de la rotation d’un environnement désactivé
* Le Specular level [Vue 3D] n’est pas appliqué correctement
* [Vue 3D] Le Specular edge color ne fonctionne pas lors de l’utilisation de la pixellisation Eclair
* [Vue 3D] La matière ajoutée par l’utilisateur n’est pas appliquée aux scènes par défaut
* [Vue 3D][Boulangers] La couleur du matériau est trop sombre une fois remplacée ou lors de l’utilisation d’un boulanger « Color »
* [Vue 3D][Bakers] Aucune couleur de matière du fichier FBX
* [Boulangers] Les couleurs de matériau dans les fichiers FBX ne sont pas correctement détectées
* [Bakers] L’option « recalculer\_tangentes » est toujours « false » dans les exportations de paramètres prédéfinis JSON
* [Bakers] CLI : Blocage lors de l’exécution du même baker de manière consécutive via un fichier JSON
* [Bakers] La mise à jour du paramètre « color-generator » ne fonctionne pas pour « Grayscale »
* [Contenu] Masquage sur tracés : échec dans les rapports non carrés
* [Contenu] Rendu Rendu PBR/Icône : fonction incorrecte du lobe de specular
* [Contenu] Tracés vers la spline : définissez la taille de sortie sur Relative au parent par défaut
* [Contenu] Liste de points : les points ne sont pas dans le bon ordre lorsque la texture des données n’est pas carrée
* [Contenu] Mappeur de spline : problème de ligne de 1 px dans des cas aléatoires
* [Contenu] Spline mapper : UV étirés dans certains cas lorsque le thickness est de 0
* [Graphique] Blocage lors de la suppression de la sortie d’un sous-graphe de fonction
* [Graphique] Le type de couleur du nœud d’entrée peut être modifié dans les packages en lecture seule
* [Graphique] L’entrée principale peut être modifiée dans les packages en lecture seule
* [Propriétés] La couleur du widget d’aperçu de couleur ne correspond pas à l’état du bouton sRVB
* [Scène] Impossible de charger un fichier OBJ de plus de 2 Go
* [UI] Les états d&#39;ancrage de la console et du gestionnaire de dépendances ne sont pas restaurés après le redémarrage

### PROBLÈMES CONNUS

* [Boulangers] Blocages lors de la cuisson avec certains pilotes NVIDIA spécifiques
* [Vue 3D] OpenGL : certaines scènes importées peuvent ne pas être rendues
* [Vue 3D] Traceur de tracé : performances lentes lors de la mise à jour des textures avec la tessation/le displacement activé
* [Vue 3D] Certaines propriétés de matériau de couleur ne sont pas gérées correctement lorsqu’elles sont remplacées
* [Vue 3D] Les scènes avec des primitives animées ne sont pas prises en charge correctement
* [Vue 3D] Les filets avec plusieurs UDims ne sont pas encore pris en charge
* [Vue 3D] Les filets comportant plusieurs UV ne sont pas pris en charge et peuvent entraîner un rendu de matériau non valide.
* [Vue 3D] Traceur de tracé non pris en charge sur les cartes graphiques AMD
