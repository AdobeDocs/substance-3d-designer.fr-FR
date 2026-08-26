---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: Découvrez comment récupérer le chemin d’installation de Substance 3D Designer à des fins de script et d’automatisation.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Récupération du chemin d’installation
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# Récupération du chemin d’installation

Cette page regroupe des informations sur la façon de récupérer le chemin d&#39;installation de [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) en fonction de la version et de la plate-forme.

## Windows

### Application pour poste de travail Creative Cloud

1. Ouvrez l&#39;<b>éditeur de registre Windows</b> (regedit)
1. Accédez à la clé de registre : <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\&lt;/b>
1. Ouvrez la sous-clé nommée <b>Adobe Substance 3D Designer.exe</b>
1. La valeur de la clé contient le chemin d’accès à l’exécutable de l’application sur lequel elle est installée

>[!NOTE]
>
> Cette clé de registre est uniquement disponible depuis la version 11.2.\
> Pour les anciennes versions, le chemin d’installation peut être récupéré à partir des associations de fichiers dans HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts

### Substance edition (autonome)

1. Ouvrez l&#39;<b>éditeur de registre Windows</b> (regedit)
1. Accédez à la clé de registre : <b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. Recherchez la sous-clé correspondant à <b>AppID</b> de la version de votre application (voir le tableau ci-dessous).
1. La valeur de la clé contient le chemin d’accès à l’emplacement d’installation de l’application

| Version | AppId |
| --- | --- |
| **Version 5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **Version 6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **Version 7.x (2017.x) à 11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **Version 11.2 (ou plus récente)** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Édition Steam

L’application est installée dans le sous-dossier steamapps/common/ du dossier d’installation de Steam.

## macOS

Sous Mac, l’application est installée dans les emplacements suivants :

| Version | Chemin |
| --- | --- |
| **11.2 ou version plus récente** | **/Applications/Adobe Substance 3D Designer.app** |
| **Hérité** | **/Applications/Substance Designer.app** |

## Linux

Sous Linux, le package rpm est installé dans le chemin suivant :

| Version | Chemin |
| --- | --- |
| **11.2 ou version plus récente** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **Hérité** | **/opt/Allegorithmic/Substance\_Designer** |
