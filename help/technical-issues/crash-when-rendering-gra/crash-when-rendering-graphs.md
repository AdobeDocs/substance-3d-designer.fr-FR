---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: Dépannez les crashs lors du rendu des graphes dans Substance 3D Designer et trouvez des solutions pour les éviter.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crash lors du rendu des graphes
user-guide-description: ''
user-guide-title: ''
source-git-commit: f72773d86b681ce0e815c5595067b1593cdd1f0a
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 4%

---


# Crash lors du rendu des graphes

Cette page répertorie les crashs survenant pendant le processus de rendu de graphe dans Substance 3D Designer et propose des étapes de dépannage pour chacun d’eux.

## TDR (Windows uniquement)

<b>[![(erreur)](crash-when-rendering-graphs.resources/error.svg)](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) Problème</b>

Le minuteur <b>Détection et récupération du délai d&#39;attente (TDR)</b> du système est *trop court* pour permettre à Substance 3D Designer de terminer ses calculs actuels avant *redémarrage* du pilote graphique.

Les calculs effectués par Substance 3D Designer peuvent être très intensifs et utilisent les pilotes graphiques à un point tel qu&#39;il *ne répond pas* au système d&#39;exploitation pendant un certain temps.\
Par mesure de stabilité et de sécurité, le système d&#39;exploitation *redémarre le pilote graphique*, ce qui raccourcit les calculs et entraîne un *blocage* de Substance 3D Designer.

<b>![(coche)](crash-when-rendering-graphs.resources/check.svg) Étapes recommandées</b>

Les valeurs du minuteur TDR doivent être *augmentées* pour empêcher de tels crashs. Pour ce faire, suivez les instructions fournies dans [cette page](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) de la documentation Substance 3D Painter, qui s&#39;appliquent également à Substance 3D Designer.
