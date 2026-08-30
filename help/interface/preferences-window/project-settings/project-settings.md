---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/preferences-window/project-settings.html"
breadcrumb-title: ''
description: Configurez les paramètres du projet dans les préférences de Substance 3D Designer pour personnaliser le comportement par défaut du projet.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Project settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paramètres du projet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '2687'
ht-degree: 1%

---


# Paramètres du projet

Cette page présente les <b>paramètres des projets</b> dans [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html), ainsi que les paramètres qu&#39;ils contiennent.

Substance 3D Designer vous permet de créer des préférences *par projet* et de les partager sur plusieurs postes de travail. Ces préférences se trouvent dans l&#39;onglet <b>Projets</b> de la fenêtre [Préférences](../../../interface/preferences-window/preferences-window.md).

Cela est très utile si vous souhaitez configurer un environnement de travail commun pour une équipe travaillant sur le même projet, en utilisant le fichier de projet *same* sur les systèmes *all*.

>[!NOTE]
>
> Pour plus d&#39;informations sur la configuration et l&#39;intégration de Substance 3D Designer dans un **pipeline de production**, nous *vous recommandons vivement* de vous référer à la section [Configuration du pipeline et du projet](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) de la documentation.

![Paramètres du projet](project-settings.resources/2019-3-0-prefs-proj-01.png "Paramètres du projet"){zoomable="yes"}

## Configuration

### Fichier de configuration

Cela vous permet de définir le chemin d&#39;accès du <b>fichier de configuration</b> pour Substance 3D Designer. Un fichier de configuration utilise l&#39;extension <b>\*.sbscfg</b> et contient une liste de fichiers de projet ainsi qu&#39;un paramètre d&#39;affichage de compatibilité défini.

*Par défaut : default\_configuration.sbscfg*

>[!NOTE]
>
> Vous pouvez utiliser l&#39;option de ligne de commande **—config-file** pour lancer Designer avec un fichier de configuration spécifique.\
> Pour plus d&#39;informations sur les fichiers de configuration, vous pouvez vous référer à la page [Liste de configuration - SBSCFG](../../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) de la documentation.

### Fichiers de projet

Un fichier de projet contient un certain nombre de paramètres qui définissent des aspects essentiels de l’environnement de travail dans Designer, organisés en onglets. Ces paramètres sont répertoriés dans le chapitre Projet de cette page. Les fichiers de projet utilisent l&#39;extension <b>\*.sbsprj</b>.

Vous pouvez importer plusieurs fichiers de projet à utiliser pour votre environnement de travail dans Designer. Lorsque plusieurs fichiers de projet existent, les paramètres qui sont des listes (par exemple, les chemins de contrôle de bibliothèque, les alias, etc.) sont *combinés* et les paramètres qui sont des valeurs uniques sont définis par le *dernier fichier de projet de la liste*.

*Par défaut : default\_project.sbsprj (lecture seule), user\_project.sbsprj*

>[!NOTE]
>
> Pour plus d&#39;informations sur l&#39;utilisation de fichiers de projet dans un pipeline de production, vous pouvez vous référer à la page [Fichiers de configuration de projet - SBSPRJ](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) de la documentation.

### Affichage de compatibilité

Certains des nœuds créés avec une version récente de Designer ne sont pas compatibles avec les anciennes versions de la Substance Engine.

Le <b>mode de compatibilité</b> mettra en surbrillance les nœuds *non* compatibles avec la Substance Engine sélectionnée, avec un contour jaune.

*Par défaut : Substance Engine v7*

### Vue 3D

