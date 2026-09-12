---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: Découvrez comment importer et utiliser des ressources Scène 3D dans Substance 3D Designer pour l’aperçu et les tests par matériau.
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ressource de scène 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: fde9d7a455c1c7b366323c119f4c1f9a2c114952
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---


# Ressource de scène 3D

Cette page décrit le type de ressource **Scène 3D** dans Substance 3D Designer, notamment ses formats de fichiers pris en charge et la manière dont il peut être utilisé.

## Vue d’ensemble

Les ressources scène 3D peuvent être utilisées dans divers workflows :

* [maps de maillage de baking](../../bakers/bakers.md)
* prévisualisez les *textures* de [graphes de Substance](../../compositing-graphs/substance-compositing-graphs.md) dans la [vue 3D](../../interface/3d-view/3d-view.md)

Les formats de fichier Scène 3D suivants sont pris en charge :

* [USD](https://graphics.pixar.com/usd/release/index.html) (\*.usd)
* [USDA](https://graphics.pixar.com/usd/release/index.html) (\*.usda)
* [USDZ](https://graphics.pixar.com/usd/release/index.html) (\*.usdz)
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview) (\*.fbx)
* [Wavefront OBJ](https://www.fileformat.info/format/wavefrontobj/egff.htm) (\*.obj)
* [Autodesk 3D Studio Maillage](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html) (\*.3ds)
* [Collada](https://www.khronos.org/collada/) (\*.dae)
* [Dessin Autodesk AutoCAD](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) (\*.dxf)

## stockage par maillage

Les scènes 3D ne peuvent *être liées* que, ce qui signifie qu’elles restent à leur emplacement sur le disque et sont simplement référencées dans l’application.

Lorsqu&#39;un package avec une ressource Scène 3D est publié en tant qu&#39;actif [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) (SBSAR), le maillage *n&#39;est pas incorporé*, mais supprimé.

## maps de maillage de Baking

Lier une Scène 3D à votre package est le seul moyen de [baker des maps de maillage](../../bakers/bakers.md) à partir de cette géométrie de scène. Pour commencer, vous pouvez effectuer les étapes suivantes :

* Cliquez sur *RMB* sur un pack et sélectionnez l&#39;option <b>Lien > maillage 3D</b> dans le menu contextuel
* Choisir un fichier Scène 3D pris en charge
* Si l&#39;invite de dialogue <b>Lier en tant que maillage Udim</b> s&#39;affiche, cliquez sur *Non*, sauf si vous souhaitez baker les UV
* Une fois la ressource chargée dans l&#39;[Explorateur](../../interface/the-explorer-window/the-explorer-window.md), cliquez sur *RMB* et sélectionnez l&#39;<b>option Informations sur le modèle de Baking</b> dans le menu contextuel
* La boîte de dialogue [Informations sur le modèle Baker](../../bakers/bakers.md) s&#39;affiche pour vous permettre de configurer et d&#39;exécuter des bakes de maps de maillage

![maps de maillage de Baking](3d-scene-resource.resources/bake-model-information.gif "maps de maillage de Baking"){width="512px"}

## Utilisation des vignettes UDIM/UV

Lorsqu’une ressource de maillage est liée et que l’application détecte qu’elle contient des UV en dehors de la plage 0-1, un message vous demande si ce maillage doit être traité comme un maillage UDIM (également appelé Tuiles UV). Il s&#39;agit d&#39;un paramètre qui peut être modifié par la suite. À moins que vous ne soyez sûr d&#39;utiliser UV-Tiles, la réponse doit être <b>Non</b>.

Si le comportement UV-Tile est actif, le baking se comporte différemment et bakera des textures pour chaque UV-Tile détecté.

## Ressource/Scène par rapport à l’état

L’application sépare ce que vous voyez dans la vue 3D en deux fichiers distincts. Le maillage 3D réel est une ressource visible dans l’Explorateur. La configuration des lumières, des caméras et d&#39;autres paramètres est appelée « <b>État</b> ». Les états peuvent être enregistrés dans des fichiers .sbsscn externes, pour y être chargés à nouveau ultérieurement. Les fichiers .sbsscn ne sont pas des ressources, il s&#39;agit de fichiers de configuration supplémentaires qui ne peuvent être chargés que via [le menu Scène dans vue 3D.](../../interface/3d-view/3d-view.md)
