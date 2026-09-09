---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Découvrez l’interface héritée pour les bakers Substance 3D Designer pour les utilisateurs familiarisés avec les anciennes versions.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interface héritée Baker
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 4%

---


# Interface héritée Baker

Voici la description de l&#39;interface de baker disponible dans les versions de [Adobe Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) antérieures à la version 6.0.4.

## Vue d’ensemble

![](bakers-legacy-interface.resources/image2017-3-13-9-33-40.png)

Le panneau baker est divisé en 4 parties :

### 1 : SCÈNE

![](bakers-legacy-interface.resources/image2017-3-13-9-35-53.png)

Vous pouvez définir la partie du maillage impliquée dans le processus de baking.

Nouveauté de la version 6 : vous pouvez également sélectionner par matériau :

![](bakers-legacy-interface.resources/image2017-3-13-9-45-26.png)

### 2 : BAKERS

![](bakers-legacy-interface.resources/image2017-3-13-9-46-26.png)

En appuyant sur le bouton ![](bakers-legacy-interface.resources/image2017-3-13-9-47-47.png), vous pouvez ajouter les bakers souhaités à la liste de traitement

>[!NOTE]
>
> Les boulangeries sont traitées en suivant l&#39;ordre des listes (de haut en bas) : cela peut être important si vous voulez réutiliser le résultat d&#39;un baking (comme la map normal) dans un autre processus de baking

En cliquant sur le signe « + » dans la disposition des bakers, vous pouvez ajouter les bakers dans une pile (vous pouvez placer autant de bakers que vous le souhaitez dans une pile).

.![](bakers-legacy-interface.resources/image2017-3-13-9-52-8.png)

Vous pouvez supprimer un processus de baking de la liste en appuyant sur ![](bakers-legacy-interface.resources/image2017-3-13-9-54-33.png)

Vous pouvez réorganiser la liste des processus de baking en sélectionnant un processus de baking et en utilisant ![](bakers-legacy-interface.resources/image2017-3-13-9-55-33.png)

### 3 : paramètres des Bakers

![](bakers-legacy-interface.resources/image2017-3-13-13-24-0.png)

Cette section affiche les options spécifiques au baker actuellement sélectionné.

### 4 : Paramètres Communs

![](bakers-legacy-interface.resources/image2017-3-13-13-28-12.png)

Affiche les paramètres partagés entre les bakers.

>[!NOTE]
>
> Par défaut, la modification de l&#39;un de ces paramètres affecte tous les bakers, sauf si vous cochez la case Remplacer les paramètres, communs à tous les bakers : dans ce cas, les modifications sont locales au baker actif.

* **Le champ Nom de la ressource** vous permet de modifier le nom du bitmap généré, si vous le souhaitez.
* **La liste déroulante Format de fichier** vous permet de modifier le format de fichier par défaut (format bitmap Windows ou OS/2, « BMP »).
* **La case à cocher** **Placer** la ressource dans un dossier spécifique au maillage vous permet de choisir si l&#39;image bitmap générée est stockée au même niveau que le modèle ou à l&#39;intérieur d&#39;un nouveau sous-dossier nommé « Ressources ».
* **La méthode** vous permet de définir si la nouvelle ressource bitmap doit être liée ou incorporée dans le package de Substance.
* **Le dossier** vous permet de définir où enregistrer les mappages.

Appuyez sur le bouton OK en bas à droite de la fenêtre des bakers pour lancer le processus de baking.

Nouveauté de la version 6 : vous pouvez désormais annuler le processus de baking à l’aide du bouton d’annulation :

![](bakers-legacy-interface.resources/image2017-3-13-13-50-4.png)
