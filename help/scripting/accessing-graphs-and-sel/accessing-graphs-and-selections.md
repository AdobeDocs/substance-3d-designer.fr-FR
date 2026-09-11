---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Découvrez comment accéder aux sélections de graphes et de nœuds dans les scripts Substance 3D Designer Python et les manipuler.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Accès aux graphes et aux sélections
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Accès aux graphes et aux sélections

La classe <b>SDApplication</b> contient des méthodes utiles qui vous permettent d&#39;accéder au graphe *actuellement actif* et à la *sélection actuelle* qu&#39;il contient.

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


Un graphe affiché dans une Vue du graphe *spécifique* est accessible à l&#39;aide d&#39;un <b>graphViewID</b>.

Cette méthode est utile lors de la création de barres d’outils de vue du graphe personnalisées. L&#39;exemple <b>Création de barres d&#39;outils dans les Vues du graphe</b> du chapitre [Création d&#39;éléments d&#39;interface utilisateur](../../scripting/creating-user-interface/creating-user-interface-elements.md) fournit plus de détails.
