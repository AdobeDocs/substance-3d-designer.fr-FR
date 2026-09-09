---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/linear-burn.html"
breadcrumb-title: ''
description: Utilisez le nœud Linear burn pour fusionner des textures à l’aide du mode de gravure linéaire afin de créer des effets d’obscurcissement et de contraste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Linear Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Densité linéaire +
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---


# Densité linéaire +

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](linear-burn.resources/linear-burn.png){width="128px"}

<b>Entrée :</b> Filtres > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue une fusion Linear burn. La formule mathématique est Premier plan + Arrière-plan - 1.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Premier plan</b> <i>Entrée couleur</i> |  |
| <b>Arrière-plan</b> <i>Entrée couleur</i> |  |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan. |
| <b>Simulation de transparence</b> <i>Faux/Vrai</i> | Active/désactive la fusion des couches alpha Premier plan et Arrière-plan. Si cette option est définie sur False, la couche alpha du premier plan est ignorée. |
