---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-12-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 12.1 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 12.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 0%

---


# Version 12.1

**Substance 3D Designer 12.1** apporte de nombreux nouveaux nœuds pour les graphes des matériaux de Substance, la prise en charge des formats de fichier USD et une plus grande interopérabilité avec Stager.

Date de publication : *26 avril 2022*

## Fonctionnalité majeure

### Nouveau contenu pour les graphiques de matériaux de Substance

![](../../assets/yellow-intense-reduce.png)

Beaucoup de nœuds ont été ajoutés dans cette version, vous trouverez de nouveaux motifs, de nouveaux bruits, de nouveaux filtres, ...

Jetez un œil aux pages de nœuds liées ci-dessous pour des exemples de l&#39;ampleur de la sortie qui est réalisée par ces nouveaux nœuds puissants !

* **Nouveaux motifs**

  * Nous avons ajouté un nouveau nœud <b>Mosaïque aléatoire 2</b> pour générer des mosaïques adjacentes de tailles et de rapports aléatoires, ce qui est très utile pour créer rapidement des grilles entièrement irrégulières avec des coins et des biseaux inclinés et arrondis.

    ![](../../assets/tilerandom2-demo2.gif){width="640px"}
  * Nouveau motif de <b>Triangle Grid</b> pour générer une grille composée de triangles. Nous l&#39;utilisons dans le matériau ci-dessous pour simuler facilement et parfaitement le grain du cuir. Ce générateur représente une surface de sommets dans l’espace 3D et peut être utilisé pour créer divers styles polygonaux.

    ![](../../assets/trianglegrid-demo.png){width="640px"}
* **Nouveaux bruits**

  * Afin de vous donner plus de variété, un ensemble de <b>15 nouvelles cartes d&#39;Usure/salissures</b> (béton, fuites, éclaboussures sales, ...) a été ajouté à la bibliothèque.

    ![](../../assets/grungemaps.png){width="640px"}
  * Vous trouverez également de <b>nouveaux bruits 2D et 3D</b>, tels que Voronoi (2D et 3D), Voronoi Fractal (2D et 3D), 3D Ridged Fractal et une mise à jour du bruit Perlin 3D actuel (ajout de carrelage et d’options absolues).\
    Ces bruits sont tous cartographiés dans l&#39;espace 3D et offrent plusieurs styles, ce qui permet une plus grande variété et un contrôle qui vous donnera beaucoup de choix pour créer la carte parfaite pour votre matériel, comme la mer et les panneaux de science-fiction ci-dessous.

    ![](../../assets/fractal-voronoi-sea.gif){width="640px"}

    ![](../../assets/fractal-voronoi-scifi-panel.gif){width="640px"}
  * Collection de <b>nœuds de texture 3D</b> (position, SDF, décalage) et de <b>nœuds de rendu 3D </b> (surface ou volume) pour créer et rendre des textures 3D, qui sont un atlas des tranches d’un modèle 3D.

    ![](../../assets/image2022-4-22-11-46-17.png){width="640px"}

* **Nouveaux filtres**

  * Avec le nœud <b>Recadrage automatique</b>, vous pouvez placer une forme au *centre* de l&#39;image sans être redimensionnée, ou la redimensionner pour l&#39;adapter à l&#39;espace. Par exemple, votre forme peut être librement modifiée tout en conservant une position et une taille cohérentes lorsqu’elle est dispersée.

    ![](../../assets/autocrop-demo-01-resized.gif){width="640px"}
  * Avec le nœud <b> Extend Shape</b>, vous pourrez étirer une section d&#39;une forme dans une direction et une distance personnalisées.

    ![](../../assets/extendshape.gif){width="640px"}
  * Et avec le nœud <b>Rotation non uniforme</b>, vous pouvez faire pivoter une entrée en fonction d&#39;un mappage donné.

    ![](../../assets/nonuniformrotation-demo-02-resized.gif){width="640px"}
* **Et aussi...**

  * Fonctions d&#39;accélération (graphique de fonction) très utiles pour piloter une valeur de manière non linéaire.
  * Enfin, cette version apporte également une nouvelle version plus précise du nœud <b>Quantize</b>, ainsi qu&#39;un tout nouveau filtre utilitaire <b>Summed Area Table</b>.

### Amélioration de l’interopérabilité