|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Moteur de rendu par défaut</b> | Ce paramètre vous permet de sélectionner le [rendu 3D](../../../interface/3d-view/3d-renderers/3d-renderers.md) qui doit être utilisé par défaut lors du démarrage d&#39;une *nouvelle* [vue 3D](../../../interface/3d-view/3d-view.md).<br><br>*Par défaut : par défaut (rendu prédéfini)* |
| <b>shader par défaut</b> | Ce paramètre vous permet de sélectionner le shader qui doit être utilisé par défaut lors du démarrage d&#39;une *nouvelle* [vue 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Configuration par défaut : open_pbr.glslfx* |
| <b>map d&#39;environnement par défaut</b> | Ce paramètre vous permet de sélectionner la texture qui doit être appliquée par défaut à l&#39;environnement lors du démarrage d&#39;une *nouvelle* [vue 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Par défaut : panorama\_map.hdr* |
| <b>Fichier d&#39;état par défaut</b> | Le fichier [vue 3D](../../../interface/3d-view/3d-view.md) **État de la Scène** inclut un certain nombre de paramètres pour la vue 3D, tels que la position de la caméra, l&#39;exposition de l&#39;environnement et le maillage. Il est utilisé pour stocker l&#39;état de la vue 3D afin que vous puissiez charger rapidement une scène adaptée à vos besoins. Les fichiers d&#39;état de scène utilisent l&#39;extension **\*.sbsscn**.Ce paramètre vous permet de sélectionner le fichier d&#39;état de Scène de données vue 3D qui doit être utilisé lors du démarrage d&#39;une nouvelle vue 3D.  **Alerte :** certaines mises à jour logicielles peuvent modifier la façon dont les états de scène sont enregistrés/chargés. Si la scène de données n&#39;est *pas restaurée correctement*, il est recommandé de définir manuellement l&#39;état souhaité de la scène de données et de *réexporter* le fichier d&#39;état de Scène de données que vous utilisez par défaut. <br><br>*Par défaut : vide (dans ce cas, un état de scène prédéfini est utilisé)* |
| <b>État d&#39;éclairage par défaut</b> | Ce paramètre vous permet de sélectionner les lumières disponibles prédéfinies qui doivent être activées lors du démarrage d&#39;une nouvelle [vue 3D](../../../interface/3d-view/3d-view.md), *si aucun fichier n&#39;est défini* dans le champ **Fichier d&#39;état par défaut**<br><br>*Par défaut : Lumière ambiante uniquement* |

### Alias

Les alias sont utilisés pour *raccourcir* les chemins système et permettre aux équipes de *partager* les ressources plus efficacement. Les alias sont utilisés *dans l&#39;ensemble du logiciel* ainsi que dans les *fichiers SBS*.

Ces paramètres vous permettent de *ajouter* et de *modifier* des alias. Lorsqu&#39;un alias est appliqué, il *remplace* le chemin mappé en utilisant la syntaxe suivante : <b>://</b>.

Exemple : si une ressource *myResource* dans le dossier *myFolder* est placée à l&#39;emplacement *C :/Users/user/Documents*, le mappage de cet emplacement à *myalias* entraînera l&#39;utilisation du chemin d&#39;accès *myalias://myFolder/myResource* dans l&#39;application *et* dans le package SBS auquel appartient la ressource.

*Par défaut : sbs ; sd-3dview-shapes ; sd-3dview-maps ; sd-3dview-shaders (projet par défaut)*

>[!WARNING]
>
> Les alias sont *globaux pour l&#39;application*. Cela signifie qu&#39;ils seront appliqués à *tous les chemins* utilisés dans l&#39;application, ainsi qu&#39;à tous les chemins dans les *fichiers de paramètres de projet SBSPRJ chargés*. Gardez cela à l’esprit lors de la configuration de votre environnement de projet !\
> En outre, nous vous recommandons de *ne pas imbriquer* les alias, c&#39;est-à-dire de créneler un chemin qui est également inclus dans un autre alias.

### Bakers

