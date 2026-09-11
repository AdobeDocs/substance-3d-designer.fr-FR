---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-12-4.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 1%

---


# Version 12.4

**Substance 3D Designer 12.4** apporte plusieurs améliorations à la qualité de vie (un outil pour nettoyer un graphe, utiliser des formules de base pour définir des paramètres, un bouton pour générer une vitesse aléatoire, un verrou pour la taille, etc.) et la prise en charge des Graphes Substance models dans l’API Python. Voir ci-dessous pour plus de détails sur toutes ces modifications.

Date de publication : *31 janvier 2023*

## Amélioration de la qualité de vie

### Outil Nettoyer le graphe

Lorsque vous modifiez votre graphe, vous devez parfois expérimenter plusieurs possibilités, et brancher / débrancher divers nœuds jusqu&#39;au moment où vous obtenez le résultat que vous voulez. Enfin, certains nœuds de votre graphe ne sont pas connectés à une sortie et n’ont donc aucun impact sur le résultat final. Ce nouvel outil vous permettra de détecter et de supprimer automatiquement ces nœuds afin de nettoyer vos graphes avant de les finaliser. L&#39;outil de nettoyage est également disponible en option dans les fonctions de paramètres, et peut être lancé sur le graphe courant via le bouton dédié dans la barre d&#39;outils de Vue du graphe, ou sur une sélection de graphes à partir de la vue Explorateur.

![](../../assets/final-clean.gif){width="640px"}

### Saisir des formules dans les champs de paramètres

Plus besoin d&#39;utiliser une calculatrice ou de calculer dans votre tête lorsque vous voulez entrer des valeurs de paramètres spécifiques. Vous pouvez désormais saisir directement des formules de base telles que les additions, les divisions, les multiplications ou les soustractions lors de la définition d&#39;une valeur numérique pour un paramètre dans les Propriétés et à d&#39;autres endroits dans l&#39;application.

![](../../assets/final-formula.gif){width="640px"}

### Boutons d’accès rapide dans la vue 3D

Nous avons ajouté une barre d&#39;outils supplémentaire dans la [vue 3D](../../interface/3d-view/3d-view.md) correspondant à toutes les options disponibles dans le menu [Affichage](../../interface/3d-view/3d-view.md), pour un accès rapide à toutes ces options (par exemple, Structure filaire, Grille, Cadre de sélection, etc.) lorsque le bouton bascule. Nous avons également ajouté un bouton pour afficher/masquer la map d&#39;environnement.

![](../../assets/final-3dview.gif){width="640px"}

### Bouton permettant de générer une valeur de départ aléatoire

Vous pouvez désormais créer rapidement différentes variations à l’aide d’un nouveau bouton pour générer la valeur de départ aléatoire de votre graphe, au lieu de déplacer un curseur.

![](../../assets/final-seed.gif){width="640px"}

### Verrouillage du widget Taille de sortie

Vous pouvez désormais verrouiller la largeur et l’height de la taille de sortie afin de vous assurer de conserver une taille carrée et d’éviter de manipuler les deux valeurs à chaque mise à jour.

![](../../assets/final-lock.gif){width="640px"}

### Transformer la saisie de l’image sur Couleur/Niveaux de gris

Basculez rapidement entre une [couleur d&#39;entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) et une [échelle de gris d&#39;entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) via le menu contextuel du nœud.

![](../../assets/final-switch.gif){width="640px"}

### Sélectionner l’épingle sélectionnée lors de l’affichage de l’Éditeur de dégradé

Dans le panneau des propriétés, si vous cliquez sur une épingle pour modifier un dégradé, vous allez maintenant sélectionner automatiquement l&#39;épingle correspondante dans l&#39;[Éditeur de dégradé](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) affiché.

![](../../assets/final-gradient.gif){width="640px"}

### Sélectionner les nœuds en aval

Nouvelle entrée dans le [menu contextuel des nœuds](../../interface/the-graph-view/the-graph-view.md) pour sélectionner tous les nœuds connectés à la sortie du ou des nœuds sélectionnés, directement ou indirectement. Vous devez donc sélectionner tous les nœuds affectés par votre nœud. Utile pour supprimer une partie de votre graphe ou retravailler la disposition du graphe.

![](../../assets/final-downstream.gif){width="640px"}

## Mises à jour de l’API Python

Cette version 12.4 apporte également la prise en charge complète des Graphes Substance models via l&#39;API Python. Cela signifie que vous disposez désormais de tous les outils nécessaires pour créer, modifier ou évaluer des Graphes Substance models. Pour plus d’informations, consultez la documentation disponible dans le menu Aide du logiciel.

## Notes de mise à jour

### 12.4.0

*(Publié Le 24 Janvier 2023)*

<b>Ajouté :</b>

* [vue 3D] Ajoutez des boutons d’accès rapide pour définir les options d’affichage (Structure filaire, map d&#39;environnement, état des scènes, etc.)
* [Gestion des couleurs] Amélioration de la qualité des tables LUT 3D bakées en mode ACE
* [Documentation] Exemples de projets pour les graphes de Substance
* [Documentation] Projet d’exemple pour les graphes de fonction
* [Explorateur] Autoriser le déplacement du Graphe et des ressources d’un parent à un autre sans fermer ni invalider les widgets
* [Éditeur de dégradé] Sélectionnez l’épingle sélectionnée lors de l’affichage de l’éditeur de dégradé
* [Graphe] Ajouter une option dans le menu contextuel d’un nœud pour sélectionner tous ses enfants
* [Graphe] Nettoyer l&#39;outil de graphe pour détecter et supprimer les nœuds inutilisés dans tous les types de graphes et graphes de propriétés
* [Graphe] Transformer l’entrée d’image sur couleur/niveaux de gris
* [Paramètres] Ajouter un verrou sur les widgets entier 2
* [Paramètres] Permet de saisir des formules de base comme paramètre
* [Substance] Basculez entre les valeurs et les icônes pour les nœuds de valeur.
* [UI] Bouton permettant de générer une valeur aléatoire lorsqu’un générateur aléatoire est requis
* [UI] Mettez en surbrillance dans la vue 3D l’élément actuellement sélectionné dans l’Explorateur de Scènes
* [UX] Réinitialiser les plages de curseur lorsque leur valeur est réinitialisée
* [API] Autoriser l’ajout d’actions aux barres d’outils de vue du graphe
* [API] Autoriser à créer/modifier/évaluer un Graphe Substance model à partir de l’API

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
