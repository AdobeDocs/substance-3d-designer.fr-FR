---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-12-3.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 12.3 pour en savoir plus sur les nouvelles fonctionnalités, les améliorations et les correctifs de bogues.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 12.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---


# Version 12.3

<b>Substance 3D Designer 12.3</b> donne une nouvelle dimension aux graphiques de Substances avec la <b>prise en charge des sous-graphes</b> (ou des instances de graphiques), plus<b> &#39;Visible if&#39; </b>contrôle des paramètres exposés et de certains<b> nouveaux nœuds</b> dédiés à l&#39;édition des courbes. Cette version introduit également deux nouveaux panneaux (<b>Bienvenue </b> et <b>Nouveautés</b>) pour améliorer l’intégration des utilisateurs, ainsi que d’autres fonctionnalités mineures ou correctifs de bogues décrits ci-dessous.

Date de publication : *6 octobre 2022*

![](version-12-3.resources/version-12-3-01.png){width="1111px"}

## Principales fonctionnalités

### Prise en charge des instances de graphiques dans les graphiques de modèles de Substance

Si vous avez l’habitude de créer des graphes, vous voulez être en mesure de créer des sous-graphes (ou des instances de graphes) afin de réutiliser votre travail, de rendre les graphes moins encombrés et plus efficaces.\
Cela est désormais possible également pour les graphiques de Substance de données : il vous suffit de glisser-déposer votre sous-graphe de l’Explorateur vers votre graphique principal pour l’utiliser en tant que nœud d’instance.

![](version-12-3.resources/version-12-3-02.gif){width="600px"}

Nous avons également introduit le concept de nœuds de sortie pour les graphiques de modèles de Substance, tels que Scène de sortie. Vous avez maintenant la possibilité d’avoir une ou plusieurs sorties dans votre graphique.\
Chaque sortie correspondra à une broche de sortie lorsque votre graphique sera instancié dans un autre graphique.

![](version-12-3.resources/version-12-3-03.png){width="600px"}

Lorsque vous cliquez avec le bouton droit sur un nœud d&#39;instance, vous pouvez bien sûr accéder à son sous-graphe référencé afin de le visualiser ou de le modifier.

![](version-12-3.resources/version-12-3-04.png){width="600px"}

Grâce aux sous-graphes et aux paramètres exposés, vous pouvez créer des actifs complexes et appliquer des variations infinies, comme le montre l’illustration ci-dessous.

![](version-12-3.resources/version-12-3-05.gif){width="600px"}

### Autres améliorations apportées aux graphiques de modèles de Substance

* <b>Visible si pour les paramètres exposés</b>\
  Lors de l’exposition de paramètres, vous pouvez masquer ou afficher des paramètres en fonction de l’état d’autres paramètres. Par exemple, un curseur s’affiche uniquement lorsqu’un bouton est activé.\
  Avec <b>Visible si</b>, vous pouvez ajouter des conditions à la visibilité des paramètres, en conservant une interface utilisateur propre et fonctionnelle. Ce mécanisme déjà disponible pour les graphes en Substance est maintenant étendu aux graphes en Substance, en utilisant bien entendu la même syntaxe. <b>\
  </b>

  ![](version-12-3.resources/version-12-3-06.gif){width="600px"}

* <b>Nouveaux nœuds dédiés à l’édition des courbes\
  </b>Cette version apporte de nouveaux nœuds dédiés à l&#39;édition des courbes : la <b>courbe inverse</b> échange les deux extrémités d&#39;une courbe, la <b>subdivision de courbe</b> ajoute plus de sommets sur les segments selon deux méthodes, la <b>courbe de lissage</b> lisse tous les angles sur une courbe 2D et enfin la <b>courbe de décalage</b> gonfle ou dégonfle une courbe 2D, comme indiqué ci-dessous.<b>

  </b>

  ![](version-12-3.resources/version-12-3-07.gif){width="600px"}
* <b>Nouvelle fenêtre graphique </b>\
  La fenêtre <b>Nouveau graphique de modèle de Substance</b> est désormais également disponible pour les graphiques de modèle de Substance. Vous pouvez ajouter vos propres modèles ou sélectionner un modèle par défaut, puis saisir directement le nom de votre graphique et sélectionner le package auquel le graphique sera ajouté.

  ![](version-12-3.resources/version-12-3-08.png){width="600px"}

### Panneaux Bienvenue et Nouveautés

Nous avons introduit deux nouveaux panneaux pour vous aider à prendre en main Designer :

Tout d&#39;abord, le panneau <b>Bienvenue</b>, affiché la première fois que vous *lancez* Designer, offre une vue d&#39;ensemble globale du logiciel et de son rôle dans l&#39;écosystème Substance 3D. Ensuite, le panneau <b>Nouveautés</b>, qui s&#39;affiche la première fois que vous exécutez une *nouvelle version* de Designer, présente rapidement les principales fonctionnalités introduites dans cette version.

Ces deux panneaux sont également accessibles à partir du menu Aide.

![](version-12-3.resources/version-12-3-09.png)

![](version-12-3.resources/version-12-3-10.png)

### Divers