|                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Nom de ressource par défaut</b> | Ce paramètre vous permet de définir un **modèle de dénomination** par défaut qui sera utilisé pour les fichiers image de sortie. Les alias disponibles dans la [fenêtre de cuisson](../../../bakers/bakers.md) peuvent également être utilisés ici (c’est-à-dire *$(mesh)*, *$(bakername)*, *$(udim)*, *$(custom)*)<br><br>*Par défaut : $(mesh)\_$(bakername)* |
| <b>Paramètre prédéfini par défaut</b> | Lors de l&#39;ouverture de la [fenêtre de cuisson](../../../bakers/bakers.md), vous pouvez la **configurer** avec des boulangers et des paramètres spécifiques en utilisant cette option pour pointer vers un fichier *JSON* prédéfini. Ce fichier peut être exporté à partir de la fenêtre de cuisson une fois qu&#39;il a été configuré selon vos besoins <br><br>*Par défaut : aucun* |
| <b>Mode de filtrage des noms</b> | Objet scène dont le nom doit être utilisé pour correspondre aux objets scène low poly et high poly :<ul data-preserve-html="true"> <li data-preserve-html="true">Nom de la géométrie : utilisez le nom de l&#39;objet géométrique de maillage</li> <li data-preserve-html="true">Nom du gabarit (hérité) : utilisez le nom du gabarit de l’objet géométrique de maillage (identique à celui de Designer versions 14.1 et antérieures)</li> </ul>*Par défaut : nom de la géométrie* |
| <b>Macros de nom de ressource</b> | Au lieu de l&#39;alias *$(bakername)*, vous pouvez utiliser vos propres chaînes de caractères pour [chaque baker](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings).  Lorsque l&#39;alias ***$(personnalisé)*** est utilisé dans le nom d&#39;image de sortie pour un boulanger, il est remplacé par la chaîne de caractères correspondant à ce boulanger dans la liste. Si une cellule de la liste correspondant à un boulanger reste vide, l&#39;alias *$(personnalisé)* *ne sera pas* remplacé pour ce boulanger.Exemple : la valeur « c-mesh » affectée au boulanger « Courbure Map From Mesh » renommera automatiquement *t\_mymesh\_&#x200B;**$(personnalisé)*** en *t\_mymesh\_&#x200B;**c-mesh*** pour la sortie de Curvature From Mesh baker *only *<br><br>*Default : None* |
| <b>Filtre de nom de sous-maillage</b> | Lorsque vous utilisez l&#39;option **Correspondance par nom** dans les [boulangers](../../../bakers/bakers.md), les parties des versions basse et haute définition d&#39;un maillage sont *correspondantes* si le nom de ces parties avant les **suffixes** définis est *identique*. Ce paramètre vous permet de définir vos propres suffixes en fonction de votre workflow spécifique. Les parties correspondantes des maillages peuvent faire que les rayons ignorent la géométrie indésirable dans les opérations de cuisson. Exemple : l&#39;objet *body-torso&#x200B;**\_low*** dans le maillage *body.fbx* serait mis en correspondance avec l&#39;objet *body-torso&#x200B;**\_high &#x200B;*** dans *body\_high.fbx,* *si ces objets existent* dans ces maillages *.**Par défaut : \_low (Low Poly Mesh) / \_high (High Poly Mesh)*De même,**&#x200B;backfaces&#x200B;**peuvent être *ignoré de manière sélective* pour les parties d&#39;un maillage dont le nom inclut le &#x200B;** suffixe&#x200B;**défini, pour [boulangers spécifiques](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings) qui incluent l&#39;option &#x200B;** Ignorer le fond**<br><br>* Par défaut : \_ignorebf *<br><br>* Remarque :* Les suffixes Ignorer le fond et Filet poly faible/élevé peuvent être *combinés dans n&#39;importe quel ordre* (par exemple. *body-torso\_low\_ignorebf*) |

### Gestion des couleurs

Consultez la page [Gestion des couleurs](../../../color-management/color-management.md).

>[!WARNING]
>
> Les modifications apportées à ces paramètres prendront effet après le redémarrage de Designer.

