---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-11-3.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 11.3 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 11.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 11.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: dca126adc56c78e85d281a00f90cf9affbb35c31
workflow-type: tm+mt
source-wordcount: '1284'
ht-degree: 1%

---


# Version 11.3

**Substance 3D Designer**

Date de publication : *24 novembre 2021*

## Fonctionnalité majeure

### Nouvelles fonctionnalités de graphe model

![](version-11-3.resources/banner-model.jpg)

De nombreuses améliorations ont été apportées au graphe model pour étendre les capacités de modélisation :

* <b>Nouveau workflow de particule</b>\
  Le nouveau workflow de modélisation de particule permet de créer des nuages de points pour manipuler la géométrie. Ils peuvent être utilisés pour créer de nombreuses nouvelles formes complexes et/ou répétitives, telles que les tuiles du toit sur l’image juste au-dessus.\
  Pour en savoir plus sur le nouveau workflow de particule, consultez les pages de documentation suivantes :

  * Types d’éléments dans une scène
  * Particules
  * Rognage de particule
  * Particules d&#39;instances

  ![](version-11-3.resources/particle-pruning.gif)

* <b>Nouveaux nœuds de modélisation et de déformation</b>\
  D’autres nœuds ont été ajoutés pour créer des formes plus complexes. Cliquez sur chaque nœud pour en savoir plus :
  * Transformation générative
  * Motif organique
  * Tour
  * Rognage de courbe

* <b>Améliorations générales\
  </b>Le workflow autour du graphe de modélisation a été amélioré avec :
  * Nouvelles info-bulles sur les paramètres des nœuds pour faciliter leur apprentissage.
  * La hiérarchie du modèle 3D est désormais conservée lors de l’exportation au format FBX
  * L’affectation de matériau peut être exportée aux formats de fichier OBJ et FBX.
  * Prévisualisation des nœuds intermédiaires dans le viewport en mode d’incrustation.

### Interopérabilité améliorée

![](version-11-3.resources/banner-sendto.jpg)

Les actions d&#39;envoi ont été étendues, avec deux nouvelles possibilités :

* **Envoyer SBSM (fichier de modèle substance) à Stager**\
  Les modèles 3D procéduraux peuvent désormais être envoyés à Stager et modifiés à partir de là avec les paramètres exposés.

* **Recevoir SBS/SBSAR de Sampler**\
  Il est désormais possible de recevoir des fichiers de Substance générés par Sampler directement dans Designer.

### Divers

![](version-11-3.resources/banner-misc-3.jpg)

Diverses améliorations ont été apportées à la qualité de vie :

* **Entrées par rapport aux entrées**\
  Les entrées de graphe définies sur Relative aux entrées hériteront désormais de la taille du nœud connecté au lieu de la taille du graphe parent par défaut. Cela facilite considérablement la gestion des différentes résolutions via des entrées de tailles différentes.

  ![](version-11-3.resources/relative-to-inputs.jpg){width="400px"}

* **Nouvelle fenêtre de graphe**\
  La nouvelle fenêtre de graphe a été retravaillée et permet désormais de mieux voir les détails d’un modèle spécifique et de créer un nouveau graphe directement dans un pack existant.

  ![](version-11-3.resources/new-graph.png){width="400px"}

* **Fermer tous les packages**\
  Une petite action qui rend moins fastidieux de gérer de nombreux paquets dans l&#39;explorateur. Utilisez **Fichier** > **Fermer tout** pour fermer tous les packs actuellement ouverts.

  ![](version-11-3.resources/close-all-packages.png)

* **Agrandir la vue actuelle**\
  Utilisez la nouvelle icône de barre de titre **icône** ou le raccourci **MAJ+Espace** pour développer une fenêtre en plein écran. Cela peut également être utilisé sur une fenêtre flottante.

* **Améliorations de la vue 3D**\
  La vue 3D dispose de nouveaux paramètres d’affichage pour basculer entre l’affichage des faces arrières sur un mannequin 3D et l’affichage des Vertex, des Tangentes et des bitangents.

### Contenu

![](version-11-3.resources/render-content.jpg)

Cette version ajoute de nouveaux nœuds de diffusion et des améliorations pour le nœud Rendu PBR :

