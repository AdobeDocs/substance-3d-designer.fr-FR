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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---


# Version 15.1

La Substance Designer 15.1 offre une fenêtre de création de graphe entièrement repensée avec un accès direct à l’échantillon, des nœuds de bruit améliorés pour de plus grandes possibilités de création, des catégories organisées dans le menu des nœuds, et bien plus encore.

*Date de publication : 11 décembre 2025*

![Bannière Designer 15.1](../../assets/bannerweb.png)

## Améliorer la création de graphes

Dans cette version, la [fenêtre de création de graphe](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) a été <b>entièrement repensée</b> pour améliorer l&#39;expérience utilisateur initiale dans Substance 3D Designer. L’objectif principal de cette mise à jour est de rationaliser le processus de sélection des modèles, ce qui permet aux utilisateurs d’identifier efficacement le modèle le mieux adapté à leurs besoins.

Les vignettes offrent des <b>références visuelles</b> instantanées pour les types de matériaux prévus, tandis que les info-bulles détaillées fournissent toutes les informations pertinentes. Pour une meilleure organisation, les modèles sont désormais classés dans des <b>catégories</b> spécifiques, telles que les matériaux, les filtres et le traitement de la numérisation.

Bien que l’interface principale ait été mise à niveau, les utilisateurs continuent d’avoir accès aux affichages précédents, y compris les options de liste, de packages et de répertoires.

[En savoir plus](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)

![reconcevoir la nouvelle fenêtre de graphe](../../assets/newgraph.png){zoomable="yes"}

## Échantillons incorporés

