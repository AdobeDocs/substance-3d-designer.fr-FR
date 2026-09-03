---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Utilisez le nœud Commutateur multiple pour basculer entre plusieurs textures d'entrée en fonction d'un sélecteur pour la sélection conditionnelle de texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Commutateur multiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Commutateur multiple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-switch.resources/multi-switch-01.png){width="128px"}

![](multi-switch.resources/multi-switch-02.png){width="128px"}

<b>Entrée :</b> Filtres > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Agit comme une boîte de commutation, ne passant que par l&#39;entrée définie par le paramètre &#39;Sélection d&#39;entrée&#39;. Ainsi, si deux entrées sont connectées, une seule d&#39;entre elles sera retournée (non modifiée), selon le choix de l&#39;utilisateur.

Très utile pour ajouter de nombreuses options différentes dans un graphe. Associé à [exposer](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) (de préférence sous forme de liste déroulante), un grand nombre de personnalisations est possible.

Important : assurez-vous d’utiliser la version appropriée pour vos commentaires. Utilisez « Multi-commutateur » pour les entrées Couleur, « Multi-commutateur Niveaux de gris » pour les entrées Niveaux de gris.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée 1-20</b> <i>Entrée couleur</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Numéro d&#39;entrée</b> <i>2 - 20</i> | Quantité d’entrées à exposer. Important : ne supprime pas les connexions lorsque le nombre est réduit ! |
| <b>Sélection d&#39;entrée</b> <i>1 - 20</i> | Entrée à renvoyer comme résultat. |
