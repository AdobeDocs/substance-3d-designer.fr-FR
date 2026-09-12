---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/warnings-from-dependencies.html"
breadcrumb-title: ''
description: Découvrez les avertissements liés aux dépendances de ressources dans Substance 3D Designer et comment les résoudre.
helpx_creative_field: ""
helpx_description: Designer > Resources > Warnings from dependencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avertissements des dépendances
user-guide-description: ''
user-guide-title: ''
source-git-commit: f0ba7fcd041b7c683b77de11d923d71bec338d08
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---


# Avertissements des dépendances

Cette page répertorie les avertissements et les messages d’erreur qui peuvent être déclenchés par des dépendances dans Substance 3D Designer et propose des étapes de dépannage courantes pour chacun d’eux.

Les dépendances sont *d&#39;autres fichiers* référencés par un fichier Substance 3D (SBS). Ils incluent [ressources](../../resources/resources.md) et d&#39;autres fichiers Substance 3D référencés par des nœuds [instance de graphe](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).

## ![(erreur)](warnings-from-dependencies.resources/error.svg) Pack dépendant non valide

Impossible de charger un package de dépendance, car il est manquant, corrompu ou incompatible avec la version de Designer utilisée.

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

Il existe deux façons principales de corriger ce problème :

1. <b>Chargement de la dépendance réussi</b>

   Vérifiez que le package de dépendance existe à l&#39;emplacement spécifié dans le message d&#39;avertissement. Si ce n’est pas le cas, recherchez le fichier et replacez-le à cet emplacement, ou recréez-le sur place. Si le fichier existe, *essayez de le charger* dans Designer et recherchez les avertissements ou les erreurs liés à ce package. Reportez-vous à la section Étapes de dépannage pour ces problèmes spécifiques et corrigez-les en conséquence.

   Ensuite, rechargez le package hôte en cliquant sur le RMB dessus dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md) et en sélectionnant l&#39;option <b>Recharger</b> dans le menu contextuel.

   ![&#39;Solution de package dépendant non valide&#39; 1](warnings-from-dependencies.resources/warnings-dep-invalid-dependent-pkg.gif "&#39;Solution de package dépendant non valide&#39; 1")
1. <b>Redéfinir l&#39;emplacement la dépendance dans le package</b>

   Vous pouvez redéfinir l&#39;emplacement la dépendance à l&#39;aide du [Gestionnaire de dépendances](../../interface/dependency-manager/dependency-manager.md). Cliquez sur RMB sur le package hôte dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md) et sélectionnez l&#39;option <b>Gestionnaire de dépendances</b> dans le menu contextuel.

   Recherchez la dépendance manquante dans la liste du gestionnaire de dépendances, cliquez sur RMB dessus et sélectionnez l&#39;option <b>Redéfinir l&#39;emplacement...</b>. Recherchez le package de dépendances à l&#39;aide de la boîte de dialogue du navigateur de fichiers et cliquez sur <b>Ouvrir</b>.

   Ensuite, rechargez le package hôte en cliquant sur le RMB dessus dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md) et en sélectionnant l&#39;option <b>Recharger</b> dans le menu contextuel.

   ![&#39;Solution de package dépendant non valide&#39; 2](warnings-from-dependencies.resources/warnings-dep-invalid-dependent-pkg-2.gif "&#39;Solution de package dépendant non valide&#39; 2")

## ![(erreur)](warnings-from-dependencies.resources/error.svg) Vérifiez que l&#39;alias *&#39;X&#39;* est défini dans votre projet

L&#39;une des dépendances ou ressources du package est chargée à partir d&#39;un emplacement qui est [alias](../../interface/preferences-window/project-settings/project-settings.md) dans les données du fichier Substance 3D (SBS) sous l&#39;alias indiqué dans l&#39;avertissement, bien que cet alias ne soit pas défini dans les [fichiers de projet](../../interface/preferences-window/project-settings/project-settings.md) actuels.

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

Au moins l&#39;un des [fichiers de projet](../../interface/preferences-window/project-settings/project-settings.md) doit définir l&#39;alias indiqué dans l&#39;avertissement.

![&#39;Vérifier l&#39;alias est défini&#39; solution](warnings-from-dependencies.resources/warnings-dep-alias.gif "&#39;Vérifier l&#39;alias est défini&#39; solution")

## ![(erreur)](warnings-from-dependencies.resources/error.svg) Impossible de trouver un fichier correspondant à cette ressource

Les fichiers correspondant au *modèle UDIM* pour une [ressource Bitmap](../../resources/bitmap-resource/bitmap-resource.md) sont introuvables.

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

Lorsqu&#39;une ressource [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) est liée et que Designer détecte une *taxonomie de dénomination d&#39;UDIM* dans son nom de fichier, par exemple `0x1` dans `my_texture_0x1.png`, il propose de la lier en tant que *modèle d&#39;UDIM*, de sorte que les nœuds [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) puissent *basculer automatiquement* vers d&#39;autres bitmaps dans un ensemble d&#39;UDIM à l&#39;aide de cette taxonomie, lors de l&#39;utilisation d&#39;un workflow UDIM dans Designer. Dans ce cas, Designer lie la ressource Bitmap d&#39;une *manière différente* qui tient compte du modèle de numérotation UDIM.

Il existe deux façons principales de corriger ce problème :

1. <b>Restaurer les fichiers</b>

   Accédez à l&#39;emplacement spécifié par l&#39;attribut <b>Chemin d&#39;accès</b> de la ressource et vérifiez que les fichiers suivant le modèle existent. Si ce n’est pas le cas, restaurez-les ou recréez-les.

   ![&#39;Aucun fichier correspondant à la ressource&#39; solution 1](warnings-from-dependencies.resources/warnings-dep-udim-2.gif "&#39;Aucun fichier correspondant à la ressource&#39; solution 1")
1. <b>Redéfinir l&#39;emplacement les fichiers</b>

   Si les fichiers ont été déplacés ou renommés, redéfinissez l&#39;emplacement-les en cliquant sur le RMB de l&#39;élément de ressource dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md) et sélectionnez l&#39;option <b>Redéfinir l&#39;emplacement</b> pour lier cette ressource au *premier fichier d&#39;un ensemble* d&#39;images UDIM du même type.

   ![&#39;Aucun fichier correspondant à la ressource&#39; solution 2](warnings-from-dependencies.resources/warnings-dep-udim.gif "&#39;Aucun fichier correspondant à la ressource&#39; solution 2")

## ![(erreur)](warnings-from-dependencies.resources/error.svg) fichier lié introuvable

Le fichier référencé par une ressource liée n&#39;existe pas à l&#39;emplacement spécifié par son attribut <b>Chemin d&#39;accès</b>.

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

Il existe deux façons principales de corriger ce problème :

1. <b>Restaurer le fichier</b>

   Accédez à l&#39;emplacement spécifié par l&#39;attribut <b>Chemin d&#39;accès</b> de la ressource et vérifiez que le fichier existe. Si ce n’est pas le cas, restaurez-le ou recréez-le.

   ![&#39;Fichier lié introuvable&#39; solution 1](warnings-from-dependencies.resources/warnings-dep-file-not-found.gif "&#39;Fichier lié introuvable&#39; solution 1")
1. <b>Redéfinir l&#39;emplacement le fichier</b>

   Si le fichier a été déplacé ou renommé, redéfinissez l&#39;emplacement-le en cliquant sur le RMB de l&#39;élément de ressource dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md) et sélectionnez l&#39;option <b>Redéfinir l&#39;emplacement</b> pour lier cette ressource à un autre fichier du même type.

   ![&#39;Fichier lié introuvable&#39; solution 2](warnings-from-dependencies.resources/warnings-dep-file-not-found-2.gif "&#39;Fichier lié introuvable&#39; solution 2")

## ![(erreur)](warnings-from-dependencies.resources/error.svg) espace colorimétrique introuvable

Une ressource [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) référence un espace colorimétrique introuvable dans l&#39;[environnement de gestion des couleurs](../../color-management/color-management.md) actuel. Il peut s’agir d’un profil ICC ou d’un espace colorimétrique dans une configuration OCIO.

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

La liste des options de l’attribut d’espace colorimétrique est automatiquement renseignée avec l’espace colorimétrique valide disponible. Remplacez la valeur d’espace colorimétrique de cette ressource par toute autre entrée de la liste.

Vous pouvez également ajouter cet espace colorimétrique à l&#39;environnement actuel de [gestion des couleurs](../../color-management/color-management.md), puis redémarrer Designer. Il peut s’agir d’un profil ICC ou d’un espace colorimétrique dans une configuration OCIO.

>[!NOTE]
>
> Cet avertissement est déclenché uniquement lors de l&#39;utilisation d&#39;un mode de gestion des couleurs autre que **Hérité** (qui s&#39;apparente à la désactivation de la gestion des couleurs). Vous pouvez activer la gestion des couleurs dans la section **Gestion des couleurs** des [paramètres du projet](../../interface/preferences-window/project-settings/project-settings.md).

![&#39;Espace colorimétrique introuvable&#39; solution](warnings-from-dependencies.resources/warnings-dep-color-space.gif "&#39;Espace colorimétrique introuvable&#39; solution")

## Ressource de référence ![(erreur)](warnings-from-dependencies.resources/error.svg) introuvable

Le graphe attribué à l&#39;UV d&#39;une [ressource Scène 3D](../3d-scene-resource/3d-scene-resource.md) est introuvable à l&#39;emplacement indiqué dans l&#39;avertissement.

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

Il existe deux façons principales de corriger ce problème :

1. <b>Restaurer le graphe</b>

   Vérifiez le contenu du package dans le panneau [Explorateur](../../interface/the-explorer-window/the-explorer-window.md) pour le graphe spécifié dans la liste <b>Tuiles UV</b>. S’il n’existe pas, restaurez-le ou recréez-le.

   ![&#39;Ressource de référence introuvable&#39; solution 1](warnings-from-dependencies.resources/warnings-dep-udim-graph-2.gif "&#39;Ressource de référence introuvable&#39; solution 1")
1. <b>Sélectionner un autre graphe</b>

   Attribuez un autre graphe du package à l’UV.

   ![&#39;Ressource de référence introuvable&#39; solution 1](warnings-from-dependencies.resources/warnings-dep-udim-graph.gif "&#39;Ressource de référence introuvable&#39; solution 2")

## ![(erreur)](warnings-from-dependencies.resources/error.svg) UV sont attribués plusieurs fois

Un UV pour une [ressource Scène 3D](../3d-scene-resource/3d-scene-resource.md) est affecté plusieurs fois à un [graphe Substance](../../compositing-graphs/substance-compositing-graphs.md).

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

Pour chaque Ensemble d&#39;UV d&#39;une ressource Maillage 3D, assurez-vous qu&#39;aucun index UDIM n&#39;est présent *plusieurs fois* dans la liste <b>Tuiles UV</b>.

![&#39;UV tiles sont affectés plusieurs fois&#39; solution](warnings-from-dependencies.resources/warnings-dep-udim-same.gif "&#39;UV tiles sont affectés plusieurs fois&#39; solution")

## ![(erreur)](warnings-from-dependencies.resources/error.svg) UV non valides

Un UV répertorié pour une [ressource Scène 3D](../3d-scene-resource/3d-scene-resource.md) n&#39;est pas défini dans le maillage ou est endommagé.

<b> ![(tick)](warnings-from-dependencies.resources/check.svg) Solution</b>

Pour chaque Ensemble d&#39;UV d&#39;une ressource Maillage 3D, assurez-vous que tous les éléments de la liste <b>Tuiles UV</b> font référence à des UDIM qui *existent* dans la ressource liée.

>[!NOTE]
>
> Cet avertissement ne peut pas être déclenché via l&#39;interface utilisateur, car il *répertorie uniquement* les UDIM détectés dans la ressource liée. Seule la modification directe des données dans le fichier Substance 3D (SBS) *directement* peut déclencher cet avertissement.

![&#39;Solution d&#39;UV non valide&#39;](warnings-from-dependencies.resources/warnings-dep-udim-invalid.gif "&#39;Solution d&#39;UV non valide&#39;")
