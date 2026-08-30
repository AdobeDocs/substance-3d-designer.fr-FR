---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: Utilisez le nœud de fusion Différence pour fusionner des textures en utilisant le mode de différence pour créer des effets d'inversion et de contraste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Différence
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Différence

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](difference.resources/difference.png){width="128px"}

<b>Entrée :</b> Filtres > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue un mode de fusion Différence entre les entrées Avant et Arrière-plan. Soustrait l’arrière-plan du premier plan, renvoyant un résultat absolu (jamais une valeur négative).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Arrière-plan</b> <i>Entrée couleur</i> |  |
| <b>Premier plan</b> <i>Entrée couleur</i> |  |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan. |
| <b>Simulation de transparence</b> <i>Faux/Vrai</i> | Active/désactive la fusion des couches alpha Premier plan et Arrière-plan. Si cette option est définie sur False, la couche alpha du premier plan est ignorée. |