* **Assistance USD** En plus de la

  et

  formats de fichiers, vous pouvez désormais importer et exporter des fichiers USD (

  ,

  ,

  ) afin de les utiliser comme ressources de vos graphiques de Substance, pour les appliquer à la cuisson ou dans la vue 3D pour présenter votre matériau de Substance. Vous pouvez également utiliser ce format pour exporter votre graphique de Substance ou le contenu de la vue 3D.
* <b>Envoyer vers Stager\
  </b>Vous pouvez désormais envoyer votre matériel de Substance à Stager en un clic, comme cela était déjà possible avec Sampler et Painter. Grâce à cette fonctionnalité, plus besoin de publier en tant que SBSAR et de charger des fichiers individuels (nécessite Stager version 1.2.0 avec le nouveau gestionnaire de matériaux)

  ![](../../assets/sendtostagershort.gif)

### Divers

* Si vous travaillez sur des tissus, vous pouvez désormais afficher un filet dédié dans la vue 3D afin de mieux voir comment votre matériau est rendu sur une forme drapée. Ouvrez le menu <b>Scène</b> dans le panneau Vue 3D et sélectionnez l&#39;option <b>Tissu</b> pour afficher ce modèle.

  ![](../../assets/fabric-rendering.png){width="640px"}

* Nous avons également ajouté de nouveaux nœuds de gestion de scènes pour les graphiques de modèles de Substance. Ces nœuds vous permettent de renommer, redéfinir la parenté, fusionner ou développer les éléments de votre scène afin d’organiser la hiérarchie de celle-ci. Il existe également un nouveau nœud pour définir le pivot d’un ou plusieurs éléments d’une scène.

* Lorsque vous travaillez sur des projets dans Designer, vous pouvez rencontrer des avertissements et des messages d’erreur, qui vous informent d’un problème dans le projet. Dans cette version, nous <b>améliorons le système de gestion des erreurs</b> afin de faire apparaître toutes les erreurs et tous les avertissements dans l&#39;Explorateur : tout est répertorié au même endroit, il est donc plus facile de vérifier si votre projet contient des problèmes.

  ![](../../assets/warning-overview-explorer.png){width="640px"}

## Notes de mise à jour

### 12.1.0

*(Publié Le 19 Avril 2022)*

<b>Ajouté :</b>

* [Main] Nouveau contenu pour les graphiques de matériaux
* [Main] Envoyer des matériaux à Stager
* [Main] Prise en charge des fichiers USD
* [Principal] Amélioration du signalement des erreurs dans l’interface utilisateur
* [Principal] Nœuds de gestion de scène pour les graphiques modèles
* [Contenu] Ajout d’options supplémentaires aux bruits de perlin 3D (mosaïque, absolu...)
* [Contenu] Nouveau nœud fractal 3D Ridged Noise
* [Contenu] Nouveau nœud Décalage de texture 3D
* [Contenu] Nouveau nœud de position de texture 3D
* [Contenu] Nouveau nœud de surface de rendu de texture 3D
* [Contenu] Nouveau nœud de volume de rendu de texture 3D
* [Contenu] Nouveau nœud de Champ de distance signée de texture 3D
* [Contenu] Nouveau nœud de recadrage automatique
* [Contenu] Nouvelles fonctions d’accélération
* [Contenu] Nouveaux nœuds Extend Shape
* [Contenu] Nouvelles Cartes D’Usure/salissures
* [Content] Nouveau nœud de rotation non uniforme
* [Content] Nouveau filtre Tableau de zones de somme
* [Contenu] Nouveau générateur Tile Random 2
* [Contenu] Nouveau générateur de motif de Triangle Grid
* [Content] Nouvelle version du nœud Quantize Grayscale
* [Contenu] Nouveaux bruits fractaux Voronoi et Voronoi (2D/3D)
* [Contenu] Seuil : ajout du mode de comparaison « Inférieur » et « Inférieur et égal »
* [Contenu][Vue 3D] Ajoutez un ajustement de maillage pour afficher les tissus aux ressources expédiées
* [Modèles de Substance] Nouveau nœud Développer les instances de groupe
* [Modèles de Substance] Nouveau nœud de Fuse
* [Modèles de Substance] Nouveau nœud Renommer
* [Modèles de Substance] Nouveau nœud Reparent
* [Modèles de Substance] Nouveau nœud Définir le pivot
* [Substance models] Mise à jour vers SDK 1.6.0
* [ThirdParty] Mettre à niveau Qt (et QtForPython) vers 5.15.8
* [Tiers] Mise à niveau de Python vers la version 3.9.9
* [Tiers] Mise à niveau d’OpenSSL vers la version 1.1.1m
* [UI] Amélioration du comportement du menu Nœud en cas de clic incorrect
* [UI] Ouvrir les sous-graphes dans le même onglet, même épinglés
* [UI] Bouton Supprimer l’épingle de la barre de titre du panneau Explorateur
* [UI] Enregistrer l’option « Ne plus afficher » sur l’écran de bienvenue dans toutes les versions
* [Vue 3D] Afficher l’unité de grille dans la clôture lorsque l’assistant « Axe » est activé
* [Automatisation] Fournir l’outil de ligne de commande sbsbaker avec Designer
* [Gestion des couleurs] Implémentation d’un nouveau back-end GPU pour Adobe ACE
* [Cooker] Ajouter une option pour cuisiner un paquet sans horodatage
* [Graphique] Ajout de badges dans le graphique FxMap
* [Bibliothèque] Ajout d’un nouveau filtre pour les fonctions d’accélération
* Prise en charge de [Player] USD
* [Properties] Ajoutez une erreur d&#39;avertissement sur le paramètre « PKG Resource Path » d&#39;un nœud Bitmap lorsque la ressource est introuvable
* [Substance Engine] Mise à niveau vers la version 8.4.1
* [Yebis] Avertissez l’utilisateur que les effets de post-traitement Yebis seront supprimés dans la prochaine version.
* [Documentation] Nouvelle page « Avertissements et erreurs »
* [Documentation] Nouvelle page décrivant l’héritage dans les graphiques de Substance
* [Documentation] Mise à jour de la section « Iray »
* [Documentation] Mise à jour de la section « Graphiques MDL »