### Général

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modèles de Substance</b> | Lors de la création d&#39;un graphique, vous êtes invité à commencer à travailler à partir d&#39;un **modèle** qui peut avoir un certain nombre de paramètres et de contenus *préconfigurés*, tels que des sorties (par exemple *PBR (métallique/rugosité)*). Ce paramètre vous permet de pointer Designer vers des répertoires où vous pouvez stocker vos propres fichiers SBS à utiliser comme modèles. Vos modèles personnalisés seront ensuite *ajoutés à la liste* lors de la création d&#39;un graphique <br><br>*Par défaut : aucun *<br><br>*Remarque :* Nous vous recommandons d&#39;utiliser les modèles actuels comme référence pour la configuration et le formatage de vos fichiers SBS de modèle.  Les modèles se trouvent dans le dossier **ressources > modèles** du répertoire d&#39;installation de Substance 3D Designer. |
| <b>scènes 3D</b> | Par défaut, Designer utilise l&#39;**espace de tangente MikkT** dans vue 3D. MikkT est largement utilisé et constitue la valeur par défaut dans des programmes tels que Unity, Unreal Moteur 4, Blender et xNormal. Vous pouvez utiliser **votre propre espace de tangente** pour la vue 3D, que vous fournissez à Designer sous la forme d&#39;un *fichier DLL* d&#39;entrée dans ce paramètre. Le libellé est détecté automatiquement à partir du fichier DLL et vous pouvez modifier la description du plug-in <br><br>*Par défaut : mikktspace.dll* Toujours recalculer les cadres de tangente <br><br>*Par défaut : décoché* Angle de lissage normal et de Tangente <br><br>*Par défaut : 180,0°* |
| <b>Divers</b> | Les mappages normaux peuvent être générés ou traités à l&#39;aide du format <b>DirectX</b> ou <b>OpenGL</b>. Ce paramètre définit la valeur de ce format à plusieurs endroits, tels que les [propriétés du matériau](../../../interface/3d-view/material-properties/material-properties.md) dans les paramètres des nœuds de filtre [Vue 3D](../../../interface/3d-view/3d-view.md) et [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md).<br><br>*Par défaut :*<br><br> En ce qui concerne le nœud de filtre [Normal](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), vous pouvez définir la valeur par défaut pour le paramètre <b>Contenu du canal d&#39;Alpha</b>. Vous pouvez choisir de forcer l&#39;alpha à 1 dans tous les cas ou de la remplir avec les informations de son entrée.<br><br>*Par défaut : Forcer l&#39;Alpha à 1* |
| <b>Formats d&#39;image</b> | Cela vous permet de spécifier les paramètres de format par défaut pour les *images exportées*<br><br>*valeurs par défaut : ondelette par défaut (BMP) / basée sur les pixels, décochée, décochée (EXR) / Décochée, décochée, 75 (JPG) / Meilleure vitesse, décochée (PNG) / Par défaut (TGA) / LZW (TIF) / Décochée, 75 (WEBP)* |
| <b>Chemins des dépendances</b> | <p>Les packages SBS ont généralement des <b>dépendances</b>, c&#39;est-à-dire qu&#39;ils dépendent de <i>ressources externes</i> telles que d&#39;autres packages SBS, bitmaps ou fichiers vectoriels.<br>Ces dépendances, qui sont répertoriées dans le [Gestionnaire de dépendances](../../../interface/dependency-manager/dependency-manager.md), sont stockées et <i>référencées dans le package SBS</i> avec un <b>chemin</b> qui pointe vers ces ressources.</p><p>Pour les dépendances qui incluent le <i>même chemin</i> que le package SBS (c&#39;est-à-dire qu&#39;elles se trouvent aux mêmes emplacements ou dans le(s) sous-dossier(s) à partir de cet emplacement), le chemin de référence est écrit <b>par rapport</b> à l&#39;emplacement du package SBS.</p><p>Exemple : pour un package SBS <code>myproject/mypackage.sbs</code>, une image <code>myproject/myfolder/myimage.png</code> sera référencé à <code>myfolder/myimage.png</code> chemin dans <code>mypackage.sbs</code>).</p><p>Pour les dépendances qui n&#39;incluent <i>pas</i> le même chemin d&#39;accès que le package SBS (c&#39;est-à-dire qui se trouvent à un emplacement complètement différent du package SBS), vous pouvez choisir la façon dont le chemin d&#39;accès est écrit.</p><p>S&#39;il est défini sur <b>chemins relatifs</b>, la ressource sera référencée de la même manière que décrite ci-dessus.</p><p>Exemple : pour un package SBS <code>myparentfolder/myproject/mypackage.sbs</code>, une image <code>myparentfolder/myotherfolder/myimage.png</code> sera référencé à <code>../myotherfolder/myimage.png</code> chemin dans <code>mypackage.sbs</code>.</p><p>S&#39;il est défini sur <b>chemins absolus</b>, la ressource sera référencée par son chemin système complet.</p><p>Exemple : pour un package SBS <code>myparentfolder/myproject/mypackage.sbs</code>, une image <code>myparentfolder/myotherfolder/myimage.png</code> sera référencé à ce même chemin complet dans <code>mypackage.sbs</code></p><p><i>Par défaut : ...chemins relatifs.</i></p><p><i>Remarque :</i> dans tous les cas, le déplacement des ressources <i>rompra les dépendances</i> , ce qui entraînera l&#39;<b>apparition de nœuds d&#39;instance fantôme</b> dans les graphiques.  Pour <i>consolider</i> toutes les dépendances dans un seul dossier de projet avec le package SBS, vous pouvez utiliser les fonctionnalités <b>Exporter avec les dépendances...</b> dans le panneau [Explorateur](../../the-explorer-window/the-explorer-window.md). Cela crée efficacement un dossier de projet <i>autonome</i> qui peut être déplacé librement. |

