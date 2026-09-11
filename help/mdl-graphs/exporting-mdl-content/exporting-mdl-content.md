---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exporting-mdl-content.html"
breadcrumb-title: ''
description: Découvrez comment exporter du contenu MDL à partir de Substance 3D Designer pour l’utiliser dans des applications et des moteurs de rendu externes.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exporting MDL content
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportation de contenu MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---


# Exportation de contenu MDL

Cette page décrit les processus d&#39;exportation associés aux [Graphes MDL](../../mdl-graphs/mdl-graphs.md) et aux matériaux dans Substance 3D Designer.

## Vue d’ensemble

Une fois qu&#39;un Matériau MDL est créé dans Designer, il doit être exporté dans un format qui peut *contenir la définition du matériau* et être lu par les moteurs de rendu qui prennent en charge MDL. MDL utilise des formats propriétaires pour transporter les définitions de matériau, appelées Modules MDL, écrites et conditionnées dans différents formats qui peuvent tous être exportés à partir de Designer.

>[!NOTE]
>
> Tous ces formats peuvent être ouverts directement avec un *éditeur de texte*, parfois après avoir été déballés avec un gestionnaire d&#39;archives, pour inspecter la définition de matériau qu&#39;ils contiennent.

## Module MDL (\*.mdl)

Il s’agit du format de fichier d’exchange fondamental pour les définitions de matériau. Un Module MDL définit les éléments suivants :

* caractéristiques et comportement du matériau
* ses paramètres exposés et valeurs par défaut
* ses annotations (c’est-à-dire les métadonnées) : auteur, balises, catégories, ...

L&#39;exportation d&#39;un Module MDL est effectuée au niveau du *pack*. Pour exporter un Module MDL pour un package donné, cliquez sur le bouton ![](../../assets/mdl-export-module-icon.png) <b>Exporter le Module MDL</b> dans l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md) ou sélectionnez la même option dans le menu contextuel *du* package. Sélectionnez un emplacement et un nom cible pour le Module MDL exporté, et la boîte de dialogue <b>Rapport d&#39;exportation</b> s&#39;affiche avec la liste des messages consignés pendant le processus d&#39;exportation.

Le module exporté contiendra les définitions de *tous* les Matériaux MDL définis par un [Graphe MDL](../../mdl-graphs/mdl-graphs.md) dans le package.

>[!NOTE]
>
> En savoir plus sur les Modules MDL dans les sections 4 et 15 de la [spécification MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) de NVIDIA.

>[!NOTE]
>
> Les avertissements suivant ce modèle : `x appears to be invalid whereas it was expected to be an mdl::call` sont provoqués par la façon dont les Matériaux MDL sont traités dans les Graphes MDL et peuvent *être ignorés* en toute sécurité.

![Chemin d’exportation MDL](../../assets/mdl-export-module.png "Chemin d’exportation MDL")

*Les chemins d&#39;accès « Module MDL d&#39;exportation » dans l&#39;Explorateur et la boîte de dialogue Rapport d&#39;exportation qui en résulte*

### Paramètre prédéfini MDL (\*.mdl)

Un paramètre prédéfini de Module MDL est en grande partie identique au module sur lequel il est basé, à la seule différence qu&#39;il porte un ensemble différent de valeurs par défaut. Pour en savoir plus, [cliquez ici](https://www.migenius.com/doc/realityserver/latest/resources/general/iray/api_reference/iray/html/classmi_1_1neuraylib_1_1IMdl__factory.html#details).

Un paramètre prédéfini pour un Matériau MDL attribué à un matériau de scène `my_material` peut être exporté à partir des emplacements suivants :

* Le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md), en cliquant sur <b>RMB</b> sur la ressource Graphe MDL et en sélectionnant l&#39;option <b>Exporter le paramètre prédéfini...</b> dans le menu contextuel
* Panneau [vue 3D](../../interface/3d-view/3d-view.md), à l’aide de l’option de menu <b>Matériaux > mon\_matériau > Exporter le paramètre prédéfini...</b>

L&#39;option de menu ouvre la boîte de dialogue <b>Exporter le paramètre prédéfini de Matériau MDL</b>, qui propose les options suivantes :

* <b>Répertoire</b> : emplacement cible vers lequel le Module MDL est exporté
* <b>Nom du fichier MDL</b> : nom du Module MDL
* <b>Incorporer les Modules MDL importés</b> : si le Module MDL repose sur des modules importés, c&#39;est-à-dire s&#39;il comporte des dépendances de module, la sélection de cette option entraîne l&#39;*incorporation* des dépendances de  dans le Module MDL exporté, ce qui le rend effectivement *autonome* au détriment de la taille du fichier et de l&#39;héritage dynamique

Le paramètre prédéfini exporté utilisera les *valeurs actuelles* des paramètres du matériau dans la vue 3D comme *nouvelles valeurs par défaut*. Ces valeurs peuvent être modifiées à l&#39;aide de l&#39;option <b>Matériaux > mon\_matériau > Modifier</b>, qui affichera les paramètres exposés du matériau dans le panneau Propriétés.