* <b>Nœuds de Diffusion</b>\
  Les nouveaux nœuds d’UV Couleur de Diffusion, Gris de Diffusion et Diffusion permettent de générer des flous de débordement légers à partir d’un masque d’entrée.

  ![](version-11-3.resources/diffusion-normal.jpg){width="230px"}

  ![](version-11-3.resources/diffusion-grayscale.jpg) ![](version-11-3.resources/diffusion-uv.jpg)

* **Nœud de Rendu PBR amélioré**\
  Ce nœud a subi les modifications suivantes :
  * Nouveau mode UV cubique pour la forme Sphère.
  * Nouvelle prise en charge de la Subsurface scattering.
  * L’Anisotropie suit désormais le modèle du Matériau de toron d’Adobe (5ASM).
  * L’éclairage basé sur l’image a été amélioré grâce à l’échantillonnage de l’importance.
  * L’éclairage de l’Emissive a été amélioré grâce à l’échantillonnage de l’importance.

## Notes de mise à jour

### 11.3.0

*(Publié Le 24 Novembre 2021)*

**Ajouté :**

* [Modèles de Substance] Ajout d’info-bulles pour les paramètres des nœuds
* [Modèles de Substance] Permet d&#39;afficher en superposition dans le viewport 3D le résultat d&#39;un nœud intermédiaire
* [Modèles de Substance] Amélioration de l’affichage des bases
* [Modèles de Substance] Conservez la hiérarchie des objets lors de l’exportation d’un Graphe Substance model au format .fbx
* [Modèles de Substance] Prise en charge de plusieurs matériaux lors de l’exportation FBX/OBJ à partir du Graphe Substance model
* [Modèles de Substance]&#x200B;[Contenu] Nœud de Particule
* [Modèles de Substance]&#x200B;[Contenu] Nœud de Transforme générative
* [Modèles de Substance]&#x200B;[Contenu] Nœud Motif organique
* [Modèles de Substance]&#x200B;[Contenu] Particules du nœud Instances
* [Modèles de Substance]&#x200B;[Contenu] Nœud d&#39;élagage de Particule
* [Modèles de Substance]&#x200B;[Contenu] Nœud de tour
* [Modèles de Substance]&#x200B;[Contenu] Nœud Shell
* [Modèles de Substance]&#x200B;[Contenu] Nœud de Projection
* [Modèles de Substance]&#x200B;[Contenu] Nœud de rognage de courbe
* [Modèles de Substance]&#x200B;[Contenu] Mettre à jour le nœud Curve Sampler
* [Modèles de Substance]&#x200B;[Contenu] Mettre à jour le nœud Sampler du Maillage
* [Modèles de Substance]&#x200B;[Contenu] Mettre à jour le nœud de Variation
* [UX] Bouton pour agrandir la vue actuelle
* [UX] Mettre à jour la fenêtre Nouveau Graphe
* [UX] Ajouter l&#39;option « Télécharger le lecteur » dans le menu Outils et l&#39;agréger avec « Localiser le lecteur »
* [UX] Ajouter l’entrée « Tout fermer » au menu Fichier
* [UX] Appliquer la même casse dans tout le menu principal
* [UX] Afficher automatiquement les propriétés des éléments de graphe dupliqués
* [UX] Ajoutez des boutons dans la barre d’outils graphe pour désactiver la taille d’écran constante pour les titres / commentaires / Épingles du Cadre
* [UX] Boutons pour copier les informations de version dans le Presse-papiers dans la boîte de dialogue À propos
* [Matériaux] Entrées relatives aux entrées
* [Contenu] Ajout de l’option « Répétition » sur les Bruits Perlin 3D
* [Contenu] Nouveau nœud de processus de Diffusion
* [Contenu] Nouvelle version du nœud de Rendu PBR
* [Interopérabilité] Recevoir SBS et SBSAR de Sampler
* [Interopérabilité] Envoyer SBSM à Stager
* [vue 3D] Ajout d’une option pour désactiver backface culling
* [vue 3D] Ajout d’une option pour afficher l’espace de tangente du Vertex
* [Explorateur] Mettez en surbrillance le graphe dans l’Explorateur lorsque vous double-cliquez sur l’arrière-plan de la Vue du graphe
* [Explorateur] Supprimer l’option « Explorer » dans les menus contextuels
* [Bakers] Masquer les bakers obsolètes
* [Gestion des couleurs] Prise en charge des règles du fichier de configuration OCIO v2
* [Bibliothèque] Renommer les catégories en fonction des types de graphe
* [Préférences] Désactivez automatiquement le processeur dans les préférences de Périphériques pour Iray si un GPU CUDA pris en charge est détecté

