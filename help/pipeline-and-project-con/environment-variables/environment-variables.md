---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: Découvrez comment utiliser des variables d’environnement dans Substance 3D Designer pour configurer les chemins et les paramètres système.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables d’environnement
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# Variables d’environnement

Cette page répertorie les variables d&#39;environnement qui peuvent être utilisées pour remplacer le comportement par défaut de l&#39;application.

| Variable | Description |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | Chemin à partir duquel Designer chargera les [plug-ins Python](../../scripting/plugin-basics/plugin-basics.md). |
| **SUBSTANCE\_DESIGNER\_LICENSE** | L&#39;emplacement du fichier de licence (*license.key*) qui doit être utilisé par Designer.   Remplace le chemin d&#39;accès défini dans l&#39;[Assistant d&#39;activation](../../getting-started/activation-and-licenses/activation-and-licenses.md) de Designer.  **Remarque :** les anciennes versions devront peut-être utiliser un autre nom de variable :<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_LICENSE</strong></li></ul> |
| <b>OCIO</b> | Chemin d&#39;accès au fichier de configuration OCIO qui doit être utilisé lors de l&#39;utilisation de la [gestion des couleurs](../../color-management/color-management.md) OpenColorIO.   Remplace le chemin défini dans les paramètres de gestion des couleurs de Designer dans les [paramètres du projet](../../interface/preferences-window/project-settings/project-settings.md). |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | Le délai en secondes avant de libérer un siège de licence en cas de configuration multi-utilisateurs est de 7 200 secondes (2 heures) par défaut. |
