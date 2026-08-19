---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: Accédez à la bibliothèque de langages de définition de matériau (Material Definition Language) dans Substance 3D Designer pour créer des matériaux personnalisés.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bibliothèque MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Bibliothèque MDL

Cette page présente la bibliothèque de contenu liée aux [graphiques MDL](../../mdl-graphs/mdl-graphs.md) et aux matières incluses dans Substance 3D Designer. Il explique également l&#39;installation et la gestion de contenu personnalisé dans la [bibliothèque](../../interface/the-library/the-library.md).

## Contenu MDL dans la bibliothèque

Les nœuds utilisables dans les graphiques MDL sont disponibles dans la section <b>mdl</b> de la [bibliothèque](../../interface/the-library/the-library.md). Les nœuds sont agencés en filtres selon le module MDL dans lequel ils sont définis.\
Si les modules sont stockés dans des sous-dossiers, cette hiérarchie sera *mise en miroir* dans la bibliothèque en tant que *catégories*.

Cette section inclut du contenu provenant des sources suivantes :

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Contenu intégré

Designer comprend des modules MDL qui contiennent des composantes de base pour la création de graphiques MDL, ainsi que des définitions de matériaux complètes prêtes à être utilisées.

Ce contenu est stocké à cet emplacement sous le répertoire d&#39;installation : `./resources/view3d/iray/`

### Contenu personnalisé

En plus du contenu intégré, vous pouvez ajouter *vos propres modules MDL* à la bibliothèque.

En effet, tout module MDL trouvé sous les répertoires répertoriés dans la section <b>MDL</b> des [paramètres du projet](../../interface/preferences-window/project-settings/project-settings.md) est ajouté à cette section *de manière cumulative* entre les fichiers de projet.

### NVIDIA vMaterials

Si la bibliothèque [vMaterials](https://developer.nvidia.com/vmaterials) de NVIDIA est installée, elle est *automatiquement ajoutée* à la bibliothèque dans sa *propre catégorie*.

</td>
<td style="border: 0;" valign="top">

![Ressources MDL dans la bibliothèque](../../assets/mdl-library.png "Ressources MDL dans la bibliothèque")

La section *« mdl » de la bibliothèque, la bibliothèque vMaterials et le contenu personnalisé sont encadrés*

</td>
</tr>
</table>

## Contenu MDL dans la vue 3D

Tous les modules MDL disponibles dans la bibliothèque peuvent être utilisés dans la [vue 3D](../../interface/3d-view/3d-view.md) lorsque le rendu Iray est utilisé.

Ouvrez le menu <b>Matières</b> et ouvrez un sous-menu *Matière de scène* pour parcourir les modules MDL disponibles. Les listes comprennent :

* Contenu intégré
* Contenu personnalisé
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* [Graphes MDL](../../mdl-graphs/mdl-graphs.md) chargés

![Matériaux MDL dans la vue 3D](../../assets/mdl-apply-in-3dview-material-list.png "Matériaux MDL dans la vue 3D")

*Matières MDL dans la vue 3D*
