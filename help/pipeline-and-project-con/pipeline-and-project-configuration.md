---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: Configurez les paramètres du pipeline et du projet dans Substance 3D Designer pour optimiser votre workflow et votre sortie.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuration du pipeline et du projet
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Configuration du pipeline et du projet

Substance 3D Designer dispose d’un système puissant pour configurer l’application pour l’utilisation du pipeline. Grâce à un système avancé de fichiers hiérarchiques « **Projet** », l&#39;application peut être instantanément configurée selon les normes Studio ou Project, toutes les configurations et le contenu de la bibliothèque étant sous contrôle de version. L&#39;objectif principal du système est de centraliser tous les paramètres pertinents pour le pipeline, tout en permettant à plusieurs configurations de se substituer et de s&#39;étendre les unes aux autres.

>[!WARNING]
>
> Ce système n&#39;est pas destiné aux utilisateurs uniques ayant des exigences plus simples, mais plutôt aux *studios avec de grands projets et des équipes* et un besoin d&#39;organisation plus élevé. Pour tirer pleinement parti de ce système, il est recommandé d&#39;effectuer une bonne planification et une bonne préparation, ainsi qu&#39;un certain degré d&#39;installation automatisée !

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Hiérarchie des fichiers de configuration

Designer dispose de 3 niveaux ou fichiers de configuration, chacun ayant un objectif différent. Sous Windows, tous les fichiers se trouvent dans *~User\AppData\Local\Adobe\Adobe Substance 3D Designer.*

L’image illustre la relation entre les différents fichiers dans la configuration par défaut de Designer, après une nouvelle installation.

</td>
<td style="border: 0;" valign="top">

![Hiérarchie des fichiers de configuration](../assets/filestructureoverview.png "Hiérarchie des fichiers de configuration")

</td>
</tr>
</table>

* <b>[User\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b> contient des paramètres généraux du programme, dont tous sauf un ne sont pas pertinents pour les pipelines du projet. Ce fichier est unique et ne peut pas être échangé, Designer est codé en dur pour utiliser ce fichier exact.\
  Il contient une seule référence à un fichier de configuration.
* <b>[Default\_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b> peut être échangé pour d&#39;autres fichiers SBSCFG avec des noms différents, mais un seul fichier SBSCFG peut être utilisé en même temps.\
  Il contient plusieurs références à des fichiers de projet. *Notez que pour la configuration par défaut, ces fichiers ne sont pas explicitement définis, mais sont codés en dur !*
* Les fichiers <b>[Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b> contiennent des paramètres pertinents pour le projet/pipeline. Plusieurs projets peuvent être définis dans une hiérarchie, en remplaçant ou en développant le projet précédemment défini.

## Configuration du pipeline Designer

Chaque type de fichier est expliqué plus en détail sur les pages enfants de cette page, mais la courte présentation de la définition idéale d’une configuration personnalisée pour Designer est la suivante :

1. <b>Identifiez et regroupez les paramètres à ajouter à vos fichiers de projet.</b> C&#39;est différent pour chaque studio et nécessite une certaine planification !\
   Dans presque tous les cas, au moins 2 projets doivent être définis : un pour les valeurs par défaut globales, à l’échelle du studio (comme les modèles standard, les fichiers de nuanceur, les paramètres de boulangerie) et un avec un contenu plus spécifique, tel que le contenu de la bibliothèque. Si plusieurs projets sont exécutés simultanément, vous pouvez créer plusieurs configurations de projet pour chacun d’eux (soit 3 ou plus au total).
1. <b>Créez les [fichiers SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) pertinents et placez-les, ainsi que leur contenu, sous contrôle de version.</b> Il est fortement recommandé de séparer le contenu du pipeline et de la bibliothèque Designer du contenu et des ressources réelles de votre projet (modèles 3D, textures, code) en créant un *référentiel distinct*.
1. <b>Créez un fichier [&#x200B; Configuration SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) répertoriant tous les fichiers de projet, placez-le sous contrôle de version</b>. Si vous avez plusieurs projets, vous pouvez créer une configuration pour chaque projet.
1. <b>Configurez [User\_Preferences.xml](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) de chaque utilisateur pour référencer son fichier de configuration pertinent.</b>\
   Vous pouvez demander à chaque utilisateur de le faire manuellement ou utiliser un script en injectant des lignes dans son fichier XML. [Plus d&#39;informations sur la page concernée](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md).
