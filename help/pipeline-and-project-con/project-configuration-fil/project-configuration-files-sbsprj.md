---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: Découvrez comment utiliser les fichiers de configuration de projet SBSPRJ dans Substance 3D Designer pour gérer les paramètres du projet.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fichiers de configuration du projet - SBSPRJ
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Vue d’ensemble

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Les <b>fichiers de configuration de projet</b> sont les fichiers les plus complexes et les plus volumineux utilisés pour configurer Substance 3D Designer.

Ils sont spéciaux dans la mesure où vous pouvez utiliser plusieurs fichiers de configuration de projet, où chaque projet « enfant » suivant développe ou remplace le « parent » précédent. À moins que cela ne soit explicitement nécessaire, les paramètres ne doivent pas être modifiés ou ajoutés aux fichiers du projet, de sorte que Designer puisse revenir à sa configuration parent, voire même aux valeurs par défaut.

</td>
<td width="25.00%" style="border: 0;" valign="top">

Icône de fichier ![SBSPRJ](project-configuration-files-sbsprj.resources/sbsprj.png "Icône de fichier SBSPRJ")

</td>
</tr>
</table>

Par défaut, Designer a deux configurations de projet actives :

<b>Projet par défaut :</b>contient tous les paramètres par défaut et la bibliothèque Designer est livrée avec une nouvelle installation.*Lecture seule, modification ou suppression impossible.*

<b>Projet utilisateur :</b>Étant donné que les valeurs par défaut sont en lecture seule, *toutes les modifications effectuées par l’utilisateur* sont appliquées par défaut à ce projet. *Impossible de supprimer.*

Cette configuration de base garantit que la bibliothèque par défaut et les autres paramètres ne peuvent pas être corrompus ou modifiés, tout en permettant aux utilisateurs amateurs uniques d’ajouter leurs propres modifications sans avoir à se soucier des configurations complexes.

## Développer ou remplacer

La plupart des paramètres d&#39;un projet consécutif <b>remplaceront</b> ceux du projet précédent. Par exemple, un autre Plugin de repère tangent dans un fichier de projet personnalisé remplacera tout plug-in TS défini dans le projet Default ou User. Cela signifie qu’à moins d’en avoir explicitement besoin, il est recommandé de ne pas remplacer ou modifier les paramètres dans les projets enfants.

Certains paramètres <b>se développent</b> sur les paramètres parents, au lieu de les remplacer. Il s’agit principalement des chemins et des filtres de bibliothèque. Vous devez donc toujours ajouter plus de contenu à la bibliothèque au lieu de le remplacer. En outre, il y a les alias (mots-clés de chemin pour les chemins de fichiers relatifs) qui se développent, ainsi que le remplacement si un doublon est défini. Cela permet un excellent contrôle sur les chemins de fichiers de contenu et les références.

## Contenu du fichier de projet

Les fichiers de projet peuvent contenir les paramètres suivants :

<b>vue 3D :</b>définitions d’état de Shader, HDR et scène par défaut.

<b>Alias :</b>Alias de mots-clés pour les chemins relatifs.

<b>Baking :</b>paramètres de baking des conventions de dénomination.

<b>Général :</b>modèles Graphe, plug-ins Repère tangent, formats normal et image par défaut.

<b>Bibliothèque :</b>Tracés suivis à afficher dans la bibliothèque.

<b>Scripts :</b>scripts et interpréteurs de rappel.

<b>Gestion de versions :</b>Paramètres d’intégration de la Gestion de versions dans Designer.

## Modification de fichiers de projet

Les configurations de projet sont, comme tous les autres types, enregistrées en tant que fichiers XML structurés (à l’aide d’une extension <b>.sbsprj</b>) qui peuvent être modifiés via l’interface utilisateur de Designer ou via un éditeur de texte externe.

## Dans Substance 3D Designer

Consultez la page [Paramètres du projet](../../interface/preferences-window/project-settings/project-settings.md) pour en savoir plus sur la gestion des fichiers de projet et la modification des paramètres du projet.

Les fichiers de projet incluent également des <b>catégories</b> personnalisées et des <b>filtres</b> pour la [bibliothèque](../../interface/the-library/the-library.md), pour en savoir plus sur la page [Gestion du contenu et des filtres](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) personnalisés.

## Modifier XML en externe