>[!WARNING]
>
> Lors de l&#39;exportation d&#39;un Module MDL à partir du panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md), un Module MDL contenant *tous* Matériaux MDL définis par un Graphe MDL dans le package, l&#39;exportation d&#39;un paramètre prédéfini MDL à partir de la [vue 3D](../../interface/3d-view/3d-view.md) entraîne un Module MDL contenant *uniquement* la définition des Matériaux MDL appliqués au *matériau sélectionné* dans le menu - `my_material` dans cet exemple.

![Chemin d’exportation du paramètre prédéfini MDL](../../assets/mdl-export-preset.png "Chemin d’exportation du paramètre prédéfini MDL")

*Chemin d&#39;accès « Exporter le paramètre prédéfini » dans vue 3D et boîte de dialogue Exporter le paramètre prédéfini de Matériau MDL qui en résulte*

## archive de module MDL (\*.mdr)

Une archive de Module MDL associe des Modules MDL (voir ci-dessus) avec des ressources telles que *textures* et des fichiers Lisez-moi dans un *fichier unique transportable*.

L&#39;exportation d&#39;une archive de Module MDL est effectuée au niveau du *pack*. Pour exporter une archive de Module MDL pour un package donné, cliquez sur le bouton ![](../../assets/mdl-export-module-icon.png) <b>Exporter l&#39;archive de Module MDL</b> dans l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md) ou sélectionnez la même option dans le menu contextuel *du* package. Sélectionnez un emplacement cible et un nom pour l&#39;archive de Module MDL exportée, et la boîte de dialogue <b>Rapport d&#39;exportation</b> s&#39;affiche avec la liste des messages consignés pendant le processus d&#39;exportation.

L&#39;archive de module exportée contiendra le Module MDL contenant les définitions de *tous* les Matériaux MDL définis par un [Graphe MDL](../../mdl-graphs/mdl-graphs.md) dans le package. Si un [graphe de Substances](../../compositing-graphs/substance-compositing-graphs.md) est [instancié dans un Graphe MDL](../../mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md) et connecté à un flux allant au nœud [Racine](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md), les textures qu&#39;il génère sont *enregistrées dans l&#39;archive*.

En plus de ces éléments, l&#39;archive comprend un fichier <b>MANIFEST</b> qui décrit les métadonnées suivantes pour l&#39;archive de Module MDL :

* `mdl` : version de MDL utilisée pour exporter l&#39;archive de module, par exemple, « 1.5 »
* `version` : la version de l&#39;archive de module, par exemple, « 1.0.0 »
* `module` : nom de l&#39;archive de module, par exemple,  »::pbr\_metallic\_roughness\_basic »
* `exports.material` : nom des matériaux définis dans l&#39;archive de module, par exemple,  »::pbr\_metallic\_roughness\_basic::MDL\_graphe »

>[!NOTE]
>
> En savoir plus sur le format de fichier d&#39;archive MDL dans l&#39;annexe C de la [spécification MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) de NVIDIA.

![Chemin d’exportation MDR](../../assets/mdl-export-archive.png "Chemin d’exportation MDR")

*Les chemins d&#39;accès « Exporter l&#39;archive du Module MDL » dans l&#39;Explorateur et la boîte de dialogue Rapport d&#39;exportation qui en résulte*

## Module encapsulé MDL (\*.mdle)

Les graphes MDL comportant des paramètres exposés peuvent être exportés sous forme de Matériaux MDL encapsulés. L&#39;encapsulation *enveloppe les données* dans une classe dédiée de sorte que les données *ne soient pas accessibles directement*.

Par exemple, alors que vous pouvez toujours modifier les valeurs des paramètres exposés pour contrôler le comportement d&#39;un matériau, la *définition* de ces paramètres n&#39;est *pas disponible* dans un Module MDL encapsulé.

L&#39;exportation d&#39;un Module MDL encapsulé s&#39;effectue dans l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md) au niveau du Graphe MDL, en sélectionnant l&#39;option <b>Exporter en tant que .mdle</b> dans le menu contextuel d&#39;un Graphe MDL. Sélectionnez un emplacement cible et un nom pour le module encapsulé MDL exporté, et la boîte de dialogue <b>Rapport d&#39;exportation</b> s&#39;affiche avec la liste des messages consignés pendant le processus d&#39;exportation.

*Seule* la définition de matériau pour le *Graphe MDL sélectionné* sera incluse dans le Module MDL encapsulé exporté.

>[!NOTE]
>
> En savoir plus sur les définitions de matériau encapsulé dans la section 13.5 de la [spécification MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) de NVIDIA et de l&#39;[API du SDK MDL](https://raytracing-docs.nvidia.com/mdl/api/mi_neuray_example_mdle.html).

![Chemin d’exportation MDLE](../../assets/mdl-export-encapsulated.png "Chemin d’exportation MDLE")

*Chemin d&#39;accès « Exporter en tant que milieu » dans l&#39;Explorateur et boîte de dialogue de rapport d&#39;exportation résultante*
