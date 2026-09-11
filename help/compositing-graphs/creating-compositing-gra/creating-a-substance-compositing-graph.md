---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph.html"
breadcrumb-title: ''
description: Apprenez à créer des graphes de composition de Substances dans Substance 3D Designer pour créer des workflows de texture procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Creating a Substance graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Création d’un graphe Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 1%

---


# Création d’un graphe Substance

Les textures de création dans Designer commencent par la création d’un graphe de Substance de données, à partir d’un modèle prédéfini ou d’un graphe vide.

<a name="create-graph"></a>

## Création d’un graphe

Pour commencer le processus de création d&#39;un nouveau [graphe de Substance](../../compositing-graphs/substance-compositing-graphs.md), vous pouvez utiliser l&#39;une des méthodes suivantes :

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Dans l&#39;écran d&#39;accueil, cliquez sur le bouton <b>Nouveau graphe</b>.

  </td>
  <td style="border: 0;" valign="top">

  ![Boîte de dialogue Nouveau graphe de Substance - Créer à partir de l&#39;écran d&#39;accueil](creating-a-substance-compositing-graph.resources/newGraphDialog-create-homeScreen.png "Boîte de dialogue Nouveau graphe de Substance - Créer à partir de l&#39;écran d&#39;accueil"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Sur n&#39;importe quel élément de package *existant* dans l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md), cliquez sur <b>RMB</b> et accédez à <b>Nouveau > graphe de Substance</b> dans le menu contextuel.

  </td>
  <td style="border: 0;" valign="top">

  ![Boîte de dialogue Nouveau graphe de Substance - Créer à partir de l&#39;Explorateur](creating-a-substance-compositing-graph.resources/newGraphDialog-create-explorer.png "Boîte de dialogue Nouveau graphe de Substance - Créer à partir de l&#39;Explorateur"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Dans la barre d&#39;outils principale, cliquez sur le bouton ![](creating-a-substance-compositing-graph.resources/image2021-6-22-20-36-44.png) <b>Nouveau graphe de Substance</b>.

  </td>
  <td style="border: 0;" valign="top">

  ![Boîte de dialogue Nouveau graphe de Substance - Créer à partir de la barre d&#39;outils principale](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainToolbar.png "Boîte de dialogue Nouveau graphe de Substance - Créer à partir de la barre d&#39;outils principale"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Dans le menu principal, accédez à <b>Fichier > Nouveau > graphe de Substance...</b>

  </td>
  <td style="border: 0;" valign="top">

  ![](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainMenu.png)

  </td>
  </tr>
  </table>

* Appuyez sur la touche <b>Ctrl+N</b> (Windows) / <b>Cmd+N</b> (macOS).

Quelle que soit la méthode choisie, la boîte de dialogue <b>Nouveau graphe de Substance</b> s&#39;affiche.

<a name="graph-templates"></a>

## Modèles de graphe

Quelle que soit la méthode utilisée pour créer un nouveau graphe de Substance, la boîte de dialogue <b>Nouveau graphe de Substance</b> s&#39;affiche toujours, vous permettant de configurer le nouveau graphe.

![Boîte de dialogue Nouveau graphe de Substance - Matériaux](creating-a-substance-compositing-graph.resources/newGraphDialog-materials.png "Boîte de dialogue Nouveau graphe de Substance - Matériaux"){zoomable="yes"}

### Modèles

Designer inclut des modèles de graphe avec des nœuds préconfigurés pour vous aider à démarrer plus rapidement. Ils peuvent inclure des nœuds de [sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), des nœuds simples pour transmettre des valeurs à ces sorties, par exemple des nœuds de [Couleur uniforme](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md), ainsi que des nœuds d&#39;[entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md).

Double-cliquez sur un modèle dans la liste ou sélectionnez-le et cliquez sur le bouton <b>Créer</b> pour créer un nouveau graphe de Substance à l&#39;aide de ce modèle. Par défaut, le nouveau graphe est placé dans un nouveau package non enregistré.

>[!TIP]
>
> Partir de zéro
> 
> Pour partir d&#39;un graphe entièrement vide, sélectionnez le modèle <b>Vide</b> dans la catégorie « Vide ».

>[!NOTE]
>
> Changement de modèle
> 
> Si vous sélectionnez le mauvais modèle, vous *ne pouvez pas* passer à un autre modèle après avoir créé le graphe.
> 
> Pour transférer votre graphe existant vers un autre modèle, vous pouvez créer un nouveau graphe à l’aide du modèle approprié, puis copier-coller votre graphe vers le nouveau modèle. Reconnectez les nœuds selon les besoins, en particulier les nœuds de sortie.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Chaque modèle est répertorié par son libellé et son sous-titre.

Le sous-titre fournit plus de contexte sur le *cas d&#39;utilisation* du modèle : le modèle de matériau sur lequel il est basé, le logiciel avec lequel il est destiné à s&#39;intégrer, etc.

En mode <b>Vignettes</b>, le sous-titre est placé sous l&#39;étiquette dans un texte plus foncé et plus petit.

Dans les modes d&#39;affichage <b>Liste</b>, <b>Packs</b> et <b>Répertoires</b>, le sous-titre est ajouté à l&#39;étiquette de la manière suivante : *Étiquette - Sous-titre*.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Boîte de dialogue Nouveau graphe de Substance - Vignette](creating-a-substance-compositing-graph.resources/newGraphDialog-thumbnailCard.png "Boîte de dialogue Nouveau graphe de Substance - Vignette")

</td>
</tr>
</table>

<a name="material-samples"></a>

### Exemples de matériaux

La catégorie <b>Exemples de Matériaux</b> comprend une [sélection de graphes](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) dont vous pouvez tirer des enseignements et expérimenter.

Vous pouvez également accéder aux échantillons directement à partir de l&#39;écran d&#39;accueil, en utilisant le bouton <b>Accéder aux échantillons</b>.

Tous les échantillons sont basés sur l&#39;[modèle de matériau](../../interface/3d-view/material-properties/material-properties.md#openpbr).

![Échantillons de Matériau - Bannière d’écran d’accueil](creating-a-substance-compositing-graph.resources/materialSamples-banner.png "Échantillons de Matériau - Bannière d’écran d’accueil"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Info-bulle d’informations

Le survol de l’icône d’informations pour chaque élément de modèle affiche une info-bulle contenant des informations supplémentaires sur le modèle :

<b>Type :</b> type de ressource que le modèle est censé produire. Ce paramètre est modifiable dans les [propriétés de graphe](../../compositing-graphs/graph-parameters/graph-parameters.md).

<b>Description :</b> détails sur le modèle tels que le workflow qu&#39;il intègre, son cas d&#39;utilisation prévu et des recommandations pour son utilisation.

<b>Sorties :</b> les nœuds [Sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) du modèle, le cas échéant.

</td>
<td style="border: 0;" valign="top">

![Boîte de dialogue Nouveau graphe de Substance - Info-bulle du modèle](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipTemplate.png "Boîte de dialogue Nouveau graphe de Substance - Info-bulle du modèle"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Modes d’affichage

La liste des modèles peut être affichée dans différents modes à l&#39;aide du bouton <b>Afficher les modes</b>.

Le filtrage effectué par la catégorie et le fichier de projet sélectionnés est appliqué dans toutes les vues.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Boîte de dialogue Nouveau graphe de Substance - Modes d&#39;affichage](creating-a-substance-compositing-graph.resources/newGraphDialog-viewModes.png "Boîte de dialogue Nouveau graphe de Substance - Modes d&#39;affichage"){zoomable="yes"}

</td>
</tr>
</table>

+++Modes d’affichage
![Boîte de dialogue Nouveau graphe de Substance - Vue Vignettes](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-thumbnails.png "Boîte de dialogue Nouveau graphe de Substance - Vue Vignettes"){zoomable="yes"}



<b>Vignettes</b>

Cartes avec des vignettes fournissant un aperçu ou une icône du type de modèle.

![Boîte de dialogue Nouveau graphe de Substance - Mode Liste](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-list.png "Boîte de dialogue Nouveau graphe de Substance - Mode Liste"){zoomable="yes"}



<b>Liste</b>

Les modèles sont répertoriés par leur étiquette uniquement.

![Boîte de dialogue Nouveau graphe de Substance - Vue Packs](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-packages.png "Boîte de dialogue Nouveau graphe de Substance - Vue Packs"){zoomable="yes"}



<b>Packs</b>

Les modèles sont répertoriés par leur étiquette en tant qu’enfants du fichier de pack auquel ils appartiennent.

Survolez un élément de fichier de package pour afficher une info-bulle avec son chemin complet.

![Boîte de dialogue Nouveau graphe de Substance - Vue Répertoires](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-directories.png "Boîte de dialogue Nouveau graphe de Substance - Vue Répertoires"){zoomable="yes"}



<b>Répertoires</b>

Les modèles sont répertoriés par leur étiquette en tant qu’enfants du répertoire hébergeant le fichier de pack auquel ils appartiennent.

Survolez un élément de répertoire pour afficher une info-bulle avec son chemin complet.

+++

### Propriétés

Après avoir sélectionné le modèle, vous pouvez définir des informations de base concernant le nouveau graphe. Il peut être modifié à tout moment après la création du graphe.

<b>Nom du Graphe</b> : identifiant du graphe. Il doit être unique pour un package donné et ne peut pas inclure d’espaces ni de caractères spéciaux.

<b>Taille</b> : la résolution parent du graphe, qui contrôle la résolution de sortie de la plupart des nœuds, consultez la page [Taille de sortie](../../compositing-graphs/output-size/output-size.md) pour en savoir plus. La largeur et l’height sont liés par défaut. Vous pouvez rompre leur lien en cliquant sur le bouton Lier situé entre les zones de liste déroulante Largeur et height.

<b>Créer un graphe dans</b> : vous pouvez utiliser cette zone de liste déroulante pour créer un *nouveau* package pour le nouveau graphe ou ajouter le nouveau graphe à un *package* existant déjà chargé dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md).

### Info-bulle Aide

Passez le curseur de la souris sur l’icône représentant un point d’interrogation pour afficher une info-bulle avec un bouton pointant directement vers cette page, afin de pouvoir consulter cette documentation si nécessaire.

![Boîte de dialogue Nouveau graphe de Substance - Info-bulle d’aide](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipHelp.png "Boîte de dialogue Nouveau graphe de Substance - Info-bulle d’aide"){zoomable="yes"}

<a name="managing-templates"></a>

## Gestion des modèles

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Filtrage par catégorie

Les catégories permettent de regrouper les modèles qui sont liés les uns aux autres par cas d’utilisation ou type d’actif.

Utilisez la zone de liste déroulante <b>Catégorie</b> pour sélectionner la catégorie par laquelle vous souhaitez filtrer les modèles.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Boîte de dialogue Nouveau graphe de Substance - Filtrage par catégorie](creating-a-substance-compositing-graph.resources/newGraphDialog-categories.png "Boîte de dialogue Nouveau graphe de Substance - Filtrage par catégorie"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Les modèles peuvent avoir une catégorie configurée dans leurs <b>données de modèle</b> [Attribut de graphe](../../compositing-graphs/graph-parameters/graph-parameters.md), utilisé comme filtre pour affiner la liste des modèles :

&lt;category>;&lt;subtitle>

Des catégories personnalisées peuvent être configurées dans les modèles fournis par les fichiers de projet (voir ci-dessous). Ces catégories sont ensuite ajoutées à la liste dans la zone de liste déroulante.

</td>
<td width="50.00%" style="border: 0;" valign="top">

![Boîte de dialogue Nouveau graphe de Substance - Configuration de la catégorie de modèle](creating-a-substance-compositing-graph.resources/newGraphDialog-templateCategorySetup.png "Boîte de dialogue Nouveau graphe de Substance - Configuration de la catégorie de modèle"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Filtrage par fichier de projet

Si l&#39;un des [fichiers de projet](../../interface/preferences-window/project-settings/project-settings.md) fournit un ou plusieurs chemins de modèle, les graphes dans les fichiers de package trouvés dans ces chemins seront ajoutés à la liste des modèles.

Ensuite, utilisez le bouton <b>Filtrer par fichier de projet</b> pour réduire la liste des modèles à ceux fournis par un fichier de projet spécifique.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Boîte de dialogue Nouveau graphe de Substance - Filtrage par fichier de projet](creating-a-substance-compositing-graph.resources/newGraphDialog-projectFiles.png "Boîte de dialogue Nouveau graphe de Substance - Filtrage par fichier de projet"){zoomable="yes"}

</td>
</tr>
</table>
