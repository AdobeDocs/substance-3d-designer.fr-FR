---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: Utilisez le nœud Commuter pour basculer entre deux textures d’entrée en fonction d’un masque pour la sélection conditionnelle de texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Basculer
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# Basculer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/switch-1.png){width="128px"}

![](../../../../../../assets/switch-grayscale.png){width="128px"}

<b>Entrée :</b> Filtres > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Un nœud de commutateur simple à 2 positions. Renvoie l’entrée 1 ou l’entrée 2 en fonction du paramètre Commutateur. Le résultat n’est pas modifié. Voir [Commutateur multiple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) pour une version plus avancée.

Très utile pour exposer un choix booléen (Vrai/Faux) dans un graphe, où vous n’avez besoin que d’un seul bouton et non d’une liste déroulante complexe pour toute une sélection d’options.

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Commutation » pour les entrées Couleur et « Commutation Niveaux de gris » pour les entrées Niveaux de gris.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée 1 (Vrai)</b> <i>Entrée couleur ou niveaux de gris</i> |  |
| <b>Entrée 2 (Faux)</b> <i>Entrée couleur ou niveaux de gris</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Basculer</b> <i>Faux/Vrai</i> | Bascule entre l&#39;entrée 1 (Vrai) et 2 (Faux). |
