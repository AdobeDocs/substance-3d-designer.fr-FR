---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Découvrez les étapes de dépannage pour les problèmes techniques liés aux textures de cuisson dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problèmes de boulangerie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Problèmes de boulangerie

Cette page répertorie les problèmes techniques liés aux [textures de cuisson](../../bakers/bakers.md) dans Substance 3D Designer et propose des étapes de dépannage pour chacun d&#39;eux.

## Dans cette page

« Correspondance par nom » ne fonctionne pas

## « Correspondance par nom » ne fonctionne pas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b> ![(error)](../../assets/error.svg) Problème</b>

Lorsque l’option Correspondance est définie sur Par nom de maillage, la correspondance ne semble pas être appliquée ou n’est pas homogène sur tous les objets de la scène.

<b> ![(tick)](../../assets/check.svg) Étapes recommandées</b>

Dans les versions 14.1 et antérieures de Designer, les objets à faible et à fort poly étaient mis en correspondance à l&#39;aide du nom de leurs *objets parents*, c&#39;est-à-dire, dans la plupart des cas, leur transformation parente.

Depuis Designer 15.0, le nom des objets *géométrie* est utilisé directement.

</td>
<td style="border: 0;" valign="top">

![Objet Geometry et son parent dans l&#39;arbre de la scène](../../assets/sceneTree_objectsName.png "Objet Geometry et son parent dans l&#39;arbre de la scène"){zoomable="yes"}

</td>
</tr>
</table>

Il existe deux chemins que vous pouvez emprunter pour obtenir la correspondance attendue :

* Ajustez le nom des objets géométriques pour appliquer des noms correspondants.
* Revenez au comportement ou aux versions précédentes de Designer, en ajustant l&#39;option [&#39;Mode de filtrage des noms&#39;](../../interface/preferences-window/project-settings/project-settings.md) dans les paramètres du projet :
  1. Accédez à Modifier > Préférences > Projets
  1. Sélectionnez le dernier fichier de projet dans la liste
  1. Sous la liste des fichiers de projet, sélectionnez l’onglet Bakers
  1. Définissez le « Mode de filtrage des noms » sur « Nom du parent (hérité) ».
