---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: Découvrez comment utiliser les listes de configuration SBSCFG dans Substance 3D Designer pour gérer les paramètres et les préconfigurations de projet.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Liste de configuration - SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Liste de configuration - SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Le fichier de configuration est beaucoup plus simple que les [fichiers de configuration de projet](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md), car il contient uniquement une liste de projets, ainsi qu&#39;un mode de compatibilité du moteur. Ils servent de liste de configuration de projet/environnement de niveau supérieur à celle des fichiers de projet uniques.

Vous pouvez avoir plusieurs configurations pour différents environnements, ces fichiers peuvent être maintenus sous contrôle de version avec les fichiers SBSPRJ.

</td>
<td width="25.00%" style="border: 0;" valign="top">

Icône de fichier ![SBSCFG](../../assets/sbscfg.png "Icône de fichier SBSCFG")

</td>
</tr>
</table>

## Modification des fichiers de configuration

Ces fichiers sont simples, mais ils peuvent être modifiés de deux manières différentes, tout comme les fichiers SBSPRJ.

### Dans les paramètres du projet

La section en surbrillance est la partie qui concerne les fichiers de configuration, vous ajoutez simplement plus de projets à la liste qui sont stockés dans le fichier SBSCFG défini ci-dessus.

![Paramètres du projet](../../assets/config-ui.png "Paramètres du projet")

### Modification externe au format XML

Pour Windows, le <b>Bloc-notes++</b> est une bonne option gratuite, tandis que le <b>texte sublime</b> de macOS est une alternative. Cependant, n&#39;importe quel éditeur avec le retrait approprié, la réduction de section et une certaine forme de mise en surbrillance de syntaxe vous rendra la vie beaucoup plus facile.

Une fois que vous avez ouvert le fichier SBSCFG dans un éditeur, vous devriez voir une disposition structurée assez simple, avec des sections correspondant à l&#39;interface utilisateur.

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


Notez que les projets par défaut et utilisateur ne sont pas explicitement répertoriés et que tout projet supplémentaire est défini après ces projets.

L&#39;exemple ci-dessus utilise également des [chemins relatifs](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md). Notez que la logique pour les chemins relatifs est légèrement différente entre les fichiers CFG et PRJ : pour les fichiers CFG, comme ci-dessus, **vous ne devez pas taper « file:/ » avant le chemin**. Au lieu de cela, le chemin est simplement ajouté à l&#39;emplacement du fichier CFG dans lequel il est défini.

## Suppression de la bibliothèque par défaut

Pour l’instant, la bibliothèque par défaut ne peut pas être supprimée. Ce n’est probablement pas une bonne idée de le faire de toute façon, car vous perdriez beaucoup de fonctionnalités de Designer.
