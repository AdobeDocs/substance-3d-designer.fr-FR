---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/graph-parameters.html"
breadcrumb-title: ''
description: Apprenez à créer et à gérer des paramètres de graphe dans Substance 3D Designer pour contrôler les propriétés et les comportements des matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Graph parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paramètres de graphe
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 1%

---


# Paramètres de graphe

Cette page décrit les paramètres standard du graphique de Substance <b>1&rbrace;.</b>

Un graphique comporte plusieurs paramètres que vous pouvez modifier. Vous pouvez les trouver en cliquant sur *espace vide* dans le graphique ou en sélectionnant l&#39;*élément de graphique* dans le panneau <b>Explorateur</b>. Les paramètres seront ensuite affichés dans la vue Paramètres.

<a name="base-parameters"></a>

## Paramètres de base

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Cette section inclut des paramètres qui ont un impact sur *tous les nœuds qu&#39;elle contient*.

En effet, chaque nœud de ce graphique dont les paramètres de base sont définis sur la méthode d&#39;héritage [Relative au parent](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) obtiendra ses valeurs des paramètres de base *du graphique*.

Les valeurs des paramètres de base du graphique dépendent du contexte dans lequel le graphique est utilisé.

</td>
<td style="border: 0;" valign="top">

![Paramètres de base](../../assets/doc-graph-props-base-params.png "Paramètres de base"){width="512px" zoomable="yes"}

</td>
</tr>
</table>

Par exemple, lorsque le graphique est utilisé dans un autre graphique en tant que nœud d&#39;instance, ses paramètres de base utilisent par défaut la méthode d&#39;héritage « Relative à l&#39;entrée ». Cela signifie qu&#39;ils obtiendront leurs valeurs à partir du nœud connecté à son entrée principale. (Sauf s&#39;ils ont été [remplacés](#input-parameters))

Dans la plupart des cas, l’héritage joue un rôle important dans la définition de ces valeurs et dans leur évolution sur l’ensemble du graphique. Il est donc fortement recommandé d&#39;acquérir une bonne compréhension de l&#39;[héritage dans les graphes de Substance](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) avant d&#39;utiliser ces paramètres.

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Taille de sortie</b> | Ce paramètre vous permet de choisir la *résolution de base* des images du graphique.  Utilisez la commande <div><img data-preserve-html="true" height="22" src="../../assets/props-output-size-lock.jpg"/></div> verrouillez le bouton pour que les valeurs de hauteur et de largeur correspondent et conservez le carré de l&#39;image lors des réglages de taille.<br><br>*Par défaut : (0,0) - Relative au gabarit* [En savoir plus](../../compositing-graphs/output-size/output-size.md) |
| <b>Format de sortie</b> | Permet de choisir le *nombre de bits par pixel de base* dans le graphique, parmi les options suivantes :<ul data-preserve-html="true"><li data-preserve-html="true">8 bits</li><li data-preserve-html="true">16 bits</li><li data-preserve-html="true">HDR Basse précision 16F (16 bits à virgule flottante)</li><li data-preserve-html="true">HDR haute précision 32F (32 bits à virgule flottante)</li></ul>*Par défaut : 8 bits par canal - Relatif au parent* |
| <b>Taille de pixel</b> | Définit la taille en pixels. Nous vous recommandons de conserver les valeurs **Largeur** et **Height** définies sur **1**.*Par défaut : (1,1) - Relative au parent* |
| <b>Mode mosaïque</b> | Définit le *mode de mosaïque* de base dans le graphique à partir de ces options :<ul data-preserve-html="true"> <li data-preserve-html="true">Aucune répétition</li> <li data-preserve-html="true">Répétition horizontale</li> <li data-preserve-html="true">Répétition verticale</li> <li data-preserve-html="true">Limites H+V (c.-à-d. horizontales et verticales)</li> </ul>*Limites H et V par défaut - Relatives au gabarit* |
| <b>Générateur aléatoire</b> | Définit la *valeur de départ aléatoire* de base du graphique.  Utilisez la commande <div><img data-preserve-html="true" height="22" src="../../assets/prop-randomise.jpg"/></div> pour attribuer une nouvelle valeur aléatoire à la valeur de départ aléatoire.<br><br>*Par défaut : 0 - Relative au parent* |

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<a name="attributes"></a>

## Attributs

La section <b>Attributs</b> contient *métadonnées* pour le graphique, qui fournit des informations pour *identifier*, *catégoriser* et *appliquer* le graphique tel que conçu par son auteur.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Attributs de graphique](../../assets/doc-graph-props-attributes.png "Attributs de graphique"){zoomable="yes"}

</td>
</tr>
</table>

