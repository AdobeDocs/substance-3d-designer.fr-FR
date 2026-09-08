---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-main-toolbar.html"
breadcrumb-title: ''
description: Découvrez la barre d’outils principale de Substance 3D Designer pour accéder aux outils et commandes courants de votre workflow.
helpx_creative_field: ""
helpx_description: Designer > Interface > Main toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Barre d'outils principale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# La barre d’outils principale

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Cette page décrit la barre d&#39;outils principale et le menu de [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html), qui apparaissent en haut à gauche de la fenêtre principale.Il se compose de deux parties : les menus déroulants principaux et les boutons d’accès rapide. Toutes les fonctions du bouton d&#39;accès rapide sont également accessibles via les menus <b>Fichier</b> et <b>Modifier</b>.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Barre d&#39;outils principale](../../assets/mainmenu.png "Barre d&#39;outils principale")

</td>
</tr>
</table>

## Boutons d’accès rapide

![](../../assets/newsubstance.png) <b>Nouveau graphe de Substance...:</b> (Ctrl+N)Affiche la fenêtre [Nouveau graphe](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md), puis crée un pack avec un [graphe de Substance](../../compositing-graphs/substance-compositing-graphs.md).

![](../../assets/open.png) <b>Ouvrir...:</b> (Ctrl+O) Ouvrir un package de [Substances (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

![](../../assets/saveall.png) <b>Enregistrer tout :</b> (Ctrl+⇧+S) Enregistre tous les packages répertoriés dans l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md).

![](../../assets/undo.png) <b>Annuler :</b> (Ctrl+Z) Annuler la dernière opération.

![](../../assets/redo.png) <b>Rétablir :</b> (Ctrl+Y) Rétablir la dernière opération annulée.

## Fichier

<b>Nouveau :</b> ouvre un sous-menu pour créer un graphe ou un pack :

* <b>Nouveau graphe de Substance...:</b>(Ctrl+N) Vous présente la fenêtre [Nouveau graphe](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) qui vous permet de configurer un nouveau [graphe de Substance](../../compositing-graphs/substance-compositing-graphs.md) ;
* <b>Nouveau graphe de fonction de Substance :</b> crée un pack avec un [graphe de fonction de Substance](../../function-graphs/function-graphs.md) ;
* <b>Vide :</b> crée un package vide.

<b>Ouvrir...:</b> (Ctrl+O) Ouvrir un package de [Substances (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

<b>Packs récents :</b> affiche la liste des packs récemment ouverts. Cliquez sur une entrée pour l’ouvrir.

<b>Ouvrir les packages de la dernière session (#)</b> : ouvre tous les packages ouverts lors de la fermeture ou de la fin de la dernière session.

<b>Enregistrer tout :</b> (Ctrl+⇧+S) Enregistre tous les packages ouverts, y compris ceux chargés en arrière-plan.

<b>Tout fermer :</b> ferme tous les packs ouverts.

<b>Recharger les ressources :</b> force Designer à recharger [toutes les ressources, y compris les bitmaps et les données de SVG](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

<b>Quitter :</b> (Ctrl+Q) - Fermer Substance 3D Designer.

## Édition

<b>Annuler :</b> (Ctrl+Z) Annuler la dernière opération.

<b>Rétablir :</b> (Ctrl+Y) Rétablir la dernière opération annulée.

<b>Préférences...:</b> Ouvre la fenêtre Préférences.

>[!NOTE]
>
> Cette boîte de dialogue est accessible à partir du menu Substance 3D Designer dans la barre des tâches de macOS.

## Outils

<b>Annuler le rendu :</b> (Echap) arrête l&#39;opération en cours pour la Substance Engine. Peut être utilisé pour interrompre une opération lourde et indésirable.

<b>Suspendre le moteur :</b> (⇧+Echap) suspend le moteur de rendu. Cela peut accélérer la modification de [graphes de Substance](../../compositing-graphs/substance-compositing-graphs.md) complexes.

<b>Changer de moteur... :</b>(F9) offre un choix de moteurs de rendu, y compris les moteurs GPU (« DirectX » sous Windows, « OpenGL » sous macOS) ainsi que le moteur CPU (« NEON » sur Apple Silicon, « SSE » sur tous les autres).

<b>Substance Player :</b> gérez l’intégration de Designer avec Substance Player :

* <b>Localiser le lecteur...:</b> Indiquez à Designer où le lecteur est installé ;
* <b>Télécharger le lecteur...:</b> ouvre la [page de destination](https://helpx.adobe.com/substance-3d-player/home.html) de la documentation de la Substance Player de données, où vous pouvez télécharger le lecteur.

<b>Gestionnaire de plug-ins...</b> : ouvre la fenêtre Gestionnaire de plug-ins, dans laquelle vous pouvez installer, charger et décharger les [plug-ins Python pour Substance 3D Designer.](../../scripting/scripting.md)

## Windows

<b>Nouvel Explorateur :</b> ouvre un nouveau dock Explorateur. Plusieurs docks Explorateurs peuvent être ouverts.

<b>Nouvelle vue 3D :</b> ouvre un nouveau dock vue 3D. Plusieurs docks vue 3D peuvent être ouverts.

<b>Nouvelle vue Bibliothèque :</b> ouvre un nouveau dock de bibliothèque. Plusieurs docks de bibliothèque peuvent être ouverts.

<b>Éditeur Python :</b> ouvre l&#39;éditeur Python utilisé pour[évaluer et créer des scripts](../../scripting/scripting.md).

<b>Réinitialiser la disposition :</b> réinitialise l&#39;espace de travail à la disposition par défaut. Toutes les fenêtres seront réorganisées et certaines d’entre elles risquent d’être à nouveau masquées. À utiliser en cas de problèmes avec la disposition du programme.

<b>Annuler l&#39;agrandissement de la fenêtre :</b> lorsqu&#39;un panneau est *agrandi*, cette option l&#39;agrandit et restaure la disposition telle qu&#39;elle était *avant* l&#39;agrandissement de la fenêtre

<b>Explorateur :</b> affichez/masquez l&#39;[Explorateur](../the-explorer-window/the-explorer-window.md).

<b>Graphique :</b> afficher/masquer la ou les [fenêtre de graphique](../../interface/the-graph-view/the-graph-view.md).

<b>Paramètres :</b> affichez/masquez les [propriétés](../properties/properties.md).

<b>Console :</b> affichez/masquez la fenêtre de la console.

<b>Vue 3D :</b> affichez/masquez [vue(s) 3D](../../interface/3d-view/3d-view.md).

<b>Gestionnaire de dépendances :</b> affichez/masquez le [Gestionnaire de dépendances](../../interface/dependency-manager/dependency-manager.md).

<b>Vues 2D :</b> affichez/masquez la [vue 2D](../2d-view/2d-view.md).

<b>Bibliothèque :</b> affichez/masquez la [fenêtre de bibliothèque](../../interface/the-library/the-library.md).

<b>Barre d&#39;outils principale :</b> afficher/masquer la barre d&#39;outils principale (boutons d&#39;accès rapide uniquement).

>[!NOTE]
>
> Pour en savoir plus sur la gestion du panneau Designer, sa personnalisation et ses fonctionnalités d&#39;amélioration du workflow, accédez à la page [Personnalisation de votre espace de travail](../../interface/customizing-your-wor/customizing-your-workspace.md) de cette documentation.

## Aide

<b>Tutorials :</b> ouvre le site web [Substance 3D tutorials](https://substance3d.adobe.com/tutorials/) (anciennement Substance Academy).<b>\
</b>

<b>Notes de mise à jour :</b> ouvre une fenêtre avec le journal des modifications de la dernière version.

<b>Configuration requise :</b> présente la configuration requise pour exécuter l&#39;application.

<b>Documentation :</b> ouvre votre navigateur web par défaut sur [cette documentation](https://www.adobe.com/go/Substance-3D-doc-Designer_fr).

<b>Documentation sur les scripts :</b> ouvre votre navigateur web sur les documents API Python locaux.

<b>Forums...:</b> Ouvre votre navigateur web sur notre forum [Communauté d&#39;assistance](https://forum.substance3d.com/) pour entrer en contact avec la communauté et poser des questions.

<b>Signaler un bogue...:</b> Ouvrez la fenêtre de signalement des bogues.

<b>Exporter le journal... :</b> exporte les fichiers journaux actuels vers un fichier compressé (.zip), à fournir au support technique.

<b>Donner votre avis...:</b> Ouvre votre navigateur web sur la page d&#39;accueil de la [Communauté de support](https://www.adobe.com/go/Substance-3D-feedback-Designer_fr) d&#39;Adobe.

<b>Ressources Substance 3D :</b> parcourez [le contenu 3D premium](https://substance3d.adobe.com/assets) pour les abonnés (anciennement Substance Source).

<b>Ressources de la communauté Substance 3D :</b> vous permet de parcourir [les ressources gratuites de la communauté](https://substance3d.adobe.com/community-assets/) (anciennement Substance share).

<b>Gérer mon compte\*:</b> ouvre la page web de votre compte Adobe.

<b>Se connecter/se déconnecter...\*:</b> Vous permet de vous connecter/vous déconnecter de votre compte Adobe.

<b>Écran d’accueil...:</b> Affiche la boîte de dialogue [Écran d’accueil](../../interface/home-screen/home-screen.md).

<b>Nouveautés...:</b> affiche un écran qui met en évidence les fonctionnalités ajoutées à la dernière version de Designer

<b>Écran d’accueil...\*:</b> Affiche l’écran a qui guide les nouveaux utilisateurs à travers l’objectif de Designer et sa place dans l’[écosystème Substance 3D](https://helpx.adobe.com/substance-3d.html)

<b>Partenaires :</b> vous permet d&#39;accéder aux avis de non-responsabilité et aux avis pour les intégrations tierces de nos partenaires dans Designer.

<b>À propos de Substance 3D Designer...:</b> Affiche des informations sur l&#39;application et ses composants, telles que le numéro de version.

\* : ces options sont uniquement disponibles dans la version de Designer installée via [Adobe Creative Cloud pour poste de travail](https://creativecloud.adobe.com/en/apps/download/creative-cloud), qui nécessite un [abonnement Substance 3D](https://www.adobe.com/creativecloud/plans.html?amp%3Bplan=individual#filter=3dar).
