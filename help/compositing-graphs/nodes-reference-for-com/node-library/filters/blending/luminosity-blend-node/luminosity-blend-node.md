---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/luminosity-blend-node.html"
breadcrumb-title: ''
description: Utilisez le nœud de fusion Luminosité pour fusionner des textures en fonction des valeurs de luminosité afin de créer des effets composites basés sur la luminosité.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Luminosity (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luminosité (nœud de fusion)
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# Luminosité (nœud de fusion)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<b>Entrée :</b> Filtres > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effectue un mode de fusion Luminosité qui préserve la teinte et la chrominance de l&#39;arrière-plan tout en adoptant la luminance du premier plan.

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