### Bibliothèque

Cette section vous permet de <b>gérer le contenu personnalisé</b> de la [bibliothèque](../../../interface/the-library/the-library.md).

Le contenu de tous les dossiers répertoriés dans la liste <b>Chemins ajoutés</b> sera inclus dans la bibliothèque. Toute modification apportée au contenu est répercutée dans la bibliothèque, après une période d&#39;actualisation qui peut être définie dans l&#39;[&#128279;](../../../interface/preferences-window/preferences-window.md)onglet[Bibliothèque](../../../interface/preferences-window/preferences-window.md) de la fenêtre [Préférences](../../../interface/preferences-window/preferences-window.md).

Dans les colonnes de la liste, vous trouverez des options vous donnant un contrôle plus précis sur la façon dont le contenu de ces dossiers est ajouté à la bibliothèque :

* **Activé :** le contenu du dossier est affiché dans la bibliothèque (*Par défaut : coché*)
* **Récursif :** le contenu de tous les dossiers enfants est également affiché dans la bibliothèque (*Par défaut : coché*)
* **Exclure le modèle :** Les fichiers dont *name* correspond à l&#39;expression régulière d&#39;entrée Regex (expression régulière) sont *non* affichés dans la bibliothèque (par exemple `wip-*`). En savoir plus sur la syntaxe d&#39;expression régulière [ici](https://doc.qt.io/qt-5/qregularexpression.html#wildcardToRegularExpression)
* **Exclure l&#39;extension :** les fichiers qui *incluent* la chaîne de texte d&#39;entrée ne sont *pas* affichés dans la bibliothèque. Les chaînes multiples doivent être séparées par `;` points-virgules. (E.g. `jpg;png;tif;fbx`)

Si des packages SBS sont ajoutés à la bibliothèque, les **graphes** et les **ressources** qu&#39;elle contient peuvent être *affichés dans la bibliothèque* en tant qu&#39;entrées distinctes, si leur paramètre **Visible dans la bibliothèque** est défini sur &#39;Oui&#39;.\
Des options sont disponibles pour définir si ce paramètre doit être défini sur &#39;Oui&#39; *par défaut* lors de la création/l&#39;ajout d&#39;un graphique ou d&#39;une ressource dans un package.

*Par défaut : coché*

