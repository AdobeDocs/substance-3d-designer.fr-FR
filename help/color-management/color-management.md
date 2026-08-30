---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/color-management.html"
breadcrumb-title: ''
description: Découvrez la gestion des couleurs dans Substance 3D Designer, notamment les espaces colorimétriques, les profils et les workflows de tons directs.
helpx_creative_field: ""
helpx_description: Designer > Color Management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gestion des couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1678'
ht-degree: 1%

---


# Gestion des couleurs

Cette page explique les fonctionnalités et les paramètres de gestion des couleurs dans Substance 3D Designer.

Substance 3D Designer peut être configuré pour utiliser [OpenColorIO](https://opencolorio.org/) (OCIO) ou Adobe Color Engine (ACE) pour la gestion des couleurs. Cela vous permet d&#39;avoir des transformations de couleur *cohérentes* et un affichage des images dans plusieurs applications.

Dans ce mode, Designer fonctionnera en interne avec les couleurs du **RGB linéaire**. Étant donné que 8 nombres de bits par pixel ne sont généralement pas suffisants pour représenter des couleurs linéaires, il est recommandé d&#39;utiliser la profondeur *au moins* **16 bits** pour les textures de couleur dans le [graphique](../compositing-graphs/substance-compositing-graphs.md).

>[!WARNING]
>
> Un workflow efficace de gestion des couleurs repose sur l&#39;utilisation d&#39;un écran correctement *étalonné*. Des solutions tierces existent pour étalonner correctement votre moniteur pour votre environnement de travail à l&#39;aide d&#39;un matériel spécialisé.
> 
> Les utilisateurs OpenColorIO doivent utiliser des espaces colorimétriques OpenColorIO correspondants pour leurs moniteurs.\
> Les utilisateurs ACE d&#39;Adobe doivent s&#39;assurer que les profils ICC sélectionnés *dans le système d&#39;exploitation* correspondent à *leurs* moniteurs.

## Configuration

Les paramètres de gestion des couleurs peuvent être configurés dans l&#39;onglet [Projets](../interface/preferences-window/project-settings/project-settings.md) de la boîte de dialogue [Préférences](../interface/preferences-window/preferences-window.md). Vous pouvez définir les paramètres suivants :

### Mode de gestion des couleurs

|  |  |
| --- | --- |
| <b>Gestion des couleurs</b> | Ce paramètre vous permet de sélectionner les modes [hérités](../color-management/color-management.md), [OpenColorIO](#opencolorio) ou [Adobe ACE](#adobe-ace) pour la gestion des couleurs dans Substance 3D Designer. *Par défaut : hérité* |

## OpenColorIO

### Configuration OpenColorIO

Lorsque vous utilisez le mode OpenColorIO pour la gestion des couleurs, Designer utilise les informations stockées dans un <b>fichier de configuration</b> (*\*.config*) pour effectuer des transformations de couleur, identifier les espaces colorimétriques et définir des valeurs par défaut.

Substance 3D Designer est livré avec les configurations suivantes :

* Substance : une configuration simple qui inclut des espaces colorimétriques communs
* [ACES 1.0.3](https://github.com/hpd/OpenColorIO-Configs/tree/master/aces_1.0.3) : la configuration complète [Academy Color Encoding System](https://www.oscars.org/science-technology/sci-tech-projects/aces) (ACES), une norme du secteur pour les workflows de gestion des couleurs

Ces fichiers de configuration se trouvent dans le dossier <b>ressources > ocio</b> des fichiers d’installation de Designer.

|  |  |
| --- | --- |
| <b>Configuration OpenColorIO</b> | Ce paramètre vous permet de sélectionner le fichier de configuration OpenColorIO à utiliser dans Designer. Vous pouvez également définir le fichier de configuration OpenColorIO à l’aide de la variable d’environnement OCIO.  Lorsqu&#39;il existera, le fichier de configuration sera *verrouillé* dans Designer. Il est toujours possible de modifier les espaces colorimétriques par défaut et d’afficher les transformations (voir les paramètres ci-dessous).  **Alerte :** après avoir ajouté la variable d&#39;environnement, nous vous recommandons de fermer Designer, de *vous déconnecter* de votre session utilisateur dans le système d&#39;exploitation, puis de vous reconnecter. Cela garantit que la variable d’environnement est activée lors du démarrage de Designer. Vous pouvez également utiliser la ligne de commande pour créer une variable d&#39;environnement temporaire et démarrer Designer à partir de l&#39;environnement de ligne de commande *same*.  *Par défaut : Substance* |
| **Fichier de configuration personnalisé** | Si l&#39;option **Personnalisé** est définie dans **Configuration OpenColorIO**, vous pouvez sélectionner le *fichier \*.config spécifique *à utiliser comme fichier de configuration dans ce champ.* Par défaut : défini par le fichier de configuration OpenColorIO ou la variable d&#39;environnement OCIO* |

### Valeurs par défaut de l’espace colorimétrique du bitmap

|  |  |
| --- | --- |
| <b>Images 8 bits</b> | Définit l’espace colorimétrique par défaut des bitmaps 8 bits. *Par défaut : défini par le fichier de configuration OpenColorIO* |
| <b>Images 16 bits</b> | Définit l’espace colorimétrique par défaut des bitmaps 16 bits. *Par défaut : défini par le fichier de configuration OpenColorIO* |
| <b>Images à virgule flottante</b> | Définit l’espace colorimétrique par défaut pour les bitmaps de précision à virgule flottante, telles que les images *HDR* aux formats *\*.exr *ou*\*.hdr*. *Par défaut : défini par le fichier de configuration OpenColorIO* |
| <b>Utiliser le nom du fichier pour détecter l&#39;espace colorimétrique</b> | Permet à Designer d&#39;attribuer automatiquement un espace colorimétrique si le *suffixe* d&#39;un nom de fichier bitmap *correspond exactement* au nom en minuscules d&#39;un espace colorimétrique inclus dans la *configuration* OpenColorIO actuelle. Exemple : une ressource bitmap *mybitmap\_aces\_acescg.png* serait automatiquement définie sur l&#39;espace colorimétrique *ACE - ACEScg* et le transforme approprié serait appliqué à l&#39;espace colorimétrique de travail. *Par défaut : coché* |

### Affichage 2D et 3D par défaut

|  |  |
| --- | --- |
| <b>Affichage 2D et 3D par défaut</b> | Définit l&#39;espace colorimétrique par défaut de l&#39;*affichage* pour les fenêtres [Vue 2D](../interface/2d-view/2d-view.md) et [Vue 3D](../interface/3d-view/3d-view.md). *Par défaut : défini par le fichier de configuration OpenColor IO* |
| <b>Vignettes de gestion des couleurs</b> | Permet à Designer de transformer automatiquement les *vignettes* du nœud dans l&#39;espace colorimétrique de *travail* du graphe. *Par défaut : coché* |

## Adobe ACE

### Paramètres de couleurs

Lors de l’utilisation du mode ACE Adobe pour la gestion des couleurs, Substance 3D Designer utilise les informations stockées dans <b>Profils ICC</b> (*\*.icc / \*.icm*) pour effectuer des transformations de couleur et identifier les espaces colorimétriques.

Designer est livré avec un certain nombre de profils ICC. Les fichiers de ces profils se trouvent dans le dossier `resources > icc` des fichiers d’installation de Designer.\
Vous pouvez ajouter *vos propres profils ICC* en plaçant ces fichiers à l&#39;emplacement `Adobe/Adobe Substance 3D Designer/icc` dans le dossier *Documents* de l&#39;utilisateur actuel du système.

|  |  |
| --- | --- |
| <b>Espace de travail</b> | Ce paramètre vous permet de sélectionner l&#39;espace colorimétrique de travail pour *effectuer des opérations colorimétriques* dans Substance 3D Designer. *Par défaut : sRGB IEC61966-2.1* |
| <b>Intention de rendu</b> | Cette option vous permet de contrôler la façon dont les couleurs doivent être transformées lorsqu&#39;elles se trouvent *en dehors de la gamme* de l&#39;espace colorimétrique de *travail*. *Valeur par défaut : Colorimétrie relative* |

### Valeurs par défaut de l’espace colorimétrique du bitmap

|  |  |
| --- | --- |
| <b>Images 8 bits</b> | Définit le profil ICC par défaut à utiliser pour les bitmaps 8 bits. *Par défaut :* sRGB IEC61966-2.1 ** |
| <b>Images 16 bits</b> | Définit le profil ICC par défaut pour utiliser les bitmaps 16 bits. **Par défaut :*sRGB IEC61966-2.1*** |
| <b>Images à virgule flottante</b> | Définit le profil ICC par défaut à utiliser pour les bitmaps de précision à virgule flottante, telles que les images *HDR* aux formats *\*.exr *ou*\*.hdr*. *Valeur par défaut : Raw (c’est-à-dire aucun profil appliqué)* |
| <b>Utiliser les profils ICC incorporés lorsqu&#39;ils sont disponibles</b> | Permet à Designer d’utiliser le profil ICC incorporé dans un bitmap au lieu des paramètres par défaut répertoriés ci-dessus. *Par défaut : coché* |

### Espace par défaut de l’affichage des vues 2D et 3D

|  |  |
| --- | --- |
| <b>Affichage 2D et 3D par défaut</b> | Définit l&#39;espace colorimétrique par défaut de l&#39;*affichage* pour les fenêtres [Vue 2D](../interface/2d-view/2d-view.md) et [Vue 3D](../interface/3d-view/3d-view.md). *Par défaut :*** Profil ICC pour l’écran principal, récupéré à partir du système d’exploitation &#x200B;**&#x200B;** |

### Affichage graphique

|  |  |
| --- | --- |
| <b>Vignettes de gestion des couleurs</b> | Lorsque *la case est cochée*, Designer transforme les *vignettes de nœud* sur l&#39;*espace colorimétrique de travail*. *Par Défaut :*** Décoché&#x200B;**&#x200B;** |

## Mode hérité

Lors de l&#39;utilisation du mode <b>hérité</b>, la gestion des couleurs est *désactivée* dans Designer-

Dans ce mode, les graphiques et les images se comportent exactement de la même manière que dans les versions précédentes. Cela signifie que votre workflow des versions précédentes n&#39;est *pas du tout affecté* si ce paramètre n&#39;est pas *modifié*. Il y a cependant quelques ajouts utiles :

Vous pouvez utiliser <b>ACES sRGB</b> *le mappage tonal* dans la <b>vue 3D</b> pour correspondre à la sortie d&#39;autres logiciels, tels que le *[moteur irréel](https://docs.unrealengine.com/en-US/Engine/Rendering/PostProcessEffects/ColorGrading/index.html)*.

Vous pouvez définir un espace colorimétrique pour les *bitmaps exportés* comme décrit dans la section [Exportation des sorties](#exporting-outputs) de cette page. Les espaces colorimétriques disponibles sont les suivants :

* sRVB
* Linéaire
* Raw

En mode hérité, Designer utilise l&#39;<b>espace colorimétrique de travail sRVB</b>, qui peut être reproduit par la plupart des écrans.

Si l&#39;on considère que l&#39;option « Brut » écrit les données d&#39;image *telles quelles* à partir du graphique, c&#39;est-à-dire en utilisant l&#39;espace colorimétrique de travail du graphique, cela signifie que les options <b>Brut</b> et <b>sRVB</b> entraînent la *même sortie couleur*.

Par défaut, l&#39;option &#39;sRGB&#39; est définie pour les sorties qui contiennent *des informations de couleur* (par exemple, Couleur de base, Émissive), et l&#39;option &#39;Raw&#39; est définie pour les sorties qui contiennent *des données pures* (par exemple, Rugosité, Métallique, Height, Normal). Comme expliqué ci-dessus, ces valeurs par défaut produisent en fait les mêmes couleurs et sont définies uniquement pour *différencier l&#39;utilisation finale* de leurs sorties.

L&#39;option <b>Linéaire</b> est la *seule* qui entraîne l&#39;application d&#39;une *transformation des couleurs* à l&#39;image. Elle ne peut être utilisée que pour les images <b>Plage dynamique élevée</b> (HDR), qui utilisent généralement la *précision en virgule flottante* (c&#39;est-à-dire le nombre de bits par pixel 16F ou 32F) dans l&#39;espace colorimétrique linéaire. Cela permet d’utiliser ces images dans un large éventail d’espaces colorimétriques et d’environnements de production.

>[!NOTE]
>
> Pour plus d&#39;informations sur les exportations d&#39;images, consultez la page [Exportation de bitmaps](../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) de la documentation.

## Importation d’images bitmap

Vous pouvez attribuer un <b>espace colorimétrique</b> (OCIO) ou un <b>profil ICC</b> (Adobe ACE) aux images bitmap importées et liées.

Lors de l&#39;importation ou de la liaison d&#39;images bitmap, un espace colorimétrique ou un profil ICC est défini *par défaut* sur la ressource bitmap à l&#39;aide des options définies dans la section <b>Espace colorimétrique bitmap par défaut</b> de l&#39;onglet <b>Gestion des couleurs</b> dans les [paramètres du projet](../interface/preferences-window/project-settings/project-settings.md).

Vous pouvez modifier l&#39;espace colorimétrique d&#39;un bitmap à tout moment. L&#39;option se trouve dans les <b>propriétés</b> de la ressource bitmap.

>[!NOTE]
>
> **OpenColorIO uniquement**
> 
> En particulier, le **nom de fichier** peut être utilisé pour définir l&#39;espace colorimétrique approprié *automatiquement*. Veuillez noter que le nom de l&#39;espace colorimétrique dans le nom de fichier doit *correspondre au nom* dans le fichier de configuration OpenColorIO (par exemple, *myImage\_utility - linear -srgb.png* sera défini sur l&#39;espace colorimétrique *Utility - Linear - sRGB*).

![Paramètre d&#39;espace colorimétrique bitmap](color-management.resources/2019-3-0-bitmap-clr-space.png "Paramètre d&#39;espace colorimétrique bitmap")

## Exportation de sorties

Lors de l&#39;utilisation de la boîte de dialogue <b>Exporter les sorties</b>, il est possible d&#39;attribuer un <b>espace colorimétrique</b> (OCIO) ou d&#39;attacher un <b>profil ICC</b> (ACE Adobe) pour *chaque sortie*.\
Designer va *convertir* les images aux espaces colorimétriques spécifiés avant d&#39;enregistrer les fichiers image.

![Boîte de dialogue Exporter les sorties](color-management.resources/2019-3-0-clr-mgt-export-outputs.png "Boîte de dialogue Exporter les sorties"){width="512px"}

Vous pouvez également attribuer un espace colorimétrique (OCIO) ou joindre un profil ICC (ACE Adobe) aux images *enregistrées* à partir de la [Vue 2D](../interface/2d-view/2d-view.md).

![Options d’exportation de la vue 2D](color-management.resources/2019-3-0-clr-mgt-save-image.png "Options d’exportation de la vue 2D")

## Vues 2D et 3D

### Afficher la barre d’outils

Vous pouvez *activer/désactiver la gestion des couleurs* et modifier la *transformation d&#39;affichage* pour l&#39;affichage à tout moment à l&#39;aide du menu déroulant de la barre d&#39;outils d&#39;affichage.

![Paramètre d&#39;espace colorimétrique dans la vue 2D](color-management.resources/2019-3-0-clr-mgt-display-toolbar.png "Paramètre d&#39;espace colorimétrique dans la vue 2D"){width="512px"}

### Environnements HDRI de bibliothèque

Les environnements HDRI livrés avec Designer se trouvent dans l&#39;espace colorimétrique <b>Linear sRGB</b>.\
Lors de l&#39;utilisation d&#39;une configuration OpenColorIO où l&#39;espace colorimétrique linéaire de la scène est *non* sRVB linéaire, telle que la configuration [ACES](https://acescentral.com/t/getting-started-with-aces/1372), l&#39;environnement affichera *des couleurs incorrectes*.

Dans ce cas, l&#39;espace colorimétrique pour les environnements HDRI de bibliothèque doit être défini *manuellement* dans les propriétés de l&#39;environnement, disponibles dans le menu <b>Environnement</b> du panneau Vue 3D.

![Paramètre d’espace colorimétrique de l’environnement 3D View](color-management.resources/2019-3-0-clr-mgt-hdri-env.png "Paramètre d’espace colorimétrique de l’environnement 3D View"){width="512px"}

## Nœuds de conversion de couleur

La [bibliothèque](../interface/the-library/the-library.md) comprend les nœuds suivants pour effectuer des <b>conversions</b> depuis et vers l&#39;espace colorimétrique ACEScg :

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[Graphe Substance](../compositing-graphs/substance-compositing-graphs.md)

* ACEScg en sRVB linéaire
* SRVB linéaire à ACEScg
* ACEScg à sRGB
* sRGB à ACEScg

</td>
<td style="border: 0;" valign="top">

[Graphe de fonction Substance](../function-graphs/function-graphs.md)

* ACEScg en sRVB linéaire
* SRVB linéaire à ACEScg

</td>
</tr>
</table>

Ils sont utiles lorsque vous travaillez avec des graphiques créés *sans* gestion des couleurs ou des matériaux de la bibliothèque [Actifs Substance 3D](https://substance3d.adobe.com/assets).

![Nœuds de conversion de couleur dans la bibliothèque](color-management.resources/2019-3-0-clr-mgt-nodes.png "Nœuds de conversion de couleur dans la bibliothèque"){width="512px"}

## Limitations connues

La mise en œuvre actuelle de la gestion des couleurs dans Substance 3D Designer présente les limitations suivantes :

* La gestion des couleurs n&#39;est actuellement *pas* exposée dans l&#39;[API Python](../scripting/scripting.md) ;
* Les *looks* [OpenColorIO](https://opencolorio.org/) ne sont *pas* pris(s) en charge.