Avec le lancement de notre nouvelle fenêtre de création de graphes, nous avons ajouté une variété de [<b>matériaux d&#39;exemple</b>](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) directement dans le logiciel. Cette amélioration fait suite à votre demande d&#39;un meilleur accès aux ressources d&#39;apprentissage.

![Fenêtre de création d&#39;un nouveau graphe pour les échantillons](../../assets/GraphSample.png){zoomable="yes"}

Pour répondre à ce besoin, nous avons inclus des échantillons de matériau tels que des tissus (y compris le cuir et le satin), le bois, le métal, le plastique, la céramique et plus encore. Ces exemples ont pour but de vous aider à démarrer vos projets en toute simplicité et à vous familiariser avec les principaux nœuds de la famille disponibles dans Substance 3D Designer

Chaque graphe est <b>annoté</b>, soigneusement organisé et contient un nombre minimal de nœuds pour le rendre aussi facile à comprendre que possible.

Vous pouvez accéder aux échantillons dans la catégorie « Échantillons de Matériau » lors de la création d’un nouveau graphe de Substance de données, ou directement depuis l’écran d’accueil à l’aide du bouton pratique « Accéder aux échantillons ».

Parallèlement à ces matériaux fondamentaux, nous avons également fourni des <b>échantillons avancés</b> pour démontrer comment utiliser plus efficacement les fonctionnalités <b>FX-map et Processeur de pixels</b>.

[En savoir plus](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)

![échantillon de bois dans substance designer](../../assets/samplegraph.png){zoomable="yes"}

## Nouveaux bruits

Les bruits jouent un rôle essentiel dans la majorité des graphes. C’est pourquoi nous avons mis l’accent sur plusieurs améliorations majeures de cette version afin d’améliorer leur fonctionnalité et leur convivialité.

Avec cette mise à jour, nous avons introduit <b>une meilleure prise en charge des scénarios sans répétition</b>, en veillant à ce que les modèles de bruit se comportent comme prévu, sans répétition obligatoire. Auparavant, les nœuds de bruit étaient soit forcés à afficher des mosaïques, soit produisaient des résultats incorrects lorsque la répétition était désactivée.

La plupart des bruits incluent désormais <b>nouveaux paramètres</b>, ce qui offre aux utilisateurs un meilleur contrôle créatif. Ces options supplémentaires permettent aux auteurs de graphe d’affiner l’apparence et le comportement du bruit dans leurs workflows.

Enfin, la profondeur de bits <b>n&#39;est plus verrouillée en mode 16 bits</b>. Vous pouvez désormais remplacer le paramètre de profondeur de bit sur des instances de nœud individuelles, ce qui vous permet d’obtenir des détails plus détaillés et une plage dynamique plus élevée si nécessaire, ou d’optimiser vos graphes pour les performances.

Consultez la liste complète des bruits mis à jour dans les [notes de mise à jour](#release-notes) ci-dessous.

Exemples : [Cellules 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) [Nuages 2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md) [Rayures directionnelles](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-scratches/directional-scratches.md) [bruit d&#39;humidité 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

![bruit de désordre directionnel](../../assets/directionaldisorder.gif){zoomable="yes"}

## Hiérarchie dans le menu des nœuds

Pour relever le défi de localiser des nœuds spécifiques dans la vaste bibliothèque, nous avons introduit des catégories dans le menu Nœud.

Le grand nombre de nœuds disponibles peut rendre difficile la recherche rapide du nœud souhaité. Pour rationaliser ce processus, un nouvel attribut [<b>Groupe</b>](../../compositing-graphs/graph-parameters/graph-parameters.md) a été implémenté au niveau du graphe. Lorsque cet attribut est défini, il est utilisé pour organiser et trier les résultats de la recherche.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![recherche de nœud avec catégorie 1](../../assets/search1-2.png){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![recherche de nœud avec catégorie 2](../../assets/search2.png){zoomable="yes"}

</td>
</tr>
</table>

## Sortie par défaut

Lorsqu&#39;un nœud a plusieurs [sorties](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), il n&#39;est pas possible de les afficher simultanément dans la Vue 2D ou en tant que miniature de nœud. La directive dominante dans de tels scénarios est d&#39;utiliser la première épingle connectée, ou, si aucune n&#39;est connectée, la première sortie par défaut.

Cependant, cette approche peut ne pas toujours donner des résultats optimaux. Par exemple, dans certains nœuds Spline, la première épingle connectée représente souvent les données de coordonnées de la spline, ce qui ne convient pas à la prévisualisation.

Pour résoudre ce problème, un attribut de sortie par défaut a été introduit. Cette fonctionnalité permet à l&#39;auteur du graphe de <b>spécifier quelle sortie doit être affichée par défaut</b>, ce qui améliore l&#39;intuitivité de l&#39;utilisation des nœuds et facilite une meilleure compréhension du graphe créé.

Jouez avec l’image ci-dessous pour voir la différence avant et après la définition de sortie par défaut.

[En savoir plus](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

<table>
  <tr>
    <td>
      <img src="../../assets/defaultouput2.png" alt="defaultouput2">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../assets/defaultouput1.png" alt="Avec la sortie par défaut, les vignettes sont toujours pertinentes.">
      <br><i>Après</i>
    </td>
  </tr>
</table>

## Nœud &#39;Is defined&#39;

Lorsque vous travaillez avec des graphes de fonction, vous devrez peut-être déterminer si une [variable](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) existe dans le graphe.

Par exemple, la détection de l’absence d’une variable vous permet de fournir une valeur de secours, en veillant à ce que la fonction se comporte comme prévu sans que chaque entrée doive être explicitement définie. C&#39;est pourquoi nous avons ajouté le nœud [&#39;Is defined&#39;](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md).

[En savoir plus](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)

![Nœud défini](../../assets/isdefined.png){zoomable="yes"}

## Notes de mise à jour

### 15.1.0

*(Publié le 11 décembre 2025)*

### Ajouté

* [NewGraph] Modification de la fenêtre du nouveau graphe
* [NewGraph] Ajout d’échantillons de matériaux et d’échantillons avancés
* [NewGraph] Ajouter un nouvel attribut pour le graphe des données du modèle (catégorie et sous-titre)
* [NewGraph] Option Supprimer le format de sortie
* [Contenu] Ajout de fonctions de hachage
* [Contenu] Ajout de mappeurs de tonalité à features.sbs
* [Contenu] bruit anisotrope v2 : ajouter le format de sortie par défaut, ajouter un désordre
* [Content] Appliquer la casse de la phrase aux étiquettes de nœuds et de paramètres
* [Contenu] Points BnW 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Points BnW 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Points BnW 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Cellules 1, 2, 3, 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions, options de désordre
* [Contenu] Clouds 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Clouds 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Clouds 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Couleur au masque v2
* [Contenu] Bruit directionnel 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Bruit directionnel 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Bruit directionnel 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Bruit directionnel 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Rayures directionnelles v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 5 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dégradé de Dirt v2 : ajout du format de sortie par défaut, nouvelles options de désordre
* [Contenu] Somme fractale Base v2 : ajout du format de sortie par défaut, désordre, pas de prise en charge des répétitions
* [Content] Somme fractale 1,2,3,4 v2 : ajout du format de sortie par défaut
* [Contenu] bruit gaussien v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Taches gaussiennes 1&amp;2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Fibres désordonnées 1,2,3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions, options de désordre
* [Contenu] bruit d’humidité v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Nouveau nœud « Moisture bruit 2 »
* bruits [Content] : mettre à jour pour ajouter le format de sortie par défaut
* [Contenu] Perlin bruit v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* Mappeur de formes [Contenu] : ajouter un mode de filtrage
* [Content] UV mapper : ajouter un mode de filtrage
* [Contenu] Forme d’onde 1 v2 : utilisation du format de sortie par défaut + nouvelles options
* [Contenu] bruit blanc v2 : utilisation du format de sortie par défaut, ajout d’options de distribution
* [Bakers] Afficher uniquement les UV du maillage sélectionné
* [Bakers] Ajoutez une option pour sélectionner la méthode de correspondance de la géométrie par nom
* [Bakers] Sélectionner le Baker le plus proche lorsqu’un baker est supprimé
* [Bakers] UDIM : définissez une liste d’UV à baker
* [Baker] Mise à jour du kit de développement logiciel baking vers la version 3.15.4
* [vue 3D/SceneBrowser] Évitez de sélectionner un élément UsdPrimitive lorsque vous effectuez un clic droit dessus
* [ColorManagement] Prise en charge d&#39;ACE 2.0
* [Graphe de composition] Autoriser à définir un nœud de sortie comme « Sortie par défaut »
* [Cooker] Supprimer l&#39;avertissement sur les entrées non connectées des instances de fonction¬†
* [Fonctions] Opérateur Add isDefined
* [Par Graphe] Regroupez les éléments par attribut &#39;group&#39; dans le menu du nœud
* [Graphe] Amélioration du rendu des vignettes

### Correctifs

* [vue 3D] La texture Niveaux de gris L16 s’affiche avec une teinte rouge lorsqu’elle est connectée à l’environnement ou à la baseColor
* [vue 3D] La modification de la liaison de matériau d’une scène sans matériau crée un nouveau matériau « par défaut »
* [vue 3D] Les normales calculées ne sont pas correctes pour des maillages OBJ spécifiques
* [vue 3D] L’environnement personnalisé de SBSSCN n’est pas visible lors du chargement dans Pathtracer
* [vue 3D] Erreurs dans la console lors de la rotation d’un environnement désactivé
* Le Specular level [vue 3D] n&#39;est pas appliqué correctement
* [vue 3D] Le Specular edge color ne fonctionne pas lors de l’utilisation de la pixellisation Eclair
* [vue 3D] Le matériau ajouté par l&#39;utilisateur n&#39;est pas appliqué aux scènes par défaut
* [vue 3D]&#x200B;[Bakers] La couleur du Matériau est trop sombre une fois remplacée ou lors de l’utilisation d’un baker « Couleur »
* [vue 3D]&#x200B;[Bakers] Aucune couleur de matériau du fichier FBX
* [Bakers] Les couleurs de Matériau dans les fichiers FBX ne sont pas correctement détectées
* [Baker] L’option « recompute\_tangentes » a toujours la valeur « false » dans les exportations de paramètres prédéfinis JSON
* [Baker] CLI : Crash lors de l’exécution du même baker de manière consécutive à travers le Fichier JSON
* [Bakers] La mise à jour du paramètre « color-generator » ne fonctionne pas pour « Grayscale »
* [Contenu] Masquage sur tracés : échec dans les rapports non carrés
* [Contenu] Rendu Rendu PBR/Icône : fonction incorrecte du lobe de specular
* [Contenu] Tracés vers la spline : définissez la « Taille de sortie » sur « Relatif au parent » par défaut
* [Contenu] Liste de points : les points ne sont pas dans le bon ordre lorsque la texture des données n’est pas carrée
* [Contenu] Mappeur de spline : problème de ligne de 1 px dans des cas aléatoires
* [Content] Spline mapper : étire les UV dans certains cas lorsque le thickness est à 0
* [Graphe] Crash lors de la suppression de la sortie d&#39;un sous-graphe de fonction
* [Graphe] Le type de couleur de Noeud d&#39;entrée peut être modifié dans les packages en lecture seule
* [Graphe] L’entrée principale peut être modifiée dans les packages en lecture seule
* [Propriétés] La couleur du widget d’aperçu de couleur ne correspond pas à l’état du bouton sRVB
* [Scène] Impossible de charger un fichier OBJ de plus de 2 Go
* [UI] Les états d&#39;ancrage de la console et du gestionnaire de dépendances ne sont pas restaurés après le redémarrage

### PROBLÈMES CONNUS

* [Bakers] Crashs lors du baking avec certains pilotes NVIDIA spécifiques
* [vue 3D] OpenGL : certaines scènes importées peuvent ne pas être rendues
* [vue 3D] Traceur de tracé : performances lentes lors de la mise à jour des textures avec la tessation/le displacement activé
* [vue 3D] Certaines propriétés de matériau de couleur ne sont pas gérées correctement lorsqu’elles sont remplacées
* [vue 3D] Les Scènes avec des primitives animées ne sont pas correctement prises en charge
* [vue 3D] Le Maillage avec plusieurs UDims n&#39;est pas encore pris en charge
* [vue 3D] Les Maillages avec plusieurs UV ne sont pas pris en charge et peuvent entraîner un rendu de matériau non valide
* [vue 3D] Pathtracer non pris en charge sur les cartes graphiques AMD
