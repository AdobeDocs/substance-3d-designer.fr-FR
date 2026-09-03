---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/release-notes/version-12-4.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 12.4 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 12.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 1%

---


# Version 12.4

**Substance 3D Designer 12.4** apporte plusieurs améliorations à la qualité de vie (un outil pour nettoyer un graphique, utiliser des formules de base pour définir des paramètres, un bouton pour générer une vitesse aléatoire, un verrou pour la taille, etc.) et la prise en charge des graphiques de Substance de données dans l’API Python. Voir ci-dessous pour plus de détails sur toutes ces modifications.

Date de publication : *31 janvier 2023*

## Amélioration de la qualité de vie

### Outil Nettoyer le graphe

Lorsque vous modifiez votre graphique, vous devez parfois expérimenter plusieurs possibilités, et brancher / débrancher divers nœuds jusqu&#39;au moment où vous obtenez le résultat que vous voulez. À la fin, certains nœuds de votre graphique ne sont pas connectés à une sortie et n’ont donc aucun impact sur le résultat final. Ce nouvel outil vous permettra de détecter et de supprimer automatiquement ces nœuds afin de nettoyer vos graphiques avant de les finaliser. L’outil de nettoyage est également disponible en option dans les fonctions de paramètres. Il peut être lancé sur le graphique actuel via le bouton dédié de la barre d’outils Vue graphique ou sur une sélection de graphiques dans la vue Explorateur.

![](version-12-4.resources/version-12-4-01.gif){width="640px"}

### Saisir des formules dans les champs de paramètres

Plus besoin d&#39;utiliser une calculatrice ou de calculer dans votre tête lorsque vous voulez entrer des valeurs de paramètres spécifiques. Vous pouvez désormais saisir directement des formules de base telles que les additions, les divisions, les multiplications ou les soustractions lors de la définition d&#39;une valeur numérique pour un paramètre dans les Propriétés et à d&#39;autres endroits dans l&#39;application.

![](version-12-4.resources/version-12-4-02.gif){width="640px"}

### Boutons d’accès rapide dans la vue 3D

Nous avons ajouté une barre d&#39;outils supplémentaire dans la [vue 3D](../../interface/3d-view/3d-view.md) correspondant à toutes les options disponibles dans le menu [Affichage](../../interface/3d-view/3d-view.md), pour un accès rapide à toutes ces options (par exemple, Structure filaire, Grille, Cadre de sélection, etc.) lorsque le bouton bascule. Nous avons également ajouté un bouton pour afficher/masquer la carte d’environnement.

![](version-12-4.resources/version-12-4-03.gif){width="640px"}

### Bouton permettant de générer une valeur de départ aléatoire

Vous pouvez désormais créer rapidement différentes variations à l’aide d’un nouveau bouton pour générer la vitesse aléatoire de votre graphique, au lieu de déplacer un curseur.

![](version-12-4.resources/version-12-4-04.gif){width="640px"}

### Verrouillage du widget Taille de sortie

Vous pouvez désormais verrouiller la largeur et l’height de la taille de sortie afin de vous assurer de conserver une taille carrée et d’éviter de manipuler les deux valeurs à chaque mise à jour.

![](version-12-4.resources/version-12-4-05.gif){width="640px"}

### Transformation de l’entrée d’image en couleur/niveaux de gris

Basculez rapidement entre une [couleur d&#39;entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) et une [échelle de gris d&#39;entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) via le menu contextuel du nœud.

![](version-12-4.resources/version-12-4-06.gif){width="640px"}

### Sélectionner l’épingle sélectionnée lors de l’affichage de l’Éditeur de dégradé

Dans le panneau des propriétés, si vous cliquez sur une épingle pour modifier un dégradé, vous allez maintenant sélectionner automatiquement l&#39;épingle correspondante dans l&#39;[Éditeur de dégradé](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) affiché.

![](version-12-4.resources/version-12-4-07.gif){width="640px"}

### Sélectionner les nœuds en aval

Nouvelle entrée dans le [menu contextuel des nœuds](../../interface/the-graph-view/the-graph-view.md) pour sélectionner tous les nœuds connectés à la sortie du ou des nœuds sélectionnés, directement ou indirectement. Vous devez donc sélectionner tous les nœuds affectés par votre nœud. Utile pour supprimer une partie de votre graphique ou pour retravailler la mise en page du graphique.

![](version-12-4.resources/version-12-4-08.gif){width="640px"}

## Mises à jour de l’API Python

Cette version 12.4 offre également la prise en charge complète des graphiques de Substance de données via l’API Python. Cela signifie que vous disposez désormais de tous les outils nécessaires pour créer, modifier ou évaluer des graphiques de modèles de Substance. Pour plus d’informations, consultez la documentation disponible dans le menu Aide du logiciel.

## Notes de mise à jour

### 12.4.0

*(Publié Le 24 Janvier 2023)*

<b>Ajouté :</b>

* [Vue 3D] Ajoutez des boutons d’accès rapide pour définir les options d’affichage (Structure filaire, carte d’environnement, statistiques de scène, etc.)
* [Gestion des couleurs] Amélioration de la qualité des tables LUT 3D cuites en mode ACE
* [Documentation] Exemples de projets pour les graphiques de Substance
* [Documentation] Exemple de projet pour les graphiques de fonction
* [Explorer] Autoriser le déplacement du graphique et des ressources d’un parent à un autre sans fermer ni invalider les widgets
* [Éditeur de dégradé] Sélectionner l’épingle sur laquelle vous avez cliqué lors de l’affichage de l’éditeur de dégradé
* [Graphique] Ajouter une option dans le menu contextuel d’un nœud pour sélectionner tous ses enfants
* [Graphique] Nettoyer l’outil de graphique pour détecter et supprimer les nœuds inutilisés dans tous les types de graphiques et graphiques de propriétés
* [Graphique] Transformation de l’entrée d’image en couleur/niveaux de gris
* [Paramètres] Ajouter un verrou sur les widgets integer2
* [Paramètres] Permet de saisir des formules de base comme paramètre
* [Substance] Basculez entre les valeurs et les icônes pour les nœuds de valeur.
* [UI] Bouton permettant de générer une valeur aléatoire lorsqu’un générateur aléatoire est requis
* [UI] Mettez en surbrillance dans la vue 3D l’élément actuellement sélectionné dans l’Explorateur de scènes
* [UX] Réinitialiser les plages de curseur lorsque leur valeur est réinitialisée
* [API] Autoriser l’ajout d’actions aux barres d’outils d’affichage des graphiques
* [API] Autoriser la création/modification/évaluation d’un graphique de modèle de Substance à partir de l’API

<b>Fixe :</b>

* [vue 3D] La valeur de la propriété « Normal » n’est pas partagée entre les moteurs de rendu
* [vue 3D] L&#39;affichage des statistiques de Scène est étiré lorsque le viewport est petit
* [vue 3D] La propriété d&#39;affichage Structure filaire n&#39;est pas enregistrée
* [Contenu] Les paramètres Couleur de flou radial n’ont aucun effet sur le canal Alpha
* [Localisation] Des curseurs et des boutons supplémentaires s’affichent dans les propriétés OpenGL de l’environnement.
* crash [MDL]&#x200B;[modèle de Substance] lors de la suppression de nœuds exposés
* [Préférences] Le fichier par défaut\_config n’est jamais recréé s’il est supprimé
* Paramètre de réorganisation de Crash [modèle de Substance] qui n&#39;apparaît pas au niveau de l&#39;instance
* [API] SDProperty.getDefaultValue() renvoie presque toujours None
