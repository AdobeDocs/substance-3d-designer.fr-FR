---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: Découvrez comment implémenter les fonctionnalités d’annulation et de rétablissement dans les scripts Substance 3D Designer Python pour les actions utilisateur.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Annuler et rétablir
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# Annuler et rétablir

Avec la classe <b>SDHistoryUtils.UndoGroup</b>, les utilisateurs peuvent *regrouper des actions* afin de *les annuler ou les rétablir* en une seule commande.

Ces groupes sont *nommés* par les utilisateurs et apparaîtront sous ce nom dans la liste Annuler/Rétablir de l&#39;interface utilisateur.  Cela facilite la gestion d’un grand nombre d’actions.

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
