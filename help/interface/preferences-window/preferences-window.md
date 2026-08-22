---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/preferences-window.html"
breadcrumb-title: ''
description: Accédez à la fenêtre Préférences de Substance 3D Designer pour personnaliser les paramètres et le comportement de l’application.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Préférences
user-guide-description: ''
user-guide-title: ''
source-git-commit: b1b28e909a4d3c19c1dbc28e5ed25b3adc327ac3
workflow-type: tm+mt
source-wordcount: '2030'
ht-degree: 1%

---


# Fenêtre Préférences

![Fenêtre Préférences](../../assets/image2021-6-22-20-56-1.png "Fenêtre Préférences")

Cette page présente la fenêtre <b>Préférences</b> et tous ses paramètres.

Vous trouverez la fenêtre Préférences via le menu <b>Modifier</b> dans la barre supérieure principale de l&#39;application. Cette boîte de dialogue permet d’ajuster un certain nombre de paramètres. Il est organisé en onglets couvrant différents domaines de comportement et de fonctionnalité.\
Nous vous recommandons de passer en revue tous ces paramètres pour mieux comprendre le fonctionnement de l’application et la façon dont elle peut être adaptée à votre workflow.

>[!NOTE]
>
> Pour plus d&#39;informations sur la façon dont ces préférences sont stockées et dont vous pouvez les intégrer dans un environnement de production, vous pouvez consulter la page [Préférences utilisateur - Configuration automatisée](../../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) de la documentation.

## Général

### Documents récents

|  |  |
| --- | --- |
| <b>La liste des documents récents contient</b>  *Par défaut : 10* | Cela vous permet de sélectionner le nombre de documents à répertorier dans l&#39;entrée <b>Packs récents</b> de l&#39;élément <b>Fichier</b> dans le [Menu principal](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html). |

### Historique

|  |  |
| --- | --- |
| **Taille de la pile d&#39;historique** *Par défaut : 200* | Cela indique le nombre d&#39;opérations d&#39;annulation disponibles à tout moment dans l&#39;élément <b>Modifier > Annuler</b> du [menu principal](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html).  **Attention :** plus vous aurez besoin d&#39;opérations d&#39;annulation, plus l&#39;application aura besoin de mémoire. |

### Langue

|  |  |
| --- | --- |
| **Choisir la langue de l&#39;application** *Par défaut : système* | Ce paramètre définit la langue utilisée dans l’interface de l’application. L&#39;option « *Système* » détecte automatiquement la langue à partir des paramètres de langue de votre système. Les langues disponibles sont répertoriées dans notre [Configuration requise](../../getting-started/system-requirements/system-requirements.md).  **Remarque :** la modification de ce paramètre ne prendra effet qu&#39;après le redémarrage de l&#39;application. |

### Vues

|  |  |
| --- | --- |
| <b>Inverser le zoom avant</b>  *Par défaut : décoché* | Si cette case est cochée, les commandes de zoom seront inversées dans la [vue 2D](../../interface/2d-view/2d-view.md), la [vue 3D](../../interface/3d-view/3d-view.md) et les [graphiques](../../interface/the-graph-view/the-graph-view.md). |

### Chemins

|  |  |
| --- | --- |
| <b>Chemin d&#39;enregistrement/d&#39;exportation</b>  *Par défaut : dernier chemin* | Détermine si le chemin d&#39;enregistrement/d&#39;exportation suggéré est le dernier chemin sélectionné ou le chemin du [package SBS](../../getting-started/overview/overview.md). Le dernier chemin sélectionné est enregistré d’une session à l’autre. |
| <b>Dossier temporaire</b>  *Par défaut : chemin en fonction du système d&#39;exploitation du système* | Lorsque les données d&#39;image d&#39;un graphique dépassent le pool de mémoire alloué (voir ci-dessous <b>Mémoire > Cache d&#39;images</b>), les données de débordement sont écrites sur le disque. Ce paramètre vous permet de définir l’emplacement dans lequel les données de la mémoire cache de l’image débordante sont écrites.   Cet emplacement est également utilisé pour stocker une copie du package SBS actuellement ouvert avec les dernières modifications apportées depuis le dernier enregistrement manuel. |