+++Liste des attributs

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Identifiant** | Il s&#39;agit du nom du graphique. Il doit être *unique*. Vous ne pouvez pas avoir deux graphiques ou plus avec le même <b>identificateur</b> dans le même package. Il est utilisé comme *nom* du graphique dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md).<br><br>*Remarque :* l&#39;identificateur *ne peut pas être une chaîne vide*. Les chaînes vides sont automatiquement remplacées par `_` ou `Substance_graph`. Vous ne pouvez utiliser *que* les caractères suivants pour cette valeur : *`A-Z, 1-9, @$%[{]}_-`.* Les caractères non autorisés sont automatiquement remplacés par `_`.<br><br>*Par défaut : nouveau\_graphe, ou définis par l’utilisateur lors de la création du graphe* |
| **Libellé** | L&#39;<b>étiquette</b> est utilisée à la place de l&#39;<b>identificateur</b> pour afficher le *nom* du graphique afin d&#39;améliorer la lisibilité dans les scénarios *auxquels l&#39;utilisateur est confronté*, par exemple l&#39;entrée [Bibliothèque](../../interface/the-library/the-library.md) ou l&#39;étiquette [nœud d&#39;instance](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).  Un libellé peut être *non unique* et peut contenir des caractères spéciaux.<br><br>*Conseil :* si vous renommez un graphique, par exemple dans l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md), vous pouvez également modifier son libellé !<br><br>*Par défaut : vide* |
| **Type** | Le <b>type</b> est utilisé pour définir l&#39;objectif prévu d&#39;un [graphique de Substance](../../compositing-graphs/substance-compositing-graphs.md). Il est principalement destiné à la fonctionnalité d&#39;interopérabilité [&#39;Envoyer&#39;](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md). |
| **Modèle de matériau** | La définition du modèle de matériau du graphique garantit que l&#39;ombrage approprié est utilisé dans la vue 3D, si un ombrage *correspondant au modèle* est disponible.<br>Par ex. L&#39;affichage d&#39;un graphique avec le mode Matériau `OpenPBR v1.1` dans la vue 3D sélectionnera le shader `OpenPBR Surface` dans pour le matériau cible.<br><br>Si aucun ombrage correspondant n&#39;est trouvé ou si le modèle du graphique est défini sur `Undefined`, l&#39;ombrage utilisé pour la matière cible dans la vue 3D est *inchangé*. |
| **Taille physique** | Cette valeur spécifie la dimension de la texture dans le *monde physique*, en X (longueur), Y (largeur) et Z (height). Il est donc intrinsèquement lié au matériau qui est produit dans le graphique. La taille physique peut être utilisée, par exemple, pour afficher la texture à son bon rapport dans la <b>vue 2D</b> et la <b>vue 3D</b>.<br><br>*Conseil :* la taille physique d&#39;un graphique de Substance peut être récupérée sous la forme d&#39;une valeur Float3 dans les graphiques de fonction de Substance appliqués à n&#39;importe quel nœud de ce graphique, à l&#39;aide de la [variable intégrée](../../function-graphs/variables/system-variables/system-variables.md) de $physicalsize.<br><br>*Remarque :* La valeur **Z** n&#39;est actuellement *pas prise en compte* dans la **3D Afficher**. La valeur de l&#39;**échelle d&#39;Height** pour le matériau doit donc être définie à l&#39;aide d&#39;un nœud **Output** défini sur l&#39;**échelle de hauteur**, ou directement dans les **propriétés du matériau**.<br><br>*Par défaut : (0,0,0)* |
| **Icône** | Cette zone vous permet de définir une *icône* qui sera utilisée par la <b>bibliothèque</b> pour afficher l&#39;entrée de ce graphique, à la fois en tant que <b>SBS</b> et <b>SBSAR</b>. L&#39;icône est également utilisée dans d&#39;autres situations, telles que la <b>tablette</b> de [Substance 3D Painter](https://www.adobe.com/fr/products/substance3d-painter.html). La zone offre les options suivantes :<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Parcourir</b> : vous permet de parcourir vos fichiers système pour trouver l&#39;<i>image existante</i> qui doit être utilisée comme icône</li> <li data-preserve-html="true"><b>Générer</b> : génère une icône à l&#39;aide d&#39;un <i>paramètre prédéfini</i> intégré du nœud <b>Rendu PBR</b></li> <li data-preserve-html="true"><b>Coller</b> : permet de coller les données d&#39;image actuellement dans le <i>presse-papiers</i> sous forme d&#39;icône</li> <li data-preserve-html="true"><b>Supprimer</b> : cette option <i>supprime</i> l&#39;icône existante et laisse l&#39;emplacement de l&#39;icône <i>vide</i></li> </ul>*Remarque :* l&#39;option **Générer** utilise la **Taille physique** pour déterminer l&#39;**échelle d&#39;Height** du **Rendu PBR** pour son effet de displacement. Si un nœud **Sortie** défini sur l&#39;utilisation **physicalsize** existe dans le graphique, cette sortie est utilisée. Si aucune sortie de ce type n&#39;existe, la valeur des **attributs** du graphique est utilisée *à la place*. Si la valeur de l&#39;attribut est (0,0,0), alors la *valeur prédéfinie* de 0,1 est utilisée.<br><br>*Remarque :* lorsque *aucune icône* est définie, la *première sortie d&#39;image* du graphique est utilisée à la place.<br><br>*Valeur par défaut : Vide* |
| **Package** | Nom de fichier *absolu* pour le **pack** auquel appartient ce graphique.Le bouton **Dossier** peut vous permettre d&#39;ouvrir une nouvelle *fenêtre de l&#39;explorateur de fichiers* système à cet emplacement.*Par défaut : nom de fichier du pack / vide si le pack n&#39;a jamais été enregistré* |
| **Exposé dans SBSAR** | Cela contrôle si le graphique et ses sorties peuvent être *affichés* dans le fichier **SBSAR** publié à partir du **package** du graphique. Ceci est utile si certains graphiques du package sont utilisés uniquement en tant que *sous-graphes* pour le graphique principal du package et que *ne doivent pas apparaître* dans le **SBSAR**.*Par défaut : Oui* |
| **Afficher dans la bibliothèque** | Détermine si le graphique doit être *visible* dans la **bibliothèque** si le package est stocké dans un emplacement *surveillé* par la **bibliothèque**.*Par défaut : à définir dans l&#39;onglet Bibliothèque des paramètres du projet* |
| **Description** | Il s&#39;agit du *texte de description* du graphique.Il est visible dans l&#39;*info-bulle* pour l&#39;entrée de graphique dans la **bibliothèque**, n&#39;importe quel nœud de **instance** pour ce graphique et le logiciel avec une **intégration de Substances** existante.*Par défaut : vide* |
| **Catégorie** | Vous pouvez utiliser ce champ pour définir une *catégorie* pour cet élément de graphique dans la **bibliothèque**.*Par défaut : vide* |
| **Auteur** | Vous pouvez utiliser ce champ pour placer le *nom* de l&#39;auteur.*Par défaut : vide* |
| **URL d&#39;auteur** | Ce champ vous permet de saisir une *URL*, par exemple le site Web de l&#39;auteur.*Par défaut : vide* |
| **Balises** | Vous pouvez utiliser ce champ pour ajouter vos propres *balises* afin d&#39;améliorer la *recherchabilité* et la *détectabilité* du graphique.*Par défaut : vide* |
| **Groupe** | Active le regroupement des éléments dans le menu Nœud. Les ressources telles que les graphiques ou les bitmaps partageant une valeur « Groupe » commune sont regroupées dans une section portant le nom du groupe. *Par défaut : vide* |
| **Données utilisateur** | Vous pouvez utiliser ce champ pour ajouter vos propres données supplémentaires. Ceci est utile pour les intégrations personnalisées dans les logiciels tiers. Substance 3D Painter et Sampler utilisent ces données utilisateur pour définir certains comportements spécifiques.*Par défaut : vide* |
| **Données de modèle** | Lorsqu&#39;un graphique de Substance est utilisé comme modèle, cet attribut définit la catégorie et le sous-titre du [modèle](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md). Ils sont ainsi séparés : &lt;category>;&lt;subtitle> <br><br>*Default : Empty* |