Pour Windows, [le Bloc-notes++](https://notepad-plus-plus.org) est une bonne option gratuite. Sur macOS, [Sublime Text](https://www.sublimetext.com/) est une alternative. Cela dit, n&#39;importe quel éditeur avec la mise en retrait appropriée, la réduction de section et une certaine forme de mise en surbrillance de syntaxe vous rendra la vie beaucoup plus facile.

Une fois que vous avez ouvert le fichier SBSPRJ dans un éditeur, vous devriez voir une disposition structurée assez simple, avec des sections correspondant aux onglets dans l&#39;interface utilisateur. Tous les paramètres ne seront pas documentés ici, car ils sont assez explicites.

![Modification XML](project-configuration-files-sbsprj.resources/project-xml.png "Modification XML")

## Chemins relatifs et alias

Les chemins relatifs combinés avec des alias sont l&#39;une des parties les plus complexes, mais les plus importantes d&#39;une configuration de projet. Cette section les clarifiera. L&#39;ajout d&#39;alias personnalisés pour un fichier de projet spécifique est effectué dans les [Paramètres du projet](../../interface/preferences-window/project-settings/project-settings.md).

L&#39;un des principaux problèmes avec les fichiers référençant d&#39;autres fichiers dans un système sur le PC de plusieurs utilisateurs, est que les chemins de fichiers absolus ne fonctionneront pas. Les utilisateurs peuvent définir leurs référentiels SVN dans des emplacements complètement différents (p ex. C :/John/Gamedev/SubstanceLibrary ou D :/Dev/SubstanceLibrary). Les alias et les chemins relatifs fonctionnent ensemble pour résoudre ce problème. Sinon, vous pourriez ouvrir le fichier de quelqu&#39;un d&#39;autre et il essaiera de rechercher le nœud personnalisé utilisé dans l&#39;emplacement spécifique où l&#39;utilisateur l&#39;avait localement, que vous n&#39;aurez probablement pas défini exactement de la même manière.

Un <b>alias</b> est un mot-clé qui remplace (fait partie) d&#39;un chemin. Il est similaire à une variable d’environnement Windows comme %TEMP%, où un seul mot remplace un chemin souvent utilisé qui est ensuite défini de manière centralisée. L’avantage est que les tracés sont simplifiés partout et qu’ils permettent de modifier toutes les références en une seule fois lorsque vous décidez de redéfinir l&#39;emplacement ce tracé.

>[!NOTE]
>
> **Exemple d&#39;alias**
> 
> | Alias | Valeur réelle du chemin d’accès |
> | --- | --- |
> | <b>sbs</b> | *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>personnalisé</b> | *D:\Dev\CustomProject\Substance* |
> 
> La bibliothèque par défaut se trouve par défaut à l&#39;emplacement *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages*, et tous les graphes utilisant le contenu par défaut font référence à ce répertoire. Au lieu de référencer le chemin complet, un alias de &#39;<b>SBS</b>&#39; (sans guillemets) est défini. Dans le cas d’une bibliothèque par défaut, la valeur exacte du chemin SBS est définie lors de l’installation dans le répertoire choisi par l’utilisateur pour Designer.
> 
> En interne, une référence est modifiée de la manière suivante, lorsqu’elle contient un chemin avec un alias :
> 
> **C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => <b>sbs://</b>blur\_hq.sbs**

<b>Les chemins relatifs</b> sont toujours relatifs au fichier dans lequel ils sont définis. Cela signifie que l’emplacement actuel du fichier de configuration détermine la plupart du chemin, et les chemins d’alias seront basés sur celui-ci, principalement en ajoutant simplement un sous-dossier. <b>Cela signifie qu&#39;il est fortement recommandé de placer vos fichiers sbsprj à côté des dossiers que vous souhaitez consulter !</b>

Par exemple, prenez un référentiel à l&#39;emplacement *C :/Versioncontrol/Substance/* contenant *CustomProject.sbsprj*, puis deux dossiers, */Base* et */Tools,* contenant des nœuds.

Pour définir deux alias relatifs pour Base et Outils, procédez comme suit dans le fichier SBSPRJ :

### C:/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


Le résultat de ce fichier de configuration est le suivant :

**BaseAlias://** sera *C :/Versioncontrol/Substance/Base/* et **ToolsAlias://** sera *C :/Versioncontrol/Substance/Tools/.*

Si vous souhaitez définir uniquement *C :/Versioncontrol/Substance/*, le chemin d&#39;accès sera indiqué comme **« file:.«**, le point indiquant l&#39;emplacement du fichier lui-même.