### Mémoire

#### Cache d&#39;image

L&#39;application conserve dans le cache une *image pleine résolution non compressée* pour chaque nœud rendu dans le graphique actuel.\
Les nœuds d&#39;instance génèrent ces images pour tous les nœuds du graphique qu&#39;ils référencent et les suppriment une fois leurs [sorties](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) calculées. Seules les sorties sont conservées en mémoire à ce moment-là.

Vous pouvez définir la taille maximale de cache allouée aux vignettes et aux images dans la mémoire système et voir l’utilisation actuelle. Si les données du cache débordent de leur pool alloué, les données excédentaires sont écrites dans le <b>dossier temporaire</b> (voir plus haut <b>Chemins > dossier temporaire</b>).

|  |  |
| --- | --- |
| <b>Budget mémoire</b>  *Par défaut : automatique* | Cette allocation est calculée automatiquement à environ 75 % du pool de mémoire système total. Pour définir cette valeur manuellement, sélectionnez l&#39;option &#39;*Personnalisé*&#39; et définissez une valeur dans le champ de saisie adjacent. |

Notez que l&#39;écriture sur le disque est *de ordres de grandeur plus lente* que l&#39;écriture sur la mémoire système. Par conséquent, le temps de rendu des graphiques *augmentera de manière exponentielle*, car les données qui débordent doivent être écrites dans le dossier temporaire.\
Pour éviter cela, nous vous recommandons d&#39;examiner les suggestions de réduction de l&#39;empreinte mémoire d&#39;un graphique dans la section [Directives d&#39;optimisation des performances](../../best-practices/performance-optimization/performance-optimization-guidelines.md) de la documentation.

#### Planificateur de tâches

Au cours de tâches spécifiques, telles que les conversions d&#39;images pour les vignettes ou la [Vue 2D](../../interface/2d-view/2d-view.md), des tâches distinctes seront créées et réparties entre les cœurs de traitement du système pour plus d&#39;efficacité. Chaque tâche écrira des données dans la mémoire système pour effectuer ses opérations.\
Ce paramètre vous permet de définir le pool de mémoire alloué pour *toutes les tâches simultanées*. Lorsque ce pool est entièrement utilisé, les nouveaux travaux sont mis en file d&#39;attente jusqu&#39;à ce que les travaux actuels soient terminés.

|  |  |
| --- | --- |
| <b>Budget mémoire</b>  *Par défaut : automatique* | Cette allocation est calculée automatiquement à environ 10 % du pool de mémoire système total. Pour définir cette valeur manuellement, sélectionnez l&#39;option &#39;*Personnalisé*&#39; et définissez une valeur dans le champ de saisie adjacent. |

### Interface utilisateur

|  |  |
| --- | --- |
| **Désactiver la haute résolution** *Par défaut : décochée* | Le mode <b>PPP élevée</b> conserve la mise à l&#39;échelle cohérente des éléments de texte et d&#39;interface utilisateur *indépendamment* des paramètres d&#39;affichage et de mise à l&#39;échelle du système.   La désactivation de ce paramètre (case à cocher *rempli*) permet de mettre l’interface à l’échelle. Le texte affiché est alors plus grand et plus lisible, mais cela peut également créer des incohérences dans la taille du texte, ainsi que d’autres problèmes de mise en page.  **Attention :** Designer acquiert l&#39;échelle spécifique des éléments de l&#39;interface utilisateur *à partir du système d&#39;exploitation*. Par conséquent, tout réglage de la mise à l’échelle de l’interface utilisateur doit être effectué dans les paramètres d’affichage du système d’exploitation. Pour vous assurer que les paramètres d&#39;affichage sont appliqués correctement dans Designer, *déconnectez-vous* de votre session utilisateur du système d&#39;exploitation et reconnectez-vous après avoir modifié ces paramètres.  **Remarque :** la modification de ce paramètre ne prendra effet qu&#39;après le redémarrage de l&#39;application. |

