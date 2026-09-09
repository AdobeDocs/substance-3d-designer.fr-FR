---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: Configurez les chemins de recherche des plug-ins dans Substance 3D Designer pour spécifier où se trouvent les plug-ins Python.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Chemins de recherche des plug-ins
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Chemins de recherche des plug-ins

Designer recherchera les plug-ins dans des répertoires spécifiques (c’est-à-dire des chemins de recherche). Cette page explique comment configurer ces chemins d’accès.

Les utilisateurs peuvent *ajouter des répertoires personnalisés* manuellement dans les préférences du logiciel ou les spécifier à l&#39;aide de variables d&#39;environnement.

## Ajout manuel de chemins de recherche de plug-ins

1. Accédez à <b>Modifier > Préférences...</b>
1. Sélectionnez la catégorie <b>Projets</b>
1. Sélectionnez le <b>fichier de projet</b> que vous souhaitez modifier
1. Dans l’onglet <b>Python</b>, cliquez sur le bouton *<b>+</b>*pour ajouter le répertoire contenant les plug-ins
1. Cliquez sur <b>OK</b> pour valider

![Configuration des plug-ins Python chemins de recherche Paramètres du projet](../../assets/image-70.png "Configuration des plug-ins Python chemins de recherche Paramètres du projet")

## Utilisation de variables d’environnement

L’application recherchera les plug-ins dans tous les chemins spécifiés à l’aide de la variable d’environnement <b>SBS\_DESIGNER\_PYTHON\_PATH</b>.