* <b>Widget à deux boutons pour les paramètres booléens exposés</b>\
  Vous disposez maintenant d&#39;une nouvelle façon d&#39;exposer des paramètres booléens dans un graphe de Substance. En plus du bouton de permutation, vous pouvez utiliser des <b>boutons côte à côte</b> avec des textes personnalisés afin de rendre plus visibles les deux modes différents pilotés par le paramètre booléen.
* <b>Résoudre les problèmes de mise à l’échelle des écrans haute résolution </b>\
  Dans les versions précédentes, Designer ne pouvait pas gérer correctement le facteur de mise à l’échelle défini dans le système d’exploitation. Comme vous pouvez le voir dans l’illustration ci-dessous, tout est parfaitement géré sur un écran 4K avec une mise à l’échelle de 125 %, toutes les polices et tous les boutons étant affichés à une taille cohérente.\
  Notez que l&#39;option « Désactiver la haute résolution » dans les Préférences a été réinitialisée sur *Faux* dans cette nouvelle version, car cette option n&#39;est plus nécessaire pour avoir une interface utilisable.

  ![](version-12-3.resources/version-12-3-11.gif){width="600px"}

* **Prise en charge native d’Apple Silicon (M1/M2) pour Steam version**\
  La version 12.2 de Designer a été la première à offrir une prise en charge complète des nouveaux ordinateurs Apple équipés de puces M1 ou M2, mais cette prise en charge était absente de l’édition Steam. Désormais, tous les utilisateurs de Designer peuvent bénéficier d’une expérience plus rapide et plus efficace sur ces ordinateurs.

## Notes de mise à jour

### 12.3.0

*(Publié Le 6 Octobre 2022)*

**Ajouté :**

* [Général] Panneau d’intégration pour accueillir les nouveaux utilisateurs
* [Général] Panneau Nouveautés pour améliorer la découvrabilité des nouvelles fonctionnalités
* [Modèle de Substance] Prise en charge des sous-graphes et des instances
* [Modèle de Substance] Prise en charge Visible Si pour les paramètres exposés
* [Modèle de Substance] Ajout de la prise en charge des nœuds de sortie
* [modèle de Substance] Nœud de décalage de courbe
* [modèle de Substance] Nœud de retournement de courbe
* [modèle de Substance] Nœud de lissage de courbe
* [modèle de Substance] Nœud de subdivision de courbe
* [modèle de Substance] Nœud de greffe
* [Substance model] Mettre à jour le nœud « Filter Scene »
* [Modèle de Substance] Rendre les nœuds non atomiques détectables dans le menu Nœud
* [Substance de données] Ajoutez l&#39;action « Ouvrir la référence » dans le menu contextuel d&#39;un nœud d&#39;instance
* [Modèle de Substance] Ajoutez une action « Afficher dans 3DView » dans le menu contextuel des nœuds pouvant être envoyés à 3DView
* [Modèle de Substance] Affiche automatiquement les propriétés d&#39;un nœud après l&#39;avoir exposé
* [Modèle de Substance] Création d’une fenêtre « Nouveau graphique de modèle de Substance » avec la liste des modèles
* [UI] Amélioration de la cohérence des options d’enregistrement d’image dans les vues 2D et 3D
* [UI] Renommez « Lien > Filet 3D » en « Lien > Scène 3D » dans le menu contextuel de l’Explorateur
* [UI] La réinitialisation de la disposition s’applique désormais à toutes les fenêtres flottantes
* [UI] Utiliser le libellé « Afficher les sorties en vue 3D » dans les menus contextuels des graphiques
* [Library] Prise en charge des graphiques de modèles de Substance non atomiques
* [SBSAR] Prise en charge de la description des sorties graphiques dans le SBSAR
* [Shader] Définissez la valeur par défaut Facteur de facettisation sur 1 pour tous les shaders
* [UI] Exposer le widget à 2 boutons pour les paramètres booléens
* [Engine] Mise à jour vers la version 8.6.4
* [Steam] Version optimisée pour le chipset Apple Silicon (Apple M1/M2)

**Fixe :**

* [UI] Résolution des problèmes de mise à l’échelle des écrans haute résolution
* [UI] Modèle &#39;$(udim)&#39; manquant dans la liste de la fenêtre de restauration
* [UI] Blocage lors de l’affichage du menu Nœud sur la bordure droite de l’écran (macOS uniquement)
* [UI] Le bouton Extension dans le menu de la vue 3D n’est pas visible
* [UI] Le menu d&#39;extension de la barre d&#39;outils Graphique est incomplet
* [UI] Valeur de widget de paramètre incorrecte après l’annulation de l’activation de la plage fixe
* [Vue 3D] Le paramètre de nuanceur non par défaut est perdu sur Iray d’une session à une autre
* [Boulangers] Blocage lors du chargement d’une fenêtre de boulangerie avec une scène sans maillages
* [Fonction] Blocage lors de la copie d’une instance dans son graphique référencé
* [Fonction] Correction d’un blocage possible lors de la manipulation des nœuds
* [Globalisation] L’italique n’est pas toujours correctement désactivé en japonais/coréen/chinois
* [Graphique] Identificateur de secours incorrect pour les nouveaux graphiques de modèles de Substance et MDL.
* [Graphique] Les paramètres hérités pilotés par des valeurs sont parfois calculés de manière incorrecte
* [GraphRender] Blocage lors du changement de moteur lors du calcul d’un graphique haute résolution (macOS uniquement)
