---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: Accédez à la référence complète de l’API de script Substance 3D Designer Python pour le développement de plug-ins.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Référence des API de script
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# Référence des API de script

Cette page décrit les principaux concepts de l’API.

Pour plus d&#39;informations, consultez la documentation livrée avec l&#39;application qui est accessible dans <b>Aide > Documentation de l&#39;API Python...</b>. Dans cette documentation, effectuez une <b>recherche rapide</b> des noms de module (entre parenthèses ci-dessous) pour trouver facilement leur définition.

## Contexte

L&#39;objet contexte (*Context*) est le <b>point d&#39;entrée principal de l&#39;API</b>. Il est créé la première fois que l&#39;utilisateur l&#39;obtient à l&#39;aide de la méthode &#39;<b>*getContext()*</b>&#39; du module &#39;*sd*&#39;.

Cet objet permet essentiellement de <b>récupérer l&#39;objet application</b> (*SDApplication*).

## Application (SDApplication)

L&#39;application (*SDApplication*) est l&#39;objet qui permet <b>l&#39;accès aux principaux gestionnaires d&#39;API</b>, tels que :

* le <b>gestionnaire de package </b>Manager (*SDPackageMgr*) qui gère tous les <b>packages</b> de l&#39;application ;
* <b>Module </b>Manager (*SDModuleMgr*) qui gère tous les <b>modules</b> de l&#39;application ;
* le <b>gestionnaire </b>d&#39;interface utilisateur (*SDUIMgr*) qui peut créer des <b>menus et des ancrages</b> dans la fenêtre de l&#39;application.

Vous pouvez enregistrer <b>rappels</b> auprès de l&#39;application qui sera appelée lorsque certains événements se produiront.

## Gestionnaire de modules (SDPackageMgr)

Cet objet gère tous les <b>packs</b> de l&#39;application. Les packages sont affichés dans le composant « <b>*Explorateur*</b> ».

Il permet de :

* <b>créer</b> un nouveau pack ;
* <b>charger/décharger</b> un package ;
* <b>enregistrer</b> un pack ;
* <b>rechercher</b> un pack.

## Package (SDPackage)

Un package (*SDPackage*) est une <b>collection de ressources</b> (*SDResource*).

Le contenu d&#39;un package peut être <b>stocké</b> dans un fichier avec l&#39;extension <b>.sbs</b> via l&#39;objet &#39;*SDPackageMgr*&#39;. Cet objet vous permet de <b>récupérer </b>des ressources spécifiques.

Pour <b>créer</b> une ressource spécifique, consultez les méthodes statiques d&#39;objet associées (par exemple : &#39;*SDSBSCompGraph.sNew()*&#39;).

Un package contient également un dictionnaire de métadonnées (SDMetadataDict). Vous trouverez plus d&#39;informations sur les métadonnées [ici](../../package-metadata/package-metadata.md).

## Ressource (SDResource)

Une ressource (*SDResource*) est un objet qui peut être <b>référencé</b> par une autre ressource.

Il existe plusieurs <b>types</b> de ressources :

* Dossiers (*SDResourceFolder*);
* Graphes (*SDGraph*);
* Bitmaps (*SDResourceBitmap*);
* Images de SVG (*SDResourceSVG*);
* Polices (*SDResourceFont*);
* Scènes (*SDResourceScene*);
* Mesures BSDF (*SDResourceBSDFMeasurement*);
* Profils lumineux (*SDResourceLightProfile*).

Une ressource peut être <b>créée</b> à partir de la méthode statique &#39;*sNew()*&#39; sous :

* un colis ;
* un dossier.

Une ressource peut avoir plusieurs <b>propriétés</b> (*SDProperty*).

## Gestionnaire d’interface utilisateur (SDUIMgr)

Le gestionnaire d&#39;interface utilisateur permet de <b>créer des éléments d&#39;interface utilisateur</b> dans la fenêtre principale de la Substance Designer, tels que des <b>menus</b>, des <b>docks</b> et d&#39;enregistrer des <b>rappels</b> à appeler lorsque des événements liés à l&#39;interface utilisateur se produisent.

En outre, le gestionnaire d&#39;interface utilisateur a accès au <b>graphe actif</b> et à la <b>sélection</b> du graphe actif.

## Graphes (graphique ODD)

Un graphe (*SDGraph*) est un objet qui contient :

* <b>nodes </b>(*SDNode*);
* <b>Objets graphe</b> (*SDGraphObjects*);
* <b>propriétés </b>(*SDProperty*).

Il existe 4 types de graphes différents :

* graphe de Substance (*SDSBSCompGraph*)
* graphe de fonction de Substance (*SDSBSFunctionGraph*)
* graphe FXMap de Substance (*SDSBSFxMapGraph*)

Un graphe peut avoir un ou plusieurs nœuds de <b>sortie</b>. Les nœuds de sortie représentent les <b>résultats</b> du graphe.