**Fixe :**

* [modèles de Substance] Crash sur Mac lors de l’utilisation de l’option « as sudb » sur .fbx
* [modèles de Substance] Crash lors de l’exportation vers SBSM dans un cas spécifique
* [Modèles de Substance] Échec de l’exportation lors de l’exportation de paramètres exposés dont les widgets n’ont jamais été créés
* [Modèles de Substance] crash aléatoire lors de l’ouverture d’un graphe faisant référence à plusieurs fichiers .fbx
* [Modèles de Substance] Les plages ne sont pas appliquées dynamiquement dans les widgets de paramètre exposé
* [Modèles de Substance] L’option Recharger le maillage ne fonctionne pas sur les ressources utilisées dans le graphe des modèles de Substance
* [modèles de Substance] les Scènes ne sont pas affichées dans une vue 3D disponible dans un cas spécifique
* [UI] La zone Désactiver est trop grande dans les options de matériau
* [UI] Problème de style dans la boîte de dialogue « Fichier de package non enregistré »
* [UI] Appuyez deux fois sur la touche de tabulation pour naviguer entre les valeurs.
* [UI] Le zoom avec le glissement de la souris est inversé entre vue 3D et les autres Viewports
* [UI] Le chargement d’un fichier SBS déjà ouvert à l’aide de la liste « Fichiers récents » déclenche une invite « Package introuvable »
* [UI]&#x200B;[macOS] Disposition d’interface par défaut incorrecte après le démarrage de l’application
* [UI] Les packages ne peuvent pas être enregistrés à la racine d’un lecteur (Windows uniquement)
* [Graphe] L’option « Afficher automatiquement dans vue 2D » est incohérente dans un cas spécifique.
* [Graphe] L’option « Ouvrir la référence » est disponible pour les instanciers SBSAR
* [Graphe] Les propriétés d’Épingle ne s’affichent que lors de la création de l’élément
* [Graphe] Les règles de chaîne d&#39;Épingle sont appliquées de manière incohérente
* [Graphe] Crash lors de l’enregistrement d’un graphe vide
* [vue 3D] Anisotropy angle inversée dans ASM shader
* [vue 3D] Shader ASM : problèmes de linéarisation avec les cartes liées à SSS
* [vue 3D] Rendu OpenGL rompu après la fermeture de vues 3D supplémentaires dans un cas spécifique
* [vue 3D] Les positions des caméras prédéfinies ne sont pas correctes dans la vue 3D avec certains fichiers .fbx
* [MDL] L’option « Ajouter un nœud » du menu contextuel ne fonctionne pas pour les Graphes MDL
* [MDL] Bogue : la connexion du nœud échoue lors de l’utilisation de composants float2.x et similaires (SD 11.1.2)
* [MDL] Crash à l’ouverture du fichier specific.sbs
* [MDL] Unités de Scène par mètre en Iray non définies au début de la session de rendu
* [MDL] Se bloque lors de l’ajustement d’un nœud lerp dans le Graphe MDL
* [MDL] Ordre des paramètres dans le code MDL exporté
* [Explorateur] un dossier de ressources vide est créé après l&#39;annulation de la création de la ressource
* [Explorateur] Seul le premier élément d’un pack peut être déplacé au bas de la liste
* [Content] RT Bent Normal et RT AO déclenchent un calcul de nœud dans les graphes imbriqués
* [Noeud d&#39;entrée] Le bitmap dans Noeud d&#39;entrée n’est pas mis à jour lorsque l’UDIM change
* [Iray] L&#39;affichage d&#39;une Scène de modèles de Substance de données avec beaucoup d&#39;instances prend beaucoup de temps
* [Préférences] Ligne vide lors de l’annulation de l’ajout d’un fichier de projet
* [Éditeur Python] L’option « Fermer » reste activée après la fermeture du dernier script et inclut toujours son nom e
