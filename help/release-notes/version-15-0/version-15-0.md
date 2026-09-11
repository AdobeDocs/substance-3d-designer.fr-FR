---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/release-notes/version-15-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 15.0 pour en savoir plus sur le nouveau moteur de rendu 3D et la prise en charge native d’USD.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 15.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1894'
ht-degree: 0%

---


# Version 15.0

Cette mise à jour apporte un tout nouveau rendu 3D, avec les modes pixelliseur et traceur, ainsi qu&#39;une prise en charge native de [USD](https://openusd.org/release/index.html) pour vous permettre de modifier et d&#39;exporter des scènes sans aucune perte de données.

*Date de publication : 15 juillet 2025*

![Bannière](../../assets/banner-47.png "Version 15.0")

## Nouveau moteur de rendu 3D

### Nouveau traceur de tracé et pixellisation

Cette nouvelle version vous donne accès à un [rendu 3D](../../interface/3d-view/3d-renderers/3d-renderers.md) avancé, avec un mode de pixellisation (pour avoir un aperçu en temps réel lorsque vous travaillez sur votre matériau) et un mode de traceur de tracé (un mode de lancer de rayon pour obtenir un rendu parfait et précis). Ce nouveau moteur de rendu améliore les fonctionnalités avec des fonctionnalités telles que les ombres en mode pixellisé, améliore la qualité et les performances, et est conçu pour prendre en charge les technologies futures telles que [MaterialX](https://materialx.org/). Il complète les rendus OpenGL et Iray existants dans Designer et s’aligne sur les rendus disponibles dans Substance 3D Viewer et Substance 3D Sampler, assurant une expérience uniforme dans l’ensemble de l’écosystème.

![tons foncés et translucency dans la pixellisation](../../assets/feature_1b.png)

La barre d&#39;outils de la vue [3D](../../interface/3d-view/3d-view.md) a été mise à jour pour avoir un accès rapide à certaines des nouvelles fonctionnalités disponibles dans ce moteur de rendu :

* <b>Outil de sélection :</b> pour sélectionner un sous-filet dans la scène. Une fois qu&#39;un sous-maillage est sélectionné, vous pouvez vous concentrer dessus (F) ou accéder à ses propriétés de matériau (clic droit).
* <b>Activez le traceur de tracé :</b> pour basculer rapidement entre les modes traceur de tracé et pixelliseur.
* <b>Activez les ombres :</b> pour activer les ombres dans la scène, ce qui est utile pour voir comment vos matériaux se comportent en fonction de la lumière.
* <b>Activer le plan de sol :</b> pour activer ou non le plan de sol dans la scène.

En outre, le raccourci clavier pour faire pivoter l&#39;éclairage d&#39;environnement a été modifié pour correspondre aux autres applications de Substance de données. Il s&#39;agit donc désormais de *<b>cliquer avec le bouton droit de la souris</b>* au lieu de *<b>cliquer avec le bouton droit de la souris tout en maintenant la touche Ctrl enfoncée</b>*.

### Effets de post-traitement

[Les Effets de post-traitement sont de retour](../../interface/3d-view/camera/post-effects/post-effects.md) ! Ils sont désormais disponibles via le menu Caméra et sont maintenant développés en interne.

* <b>Fleur :</b> simulez le reflet autour des points lumineux comme les lumières et les reflets, ce qui permet de mieux visualiser les surfaces d&#39;emissive.
* <b>Mappage des tonalités :</b>la gamme de couleurs avec les profils pour obtenir un effet de plage dynamique élevée (HDR).
* <b>Profondeur de champ :</b> simule les propriétés de mise au point d&#39;un objectif de caméra (pixellisation uniquement).

![Publier l’outil FX dans Designer 15.0](../../assets/postfx.gif)

## Édition d’actifs en contexte

Lorsque vous travaillez sur vos matériaux, vous pouvez [les prévisualiser dans le cadre d&#39;une Scène 3D spécifique](../../working-with-3d-scenes/working-with-3d-scenes.md). C’est pourquoi nous avons ajouté la possibilité d’importer et de rendre une scène complète, avec toutes ses textures, caméras et éclairages. Et cerise sur le gâteau, si cette scène fait référence à des ombrages MaterialX, ils seront correctement rendus avec le pixelliseur !

![scène USD chargée et rendue dans Designer](../../assets/feature_2.png)

Une fois importé, vous pouvez travailler sur votre scène en sélectionnant un maillage (avec une combinaison MAJ+clic ou grâce à l&#39;explorateur de scènes) et en [remplaçant l&#39;un de ses matériaux](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md). Vous pouvez alors :

* Créez ou chargez un graphe et appliquez-le sur un matériau de scène.
* Ajustez un matériau existant en [extrayant ses textures](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md) dans un nouveau graphe.

Enfin, une fois votre scène 3D modifiée, vous pouvez [l&#39;exporter](../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) en tant que nouveau fichier ou en tant que nouveau calque du fichier d&#39;origine, ce qui vous empêche de perdre des données (format USD uniquement).

Enfin, d’autres formats 3D sont désormais pris en charge pour l’importation et l’exportation : USD (+ usda, usdc, usdz), STL, PLY et GLTF, en plus des formats FBX et OBJ déjà disponibles.

## Infobulles enrichies

Des info-bulles riches ont été introduites pour mieux démontrer l&#39;objectif de chaque nœud. Ces info-bulles, actuellement disponibles uniquement pour les [noeuds atomiques](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), incluent des visuels pour démontrer l&#39;effet du nœud et fournissent un lien direct vers la documentation pour obtenir des informations détaillées, notamment la liste des paramètres, des conseils et des astuces.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![nœud de fusion](../../assets/blend.gif)

</td>
<td style="border: 0;" valign="top">

![nœud de flou](../../assets/blur.gif)

</td>
<td style="border: 0;" valign="top">

![nœud de distance](../../assets/distance.gif)

</td>
</tr>
</table>

## Amélioration de la prise en charge non carrée

Si vous devez travailler avec des textures non carrées, cette nouvelle option est faite pour vous. Dans les [propriétés du matériau](../../interface/3d-view/material-properties/material-properties.md) de la vue 3D, dans les options UV pour contrôler la répétition, vous pouvez désormais définir une valeur différente pour les deux axes.

![échelle U V différente](../../assets/nonsquare.png){zoomable="yes"}

## Bakers

Bien que l’interface de baking n’ait subi que des mises à jour mineures (consultez la liste détaillée ci-dessous pour plus d’informations), la bibliothèque de bakers a été entièrement reconstruite pour utiliser des bakers basés sur le GPU, ce qui se traduit par de bien meilleures performances. Avec les nouveaux formats de fichiers pris en charge mentionnés ci-dessus, cette mise à jour représente une avancée considérable pour les utilisateurs engagés dans des workflows de baking.

Remarque : si vous utilisiez sbsbaker.exe pour automatiser votre processus, l’outil a été renommé substance3d\_baker.exe (utilisez substance3d-baker —help pour plus d’informations).

## Mises à jour de la configuration requise pour les effets spéciaux

Chaque année, la [plateforme de référence pour les effets visuels](https://vfxplatform.com/) publie une liste d&#39;outils et de bibliothèques à utiliser dans chaque logiciel du secteur des effets visuels afin de réduire les incompatibilités entre les logiciels. Comme d&#39;habitude, nous *mettons à jour toutes nos dépendances* afin de respecter toutes ces recommandations.

## Vidéo

[![Mise à jour de Substance 3D Designer : nouveau moteur de rendu, post-FX et modification du contexte | Adobe Substance 3D](../../assets/video_15.png)](https://www.youtube.com/watch?v=6EkXxu-0Q_E)

## Notes de mise à jour

### 15.0.0

*(Publié le 15 juillet 2025)*

### Ajouté

* [vue 3D] Nouveau système de rendu, avec modes pixelliseur et traceur de tracé
* [vue 3D] Ajout d’un outil de sélection pour sélectionner un objet dans la Scène 3D
* [vue 3D] Ajouter la nouvelle option « Exporter la scène avec les calques... » action dans le menu « Scène »
* [vue 3D] Ajouter de nouveaux boutons de barre d’outils
* [vue 3D] Ajout de la possibilité de basculer entre plusieurs caméras contenues dans une scène USD
* [vue 3D] Permet de se concentrer sur l’objet sélectionné en appuyant sur la touche F dans le viewport
* [vue 3D] Autoriser à générer un Graphe de composition de Substance à partir d&#39;un matériau existant
* [vue 3D] Permet d’envoyer un Graphe SBS Comp dans vue 3D et d’affecter sa sortie unique à l’utilisation d’Environnement/Panorama
* [vue 3D] Effacez la sélection en cours en appuyant sur la touche Échap
* [vue 3D] Afficher une Scène 3D importée avec des textures
* [vue 3D] Distinguer les commandes de répétition de texture X et Y
* [vue 3D] Activer/désactiver les tons foncés
* [vue 3D] Activer/désactiver le plan de sol
* [vue 3D] Dans le menu « Matériaux », ajoutez « Supprimer » uniquement pour les Matériaux qui ont été ajoutés manuellement et qui sont inutilisés
* [vue 3D] Dans le menu « Matériaux », supprimez l’action « Tout supprimer »
* [vue 3D] Rendre les fichiers USDZ exportés autonomes
* [vue 3D] Rendre les propriétés de rendu persistantes lors du changement de mode de rendu
* [vue 3D] Conserver les entrées de matériau existantes lors du remplacement d’un Matériau
* [vue 3D] Réorganisation des propriétés de Caméra
* [vue 3D] Supprimer les actions « Caméra/Enregistrement de la capture d’écran... » et « Caméra/Copier la capture d’écran dans le presse-papiers »
* [vue 3D] Supprimez l’action de menu « Matériau/Tout reconstruire ».
* [vue 3D] Supprimez le préfixe « Par défaut » de l’étiquette de la caméra par défaut
* [vue 3D] Définissez l’action de menu « Rétablir la valeur par défaut » comme dernière action dans le menu hamburger de la propriété d’entrée de matériau
* [vue 3D] Réglages du Raccourci
* [vue 3D] Prise en charge des tons foncés et du translucency en mode temps réel
* [vue 3D] Prise en charge des nuanciers MaterialX à partir d&#39;une scène USD importée
* [vue 3D / OpenGL] Renommez le paramètre « Échelle UV activée » en « Activer la Taille physique à partir du Graphe ».
* [vue 3D / Effets de post-traitement] Fleur
* [vue 3D / Effets de post-traitement] Profondeur de champ
* [vue 3D / Effets de post-traitement] Mappage de tonalité
* [vue 3D / Scène Browser] Permet d’afficher les propriétés du Matériau lors de sa sélection dans SceneBrowser
* [vue 3D / Scène Browser] Masquer la colonne « Matériau »
* [vue 3D / Scène Browser] Mettre en gras les primitives USD qui sont contrôlées par une entité prédéfinie
* [Bakers] Ajout d’un menu contextuel dans l’arborescence avec des actions « Tout sélectionner »/« Tout désélectionner »
* [Bakers] Ajout d’une option pour contrôler l’interpolation bitangente
* [Bakers] Ajout d’un séparateur horizontal dans l’interface utilisateur graphique
* [Bakers] Ajout d’une macro UDIM par défaut dans le nom de la sortie lorsque la scène est udim
* [Bakers] Autoriser à recalculer la tangente
* [Bakers] Autoriser à renommer un baker sans rompre les liens
* [Bakers] Modification de la taille par défaut du panneau central
* [Baker] texture de saisie pour le workflow UDIM
* [Bakers] Faire correspondre l’ordre de liste des cartes vue 2D à l’ordre de liste de rendu des Bakers
* [Bakers] Rendre la fenêtre de baking modale
* [Baker] Gestion des paramètres de mappage de tonalité
* [Bakers] Supprimer la sélection de plugin de repère tangent
* [Bakers] Statut d’enregistrement « activé » ou « désactivé » pour les Bakers lors de l’enregistrement d’un paramètre prédéfini
* [Bakers] Sélectionner le matériau par défaut dans le widget de sélection
* [Bakers] Définir l’orientation par défaut de la texture de sortie normale par rapport à la préférence
* [Baker] Définissez UV tiles sur Tous par défaut
* [Baker] Option d’ajout FromTexture/FromValue dans WordSpaceDirection
* [Bakers] World to tangente : définissez l’entrée par défaut sur « from texture »
* [SBSBaker] Création d’une option pour contrôler l’ordre du back-end
* [SBSBaker] Amélioration de l’utilisation de l’argument StringList
* [SBSBaker] Renommez « match\_source\_instance » en « match\_maillage\_name »
* [SBSBaker] Renommez « Submesh » en « GeomSubset ».
* [SBSBaker] Renommer en substance3d\_baker
* [Contenu] Ajouter une forme « Hémisphère » aux nœuds de générateur exposant des formes de quadrant
* [Interop] Prise en charge du format de fichier GLTF
* [Interop] Prise en charge du format de fichier PLY
* [Interop] Prise en charge du format de fichier STL
* [Bibliothèque] Uniformiser les info-bulles pour les noeuds atomiques
* [Mac] Ne plus prendre en charge les plates-formes MacIntel
* [Nodes] Ajouter des info-bulles riches pour les noeuds atomiques
* [Paramètres] Fermer la section « Attributs » par défaut
* [Paramètres] Permet à l’utilisateur de spécifier les valeurs par défaut des paramètres de base pour les nouvelles instances
* [Préférences] Bakers : ajoutez une option booléenne pour calculer l’espace de tangente par fragment
* [Préférences] Supprimer les plug-ins d’espace de tangente
* [Préférences] Stockez les préférences par version mineure de SD (XX.X).
* [VFX] Mise à jour de Boost vers 1.85.0
* [VFX] Mise à jour de MacOS version minimale vers la version 12.0
* [VFX] Mise à jour d’OpenColorIO vers la version 2.4.2
* [VFX] Mise à jour d’OpenColorIO vers la version 2.4.x
* [VFX] Mettre à jour OpenExr vers la version 3.3.x
* [VFX] Mise à jour de Qt vers la version 6.5.8

### Correctifs

* Les Textures [vue 3D] de la scène USD exportée ne sont pas correctement appliquées
* [vue 3D] [UDIM] Impossible d&#39;afficher les sorties du graphe UDIM dans vue 3D lorsque l&#39;affichage automatique à l&#39;ouverture du graphe est désactivé dans les préférences de graphe
* [Bakers] &#39;Anticrénelage.&#39; et &#39;Moy. les cellules des normales pour les bakers non applicables sont vides et modifiables
* [Bakers] L’action « Actualiser » utilise le back-end raytracing lorsqu’elle est désactivée dans les préférences
* [Bakers] Bakers bloqués comme occupés après l&#39;échec du processus « Actualiser toutes les maps bakées »
* [Bakers] Crash à plus de 180 UDIM lors du baking du mappage de position OpenGL sur un maillage spécifique
* [Bakers] Crash lors de l’ouverture de la boîte de dialogue « Informations sur le modèle Baker » plusieurs fois de suite (macOS uniquement)
* [Bakers] Dans l’exportation du paramètre prédéfini JSON, la valeur « udim » est remplacée par « 1001 » lorsqu’elle était définie sur « Tout ».
* [Bakers] La mémoire n&#39;est pas correctement détectée sous Linux
* [Bakers] La dépendance d’entrée de mappage manquante ne déclenche pas d’avertissement et/ou de rendu de bloc
* [Bakers] Aucun libellé d’erreur lorsque le nom de la sortie est vide
* [Bakers] Le remplacement du maillage high poly du fichier n’a aucun effet
* [Bakers] Le baker cible n’est pas sélectionné par défaut lors de l’utilisation de l’action « Rebake »
* [Moteur] Distance : « coupe » visible dans certaines situations
* [Moteur] Fx-Map : les couleurs négatives ne sont pas prises en charge lorsque la profondeur de bit est de 8 bits (moteurs GPU uniquement)
* [Localisation] La saisie des caractères revient du japonais au latin dans le menu des nœuds
* [Security] Vulnérabilité d&#39;analyse de fichier USDC hors écriture liée
* [Sécurité] Vulnérabilité II d’écriture hors limites lors de l’analyse du fichier NEF
* [Sécurité] Vulnérabilité de lecture III hors limites lors de l’analyse du fichier DNG
* [Préférences] Problèmes UX dans les paramètres de projet pour les projets en lecture seule
* [Ressources] Les Ensembles d&#39;UV multiples ne s’affichent pas lors de l’ouverture de fichiers FBX
* [UI] Libellés qui se chevauchent dans la barre d’état
* [UI] Les info-bulles du menu déroulant « Mode de création de lien » ne sont pas affichées

### PROBLÈMES CONNUS

* [Bakers] Crashs pendant le baking avec certains pilotes NVidia spécifiques
* [vue 3D] OpenGL : certaines scènes importées peuvent ne pas être rendues
* [vue 3D] Pixellisation : artefacts d’ombre lors de l’utilisation du displacement sur une Scène plate
* [vue 3D] Traceur de tracé : performances lentes lors de la mise à jour des textures avec la tessation/le displacement activé
* [vue 3D] Certaines propriétés de matériau de couleur ne sont pas gérées correctement lorsqu’elles sont remplacées
* [vue 3D] Les Scènes avec des primitives animées ne sont pas correctement prises en charge
* [vue 3D] Le Maillage avec plusieurs UDims n&#39;est pas encore pris en charge
* [vue 3D] Les Maillages avec plusieurs UV ne sont pas pris en charge et peuvent entraîner un rendu de matériau non valide
* [vue 3D] Pathtracer non pris en charge sur les cartes graphiques AMD
