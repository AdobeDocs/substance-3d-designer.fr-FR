---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: Découvrez comment transférer les plug-ins des versions précédentes de Substance Designer vers l’API Python active.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Portage des plug-ins précédents
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Portage des plug-ins précédents

En raison des modifications apportées à la prise en charge de Qt pour Python, **les plug-ins précédents ne fonctionneront plus**.\
En particulier, veuillez noter ce qui suit :

## Chargement et déchargement du plug-in

Les plug-ins sont désormais chargés au <b>démarrage</b> de l&#39;application et déchargés à la <b>fermeture</b>.\
Par conséquent, il n&#39;est *pas nécessaire* que les plug-ins héritent de &#39;*sdplugins.Plugin*&#39;.

Pour plus d&#39;informations, consultez la section [Principes de base des plug-ins](../../scripting/plugin-basics/plugin-basics.md).

## Création d’éléments d’interface utilisateur

Les plug-ins *n&#39;ont plus besoin* de définir un &#39;*sdplugins.PluginDesc*&#39;.\
À la place, les plug-ins peuvent utiliser le <b>nouvel objet [gestionnaire d’interface utilisateur](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)</b> et <b>Qt pour Python</b> pour créer les éléments d’interface utilisateur dont ils ont besoin.

Vous trouverez de petits exemples de code dans la section [Création d&#39;éléments d&#39;interface utilisateur](../../scripting/creating-user-interface/creating-user-interface-elements.md).

## Remplacement des utilisations du contexte d’emplacement

La classe &#39;*SDLocationContext*&#39; a été *supprimée* de l&#39;API Python.\
Les plug-ins peuvent utiliser l&#39;objet <b>[UI manager](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)</b> pour accéder au graphique et à la sélection actuellement actifs.

Vous trouverez quelques exemples dans la section [Accès aux graphiques et aux sélections](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md).