+++
<a name="input-parameters"></a>

## Paramètres d’entrée

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Tous les paramètres spécifiques au graphique, y compris les [paramètres exposés](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), sont [gérés](../../compositing-graphs/manage-parameters/manage-parameters.md), modifiés et prévisualisés ici.

[Les paramètres prédéfinis](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md) peuvent également être créés pour tout ou partie des paramètres.

</td>
<td style="border: 0;" valign="top">

![Paramètres d&#39;entrée](../../assets/doc-graph-props-input-parameters.png "Paramètres d&#39;entrée"){zoomable="yes"}

</td>
</tr>
</table>

+++Remplacement des paramètres de base
Lorsque vous utilisez un graphique dans un autre graphique en tant que [nœud d&#39;instance](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), vous pouvez contrôler la valeur par défaut de n&#39;importe quel paramètre de base sur ce nouveau nœud d&#39;instance.

Ouvrez le menu hamburger en haut de la section Paramètres d’entrée et accédez au sous-menu Remplacer les paramètres de base pour sélectionner un paramètre de base pour lequel vous souhaitez définir une valeur par défaut arbitraire.

L’éditeur du paramètre sélectionné apparaîtra en haut de la liste des paramètres d’entrée du graphique. Vous pouvez ensuite ajuster leur valeur et leur [méthode d&#39;héritage](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) selon vos besoins.

+++

>[!IMPORTANT]
>
> Les onglets <b>Aperçu</b> et <b>Paramètres prédéfinis</b> sont désactivés lors de l&#39;[édition contextuelle](../../interface/preferences-window/preferences-window.md).

<a name="inputs"></a>

## Entrées

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Dans cette partie, tous les nœuds [Entrée](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) du graphique sont répertoriés.

Vous pouvez les réorganiser en les faisant glisser sur la poignée située à l’extrême gauche de chaque élément.

</td>
<td style="border: 0;" valign="top">

![Entrées](../../assets/doc-graph-props-inputs.png "Entrées"){zoomable="yes"}

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Dans cette partie, tous les nœuds de [sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) du graphique.

Vous pouvez les réorganiser en les faisant glisser sur la poignée située à l’extrême gauche de chaque élément.

</td>
<td style="border: 0;" valign="top">

![Sorties](../../assets/doc-graph-props-outputs.png "Sorties"){zoomable="yes"}

</td>
</tr>
</table>
