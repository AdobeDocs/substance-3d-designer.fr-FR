---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: Apprenez les bases de la création de modules Python pour Substance 3D Designer afin d’étendre les fonctionnalités de l’application.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Principes de base des plug-ins
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Principes de base des plug-ins

Un plug-in est un fichier Python ou un module Python qui définit une fonction <b>initializeSDPlugin()</b>.

La fonction <b>initializeSDPlugin()</b> est appelée lorsque le plug-in est chargé.\
Dans cette fonction, vous pouvez créer des éléments d&#39;interface utilisateur, enregistrer des rappels et tout autre élément de fonctionnalité dont vous pourriez avoir besoin.

Éventuellement, le plug-in peut définir une fonction <b>uninitializeSDPlugin()</b> qui sera appelée lorsque le plug-in sera déchargé.\
Vous pouvez utiliser cette fonction pour libérer des ressources, fermer des connexions réseau et des choses similaires.

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