Si un document [Photoshop](https://www.adobe.com/products/photoshop.html) (fichier\*.PSD) inclus dans la bibliothèque comporte <b>plusieurs calques</b>, une option vous permet d&#39;afficher le contenu de* chaque calque sous la forme d&#39;une entrée d&#39;image distincte* dans la bibliothèque.

*Par défaut : coché*

>[!NOTE]
>
> Vos ressources personnalisées seront ajoutées à la bibliothèque, mais elles risquent de *ne pas être visibles* en raison des règles de filtrage définies pour les catégories de bibliothèque existantes. Nous vous recommandons de créer *vos propres filtres* organisés dans des dossiers, pour garantir la fiabilité de la recherche de votre contenu lorsque vous travaillez sur vos projets.\
> Voir la section [Gestion du contenu et des filtres personnalisés](../../the-library/managing-custom-content/managing-custom-content-and-filters.md) de la documentation pour plus d&#39;informations.

### Python

Substance 3D Designer chargera automatiquement tous les [plug-ins](../../../scripting/plugin-basics/plugin-basics.md) situés dans les dossiers que vous ajoutez à la liste <b>Url</b>.

*Par défaut : aucun*

>[!WARNING]
>
> Les modifications apportées à ces paramètres prendront effet après le redémarrage de Designer.\
> [Les packages de plug-ins](../../../scripting/plugins-packages/plugins-packages.md) doivent encore être installés *manuellement* à l&#39;aide du [gestionnaire de plug-ins](../../../scripting/plugin-manager/plugin-manager.md).

### Script

>[!WARNING]
>
> Cette fonctionnalité sera *retirée* dans une prochaine version en faveur de l&#39;**API Python** plus robuste. Par conséquent, nous vous recommandons de basculer vos scripts dès que possible.\
> Pour commencer, vous pouvez accéder à la page [Rappels d&#39;application](../../../scripting/application-callbacks/application-callbacks.md) dans la section [Scripts](../../../scripting/scripting.md) de notre documentation.

Cette section vous permet de configurer et de contrôler *scripts* à exécuter lorsque des *événements* spécifiques se produisent dans Designer. Elle est particulièrement utile lorsqu&#39;elle est utilisée conjointement avec l&#39;intégration [Perforce](https://www.perforce.com/) qui peut être configurée dans l&#39;onglet Contrôle de version des paramètres du projet.

|                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Actions</b> | Designer a préconfiguré **des déclencheurs de rappels**, qui *exécuteront le script* que vous fournissez à l&#39;aide de l&#39;interpréteur configuré dans la liste **Interpréteurs** décrite ci-dessous.Les rappels inclus sont les suivants :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>onBeforeFileLoaded</strong> : exécute le script <em>avant</em> le chargement d&#39;un package SBS</li><li data-preserve-html="true"><strong>onAfterFileLoaded</strong> - exécute le script <em>après</em> le chargement d&#39;un package SBS</li><li data-preserve-html="true"><strong>onBeforeFileSaved</strong> : exécute le script <em>avant</em> l’enregistrement d’un package SBS</li><li data-preserve-html="true"><strong>onAfterFileSaved</strong> - exécute le script <em>après</em> l&#39;enregistrement d&#39;un package SBS</li><li data-preserve-html="true"><strong>getGraphExportOptions</strong> : exécute le script lorsque les options [Exporter les sorties](../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) sont appelées</li></ul>Un script [Python](https://www.python.org/) est inclus dans les fichiers d&#39;installation. Les fonctions déclenchées par chaque rappel *sont déjà configurées* et prêtes à être utilisées. Vous pouvez l’utiliser comme point de départ et ajouter des fonctionnalités en fonction de vos besoins. Ce script est **function.py**. Il se trouve dans le dossier **tools > scripting** des fichiers d&#39;installation <br><br>*Par défaut : aucun *<br><br>*Remarque :* Au départ, la sélection d&#39;un script pour l&#39;un des rappels entrera ce script dans les rappels *tous* pour des raisons de commodité. Vous pouvez librement configurer différents scripts pour des rappels spécifiques après ce point. |
| **Interprètes** | Dans cette liste, vous pouvez fournir des *interpréteurs* spécifiques que Designer doit utiliser pour exécuter les scripts configurés dans la liste **Actions** décrite ci-dessus. Les interprètes sont identifiés à l&#39;aide d&#39;un *alias personnalisé* que vous pouvez modifier dans le champ de texte de chaque entrée de la liste.Un interpréteur [Python](https://www.python.org/) 3.6 est fourni avec les fichiers d&#39;installation de Designer. Vous le trouverez dans le dossier **plug-ins > pythonsdk** des fichiers d&#39;installation <br><br>*Par défaut : aucun* |

### Gestion de versions

>[!WARNING]
>
> [Perforce](https://www.perforce.com/) est l&#39;outil *uniquement* qui est actuellement pris en charge pour le contrôle de version.

Reportez-vous à la page [Contrôle de version](../../../interface/preferences-window/version-control/version-control.md).

**Comment devriez-vous l’utiliser ?**

Vous devez définir toutes les préférences *spécifiques au projet* dans un fichier de projet (\*.sbsprj) dans Designer. Ces préférences sont les suivantes :

* Plug-in d’espace tangent
* Bibliothèque
* Alias
* Paramètres de la vue 3D
* Paramètres de cuisson
* [Paramètres de contrôle de version](../../../interface/preferences-window/version-control/version-control.md)

Tous les chemins sont stockés *par rapport à* le fichier de projet (.spsprj). ainsi, vous pouvez avoir un dossier **bibliothèque** au même emplacement que votre fichier de projet dans Perforce, avec l&#39;arborescence de sous-dossiers suivante :

* maps/
* maillages/
* sbs/
* sbsar/
* psd/
* 3Dview/
* ...

Au même niveau que le fichier de projet, vous pouvez également stocker un plug-in d’espace tangent ou un shader par défaut.

Le fichier de configuration (\*.sbscfg) doit être placé dans l’espace de travail Perforce à côté du fichier de projet.

>[!NOTE]
>
> Pour plus d&#39;informations sur la configuration et l&#39;intégration de Substance 3D Designer dans un **pipeline de production**, nous *recommandons vivement* en nous référant à la section [Configuration du pipeline et du projet](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) de la documentation.
