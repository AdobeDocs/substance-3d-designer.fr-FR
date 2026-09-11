---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: Résolvez les problèmes de script Python dans Substance 3D Designer, y compris les problèmes de plug-in et d’API.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problèmes avec Python
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Problèmes avec Python

Cette page répertorie les problèmes techniques liés à l&#39;[API Python](../../scripting/scripting.md) de Substance 3D Designer, ainsi que les fonctionnalités implémentées dans Python, et propose des étapes de dépannage pour chacun d&#39;eux.

Les fonctionnalités implémentées dans Python incluent les actions [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Envoyer à](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) dans la barre d&#39;outils de l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md), ainsi que l&#39;outil permettant de supprimer les nœuds inutilisés dans les graphes.

## Le module &#39;QtForPython&#39; ne se charge pas

<b> ![(error)](../../assets/error.svg) Problème</b>

Le module Python « QtForPython » ne se charge pas, ce qui entraîne des fonctionnalités manquantes implémentées dans Python, telles que les actions [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Envoyer à](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) dans la barre d&#39;outils de [l&#39;Explorateur](../../interface/the-explorer-window/the-explorer-window.md), ainsi que l&#39;outil permettant de supprimer les nœuds inutilisés dans les graphes.

En outre, de nombreux [plug-ins Python](../../scripting/plugin-basics/plugin-basics.md) ne se chargeront pas ou ne fonctionneront pas comme prévu.

<b> ![(tick)](../../assets/check.svg) Étapes recommandées</b>

Il existe probablement un conflit entre l’installation Designer de QtForPython et de ses dépendances et une installation existante sur le système.

Supprimez toute autre installation système de [QtForPython](https://doc.qt.io/qtforpython-5/index.html) ([PySide2](https://pypi.org/project/PySide2/)) et de [Shiboken2](https://pypi.org/project/shiboken2/).

Au lieu d&#39;une installation de QtForPython à l&#39;échelle du système, vous pouvez également envisager d&#39;utiliser des *environnements virtuels* Python ou un *gestionnaire de modules* tel que [rez](https://github.com/AcademySoftwareFoundation/rez).