<b>Fixe :</b>

* [UI] Problèmes d’écrêtage dans les info-bulles des modèles dans la nouvelle fenêtre graphique
* [UI] Texte blanc difficile à lire dans les nœuds lors de l’utilisation du mode sombre dans macOS
* [UI] Problème de disposition dans certaines boîtes de dialogue
* [UI] Le message d’avertissement s’affiche tronqué lors de la création du graphique de fonction de Substance dans l’Explorateur.
* [UX] Le sélecteur de couleurs descend à chaque nouvelle ouverture
* [UX] La fenêtre de l’éditeur de dégradé s’ouvre à chaque apparition
* [UX] Les propriétés du graphique ne s&#39;affichent pas automatiquement pour les packages chargés
* Mappeur de Flood Fill [Content] : sélection d&#39;entrée incorrecte dans un cas spécifique
* [Contenu] Flood Fill : fond perdu de texte dans les boutons de paramètres booléens
* [Contenu] Plage incorrecte pour le paramètre Angle du premier échantillon de lumière du nœud Plusieurs angles vers Normal
* [Modèles de Substance] Les propriétés du nœud affichent l&#39;identificateur au lieu de l&#39;étiquette
* [Modèles de Substance][Vue 3D] Problème d’actualisation lors de la réouverture d’un projet
* [Modèles de Substance][3Dview] Problème d’actualisation lors de l’utilisation de l’aperçu structure filaire
* [Paramètres] Blocage lors de la suppression rapide des entrées de graphique dans un cas spécifique
* [Paramètres] Blocage lors de la réinitialisation d’un paramètre d’instance lors de la modification de sa description de référence
* [Bitmap] La détection UDIM n&#39;est pas déclenchée pour les fichiers bitmap déposés dans le graphique
* [Graphique] Les nœuds de bitmap/SVG ne sont pas invalidés lorsque la ressource est modifiée sur le disque après le chargement du package
* [GraphRender] Fuite de mémoire lorsque l’évaluation du graphique de Substance est annulée
* [Localisation] La chaîne « Rebake all maps for this resource » apparaît non localisée
* [MDL] Paramètre exposé initialisé à 0 si l&#39;entrée est connectée à un nœud Dot non connecté
* [Préférences] Les info-bulles s’affichent même lorsque le curseur se trouve dans un espace vide
* [Propriétés] L’annulation d’une modification de la valeur d’espace colorimétrique définit la valeur par défaut dans un cas spécifique
* [Text] Impossible d&#39;annuler le changement de police vers une ressource de police manquante