### Sauvegarde automatique

Une fonctionnalité d&#39;enregistrement automatique est incluse par défaut, qui crée des copies de l&#39;état actuel des [packs SBS](https://docs.substance3d.com/display/DRAFTDESIGNER/.Overview+vDraftVersion) ouverts à des périodes définies. Les enregistrements automatiques sont placés dans un dossier <b>.autosave</b> à l’emplacement du package SBS.

|  |  |
| --- | --- |
| <b>Sauvegarde automatique toutes les # minutes</b>  *Par défaut : 5* | Période entre chaque enregistrement automatique. |
| <b>Garder jusqu’à # versions</b>  *Par défaut : 6* | Nombre maximal d’enregistrements automatiques à conserver à un moment donné. |

Lorsque le nombre maximal de versions est atteint, les sauvegardes plus récentes suppriment les sauvegardes les plus anciennes.\
Notez également que les enregistrements automatiques doivent être ouverts *après leur déplacement* vers l&#39;emplacement d&#39;origine du package SBS. Ils ne doivent *pas* être ouverts à leur emplacement actuel.

### Publication et envoi de fichiers SBSAR

|  |  |
| --- | --- |
| <b>Enregistrez toujours le fichier .sbs lors de la publication vers .sbsar ou de l&#39;envoi vers une autre application</b>  *Par défaut : True* | Contrôle l&#39;enregistrement automatique du package SBS lors de la [publication](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) ou de l&#39;[envoi à une autre application](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/send-to-215286290.html). |

### Cooker