Tous les nœuds disponibles pour un graphe peuvent être <b>récupérés</b> avec la méthode &#39;*getNodeDefinitions()*&#39;.

Un nouveau nœud peut être <b>créé</b> avec la méthode &#39;*newNode()*&#39;.

Un nouveau nœud <b>instance</b> peut être créé à partir d&#39;une ressource (*SDResource*) avec la méthode &#39;*newInstanceNode()*&#39;.

## Nœud (SDNode)

Un nœud (*SDNode*) représente une <b>opération</b> effectuée sur un objet.

Il peut être créé à partir de :

* a <b>définition</b> (*SDDefinition*) (voir &#39;*SDGraph.newNode()&#39;*);
* a <b>ressource</b> (*SDResource*) (voir &#39;*SDGraph.newInstanceNode()&#39;*).

Un nœud peut avoir plusieurs <b>propriétés</b>.

Il existe plusieurs <b>types</b> de nœud :

* *<b>SDSBSCompNode</b>* : nœud du Graphe Substance (*SDSBSCompGraph*);
* *<b>SDSBSFunctionNode</b>* : nœud du Graphe de fonction Substance (*SDSBSFunctionGraph*);
* *<b>SDSBSFxMapNode</b>* : nœud du Graphe FXMap de la Substance de données (*SDSBSFxMapGraph*);

## Objets Graphe (SDGraphObjects)

Un objet de graphe (*SDGraphObject*) est un objet qui <b>ajoute des informations supplémentaires</b> au graphe, mais qui <b>*n&#39;est pas* pris en compte</b> pendant le processus d&#39;évaluation du graphe.

Il existe <b>3 types</b> d&#39;objets graphe :

* <b>Épingle</b> (*SDGraphObjectPin*)
* <b>Commentaire</b> (*SDGraphObjectComment*)
* <b>Cadre</b> (*SDGraphObjectFrame*)

Pour plus d&#39;informations sur la <b>création</b> de ces objets, consultez la méthode statique &#39;*sNew()*&#39;.

## Propriétés (SDProperty)

Une propriété (*SDProperty*) est un objet qui <b>décrit</b> une propriété de <b>un autre objet</b> (un graphe, un nœud, une ressource, etc.).

Il appartient à une <b>catégorie</b> spécifique (*SDPropertyCategory*) :

* <b>Entrée</b> : classe les propriétés d&#39;entrée d&#39;un objet, qui ont généralement<b> un impact sur l&#39;opération</b> effectuée par l&#39;objet actuel ;
  * Exemple : la propriété &#39;*color*&#39; d&#39;un nœud de Couleur uniforme dans un graphe de Substance est une propriété d&#39;entrée ;
* <b>Sortie</b> : classe les propriétés de sortie d&#39;un objet. Il est utilisé pour identifier un <b>résultat</b> d&#39;un objet ;
* <b>Annotation</b> : classe les propriétés qui <b>*n&#39;ont pas* d&#39;impact sur l&#39;opération</b> effectuée par un objet ;
  * Ex. : le &#39;*label*&#39; d&#39;un graphe est une propriété d&#39;annotation, car il n&#39;a aucune incidence sur le calcul du graphe.

Il contient les <b>membres</b> suivants :

* <b>Id</b> : identifiant de la propriété dans le cadre de cette catégorie ;
* <b>Types</b> : types pris en charge par la propriété actuelle. Certaines propriétés peuvent prendre en charge *plusieurs* types : &#39;*int*&#39;, &#39;*float*&#39;, etc.;
  * Ex. : les propriétés d&#39;entrée d&#39;un nœud &#39;*sbs::function::add*&#39; peuvent prendre en charge différents types : &#39;*int&#39;*, &#39;*int2&#39;*, &#39;*int3&#39;*, &#39;*int4&#39;*, &#39;*float&#39;*, &#39;*float2&#39;*, &#39;*float3&#39;*, &#39;*float4&#39;, etc.;*
* <b>Catégorie</b> : catégorie à laquelle la propriété appartient (entrée, sortie, annotation);
* <b>Libellé</b> : libellé de la propriété, utilisé pour l&#39;affichage *uniquement*;
* <b>Description</b> : description de la propriété ;
* <b>DefaultValue</b> : valeur par défaut ;
* <b>IsConnectable</b> : indique si une connexion (*SDConnection*) *peut* être effectuée sur cette propriété ;
* <b>isReadyOnly</b> : indique si la propriété est en lecture seule. Si la valeur est true, la valeur qui lui est associée *ne pourra pas* être modifiée ;
* <b>isVariadic</b> : si la valeur est true, cette propriété sera représentée comme *propriétés multiples* sur l&#39;objet ;
* <b>isPrimary</b> : indique si la propriété spécifiée est la propriété *principale* qui contrôle d&#39;autres propriétés. *Remarque :* ceci est spécifique aux *nœuds de composition* de Substance (*SDSBSCompNode*).

Exemples :

* Propriétés du nœud &#39;*sbs::compositing::input*&#39; :

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::input</th></tr><tr><td style="text-align: left;"><strong>Entrée</strong></td><td style="text-align: left;"><strong>Annotation</strong></td><td style="text-align: left;"><strong>Sortie</strong></td></tr><tr><td>$outputsize</td><td>étiquette</td><td><p>unique_filter_output (CONNECTABLE)</p></td></tr><tr><td>$format</td><td>description</td><td><br/></td></tr><tr><td>$pixelsize</td><td>identifiant</td><td><br/></td></tr><tr><td>$pixelratio</td><td>userdata</td><td><br/></td></tr><tr><td>$répétition</td><td>groupe</td><td><br/></td></tr><tr><td>$randomseed</td><td>visible si</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>usages</td><td><br/></td></tr></tbody></table>

* Propriétés du nœud &#39;*sbs::compositing::blend*&#39; :

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::blend</th></tr><tr><td style="text-align: left;"><strong>Entrée</strong></td><td style="text-align: left;"><strong>Annotation</strong></td><td style="text-align: left;"><strong>Sortie</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output (CONNECTABLE)</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$répétition</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.connecteur (CONNECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.connecteur (CONNECTABLE)</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connecteur (CONNECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td>opacitymult</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">mode de fusion</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">mélange de couleurs</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">maskrectangle</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## Type (SDType)

Un type (*SDType*) contient des informations d&#39;une valeur <b>type</b>, telles que :

* <b>Id</b> : identifiant du type ;
* <b>Modificateur</b> : le modificateur de type qui peut être l&#39;une des valeurs &#39;*SDTypeModificateur&#39;* <b>enum</b> :
  * *Auto*;
  * *Uniforme* : la valeur est évaluée *une* fois par opération ;
  * *Variation* : la valeur est évaluée *plusieurs fois* par opération (par exemple : pour chaque texel).

Plusieurs types sont définis, tels que :

* <b>enums</b> (*SDTypeEnum*) : décrit un type <b>enumeration</b> avec toutes ses propriétés ;
* <b>structures</b> (*SDTypeStruct*) : décrit un type <b>structure</b> avec toutes ses propriétés ;
* <b>array</b> (*SDTypeArray*) : décrit un <b>array</b>.
* etc.

Voir la *documentation de l&#39;API Python* de la Substance Designer pour la liste exhaustive.

## Valeurs (SDValue)

Une valeur (*SDValue*) est un objet qui <b>encapsule</b> une valeur de *type de base*.

Par exemple :

* un objet &#39;<b>*SDValueInt*</b>&#39; encapsule une valeur &#39;*int*&#39;;
* un objet &#39;<b>*SDValueFloat4*</b>&#39; encapsule une valeur &#39;*float4*&#39;;
* etc.

La valeur de type de base peut généralement être <b>récupérée</b> avec la méthode &#39;<b>get()</b>&#39;, mais cela peut dépendre du *type* de &#39;*SDValue&#39;* qui a été retourné.

## Connexion (SDConnection)

Une connexion (*SDConnection*) représente un <b>lien</b> entre deux<b> propriétés</b> différentes de deux <b>nœuds</b> différents.

Il contient :

* Le <b>nœud cible</b>;
* <b>propriété cible</b> du nœud cible ;

Toutes les <b>opérations de connexion</b> sont effectuées sur un nœud :

* <b>création</b> d&#39;une nouvelle connexion, voir &#39;*SDNode.newPropertyConnection()*&#39;
* <b>suppression</b> d&#39;une connexion existante, voir &#39;*SDNode.deletePropertyConnection()*&#39;
* <b>récupération</b> des connexions d&#39;une propriété, voir &#39;*SDNode.getPropertyConnections()*&#39;

## Module (SDModule)

Un module est une <b>collection de définitions et de types</b>.

Il permet de récupérer facilement toutes les informations sur les nœuds qui peuvent être créés, ainsi que sur les énumérations et les structures.

Il contient :

* un <b>identifiant</b> (*Id*) unique dans le contexte du gestionnaire de modules (*SDModuleMgr*);
* une liste de <b>définitions</b> (*SDDefinition*);
* une liste de <b>types</b> (*SDType*).

## Définition (SddDefinition)

Un objet de définition (*SDDefinition*) contient des informations sur la définition d&#39;un <b>objet</b> particulier basé sur <b>propriétés</b> (« *SDNode »*, etc.).

Il contient :

* <b>Id</b> : identifiant de la définition ;
* <b>Libellé</b> : libellé de la définition ;
* <b>Description</b> : description de la définition ;
* <b>Propriétés</b> : propriétés de toutes les propriétés disponibles *catégories* (*SDPropertyCategory*).