|  |  |
| --- | --- |
| <b>Limite de taille de cuisson</b>  *Par défaut : 8 192 pixels* | Définit la résolution maximale de pixels autorisée pour tous les [nœuds](https://helpx.adobe.com/fr/substance-3d/unlisted/documentation/sddoc/nodes-reference-129368078.html) dans n&#39;importe quel [graphique](../../compositing-graphs/substance-compositing-graphs.md). Les sorties graphiques étant toujours des images carrées de résolutions de puissance 2, la valeur définie ici définit la largeur maximale et l’height, en pixels. |

### Moteur

|  |  |
| --- | --- |
| <b>Limite de cache GPU</b>  *Par défaut : 2 048 Mo* | Ce paramètre vous permet de définir la quantité de mémoire à réserver pour la mise en cache des étapes de rendu. Généralement, la Substance Engine met en cache la sortie de chaque nœud dans un graphique de Substance. |

>[!NOTE]
>
> Nous vous recommandons d&#39;examiner les suggestions de réduction de l&#39;empreinte mémoire d&#39;un graphique dans la section [Directives d&#39;optimisation des performances](../../best-practices/performance-optimization/performance-optimization-guidelines.md) de la documentation.

## Projets

Reportez-vous à la page [Paramètres des projets](../../interface/preferences-window/project-settings/project-settings.md).

## Graphe

### Commun

|  |  |
| --- | --- |
| La touche de tabulation <b>affiche le menu du nœud</b>  *Par défaut : coché* | Si cette case est cochée, la touche Tab ouvre le menu <b>Nœud</b>, en répliquant la fonctionnalité de la touche Espace. |
| <b>Activer la création de nœuds en faisant glisser les connecteurs</b>  *Par défaut : coché* | Si cette case est cochée, lorsque vous cliquez sur un connecteur, faites glisser le curseur et relâchez le lien créé dans l&#39;espace vide du graphique pour afficher le <b>menu Nœud</b>.   Le menu sera également *filtré* en fonction du type du connecteur sur lequel vous avez cliqué. Cela signifie que seuls les nœuds compatibles avec le connecteur cliqué seront affichés. |
| <b>Afficher les sorties en vue 3D lors de l’ouverture d’un graphique</b>  *Par défaut : coché* | Si cette case est cochée, toutes les sorties de graphique sont automatiquement appliquées dans la [Vue 3D](../../interface/3d-view/3d-view.md) lorsque ce graphique est ouvert.   Cela a également pour effet de rendre tous les nœuds qui font partie d&#39;un flux menant à un nœud [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |

### Graphe de composition Substance

|  |  |
| --- | --- |
| <b>Calculer automatiquement toutes les miniatures de nœuds lors de l&#39;ouverture d&#39;un graphique</b>  *Par défaut : coché* | Si cette case est cochée, le rendu de toutes les miniatures de nœud est automatique lors du chargement du graphique. |
| <b>Afficher la sortie en vue 2D lors de l’ouverture d’un graphique</b>  *Par défaut : coché* | Si cette case est cochée, la première sortie de graphique s&#39;affiche automatiquement dans la [Vue 2D](../../interface/2d-view/2d-view.md) lorsque ce graphique est ouvert. Cela a également pour effet de rendre tous les nœuds qui font partie d&#39;un flux menant à ce nœud [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |
| <b>Afficher automatiquement le nœud de composition nouvellement créé</b>  *Par défaut : coché* | Si cette case est cochée, la [Vue 2D](../../interface/2d-view/2d-view.md) se mettra automatiquement à jour pour afficher la sortie d&#39;un nœud nouvellement créé. |
| <b>Insérer automatiquement le nœud de conversion couleur/niveaux de gris</b>  *Par défaut : décoché* | Si cette case est cochée, résolvez automatiquement les incohérences de types de connexion Couleur/Niveaux de gris en *plaçant des nœuds spécifiques* pour effectuer la conversion appropriée.   Lorsqu&#39;une sortie *Niveaux de gris* (connecteur gris) est connectée à une entrée *Couleur* (connecteur jaune), un nœud [Courbe de transfert de dégradé](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) est automatiquement placé entre les deux connecteurs.   Lorsqu&#39;une sortie *couleur* (connecteur jaune) est connectée à une entrée *niveaux de gris* (connecteur gris), un nœud [conversion des niveaux de gris](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) est automatiquement placé entre les deux connecteurs. |
| <b>Activer la modification de graphiques en contexte</b>  *Par défaut : décoché* | Par défaut, lorsque vous ouvrez un graphique référencé par un [nœud d&#39;instance](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) avec un clic droit sur le nœud et que vous sélectionnez <b>Ouvrir la référence</b>, ce graphique est chargé et modifié *séparément*.   Si cette case est cochée, vous pouvez modifier les graphiques référencés par les instances *à l&#39;aide des informations transmises dans l&#39;instance* par le graphique actuel. Pour ce faire, cliquez avec le bouton droit de la souris sur un nœud d&#39;instance et sélectionnez <b>Ouvrir la référence en contexte</b>, ou utilisez la touche Ctrl+E.   Cela signifie qu’un graphique instancié peut être modifié dans le contexte du graphique dans lequel il est instancié. Cette fonction est très utile pour voir les effets des modifications sur le graphique sur lequel vous travailliez. Voir l’exemple ci-dessous.  **Remarque :** les onglets <b>Aperçu</b> et <b>Paramètres prédéfinis</b> sont *désactivés* dans les [propriétés du graphique](../../compositing-graphs/graph-parameters/graph-parameters.md) lors de l&#39;utilisation de l&#39;édition contextuelle. |

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Modification contextuelle désactivée](../../assets/substance3ddesigner_incontext_no.gif "Modification contextuelle désactivée")

*Ouvrir la référence*

</td>
<td style="border: 0;" valign="top">

![La modification contextuelle a été activée](../../assets/substance3ddesigner_incontext_yes.gif "La modification contextuelle a été activée")

*Ouvrir La Référence En Contexte*

</td>
</tr>
</table>

## Vue 3D

### Divers

|  |  |
| --- | --- |
| <b>Environnement masqué par défaut</b>  *Par défaut : coché* | Détermine le paramètre de visibilité par défaut de [Environnement](../../interface/3d-view/3d-view.md). Lorsque cette option est masquée, l&#39;arrière-plan de la vue 3D est remplacé par une *couleur unie*. |
| <b>Mise à l&#39;échelle de l&#39;aire d&#39;affichage</b>  *Par défaut : Auto* | Contrôle la mise à l’échelle de la résolution de rendu de la vue 3D lorsque le système utilise la mise à l’échelle de l’affichage.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Auto</i> : la résolution de rendu est basée sur la résolution d&#39;affichage <i>mise à l&#39;échelle</i></li> <li data-preserve-html="true"><i>Aucun</i> : la résolution de rendu est basée sur la résolution d&#39;affichage <i>native</i></li> </ul> |

### OpenGL

|  |  |
| --- | --- |
| <b>Nombre d&#39;échantillons</b>  *Par défaut : 64* | A un impact sur la taille de la table d’exemple des ombrages de la vue 3D. Plus la valeur est élevée, plus la qualité de l’image est élevée, au détriment des performances.  **Remarque :** la table d&#39;exemple des nuanceurs est également affectée par le GPU et le système d&#39;exploitation du système. |

## Bakers

|  |  |
| --- | --- |
| <b>GPU raytracing</b>  *Par défaut : coché* | Si cette case est cochée, le lancer de rayons sera effectué sur le GPU pour les [bakers compatibles](https://experienceleague.adobe.com/fr/docs/substance-3d/bakers/features/gpu-raytracing).   Les principaux GPU raytracings suivants seront définis par défaut en fonction de l’architecture GPU NVIDIA :<ul data-preserve-html="true"> <li data-preserve-html="true"><i>DXR</i> : Turing et plus récent</li> <li data-preserve-html="true"><i>Optix</i> : Pascal et Maxwell</li> </ul>  **Remarque :** des informations supplémentaires sur les boulangers optimisés par GPU sont disponibles dans la section [GPU raytracing](https://experienceleague.adobe.com/fr/docs/substance-3d/bakers/features/gpu-raytracing) de la documentation [Substance Bakers](https://experienceleague.adobe.com/fr/docs/substance-3d/bakers/home).  **Conseil :** vous pouvez utiliser les *arguments de ligne de commande* suivants lors du démarrage de l&#39;application pour *forcer* l&#39;utilisation d&#39;un autre back-end de GPU raytracing : <ul data-preserve-html="true"> <li data-preserve-html="true"><code>—force-optix</code> : forcer l’utilisation d’Optix sur les GPU Nvidia Turing ou plus récents</li> <li data-preserve-html="true"><code>—force-dxr</code> : forcer l’utilisation de DXR sur les GPU Nvidia Pascal</li> </ul> |

## Bibliothèque

|  |  |
| --- | --- |
| <b>Vignettes de reconstruction</b> | L&#39;option déclenchera un nouveau calcul de toutes les vignettes de la [bibliothèque](../../interface/the-library/the-library.md), qui remplaceront automatiquement les précédentes. |

## Raccourcis

Vous pouvez attribuer des raccourcis clavier personnalisés pour la création de nœuds dans les graphiques.

Des raccourcis peuvent être attribués pour les nœuds dans tous les types de graphiques : [graphiques de Substance](../../compositing-graphs/substance-compositing-graphs.md), [graphiques de fonction de Substance](../../function-graphs/function-graphs.md) et [graphiques FX-Map](../../function-graphs/fxmaps/fxmaps.md).

Un raccourci peut être attribué à n’importe quel nœud, même aux nœuds de bibliothèque personnalisés. Un même raccourci peut être affecté à différents types de graphiques. Aucun raccourci n’est attribué par défaut, vous pouvez le personnaliser à votre convenance.

En cas de conflit avec un autre raccourci de nœud ou un raccourci de programme intégré, l’entrée est mise en surbrillance et un avertissement s’affiche. Le raccourci n&#39;aura *aucun effet* tant que le conflit n&#39;aura pas été résolu.

>[!IMPORTANT]
>
> Raccourcis remplacés par les plug-ins Python
> 
> Lorsqu’un plug-in Python définit un raccourci clavier attribué à un nœud, le plug-in remplace ce raccourci. Cela signifie que la clé déclenchera l’action du plug-in au lieu de créer un nœud.
> 
> C&#39;est déjà le cas pour les touches H, S et V utilisées par les [outils d&#39;alignement des nœuds](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md).
