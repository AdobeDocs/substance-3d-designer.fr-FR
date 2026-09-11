---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion de réglage du Matériau pour fusionner les réglages de matériau entre les matériaux afin d’affiner les effets composites.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion de réglage du matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# Fusion de réglage du matériau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-adjustment-blend.resources/material-adjustment-blend.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud permet d’ajuster toutes les couches d’un matériau complet, en fonction d’un masque. Il est conçu pour faciliter et accélérer un workflow de matériau complet.

Cette option est utile lorsque vous souhaitez ajuster quelques couches d’un matériau (comme éclaircir une rugosité diffuse ou l’assombrir) en fonction du même masque.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Masque d&#39;identifiant de couleur</b> <i>Entrée couleur</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Masque de niveaux de gris</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Active et désactive les canaux matériau dans ce groupe, par exemple lors de l&#39;utilisation de cartes de Specular/Brillance au lieu de Métallique/Rugosité.<br><br>Cela active et désactive également l&#39;apparence des groupes pertinents du canal. |
| <b>Diffuse</b> | Effectue des opérations de réglage sur la couche de Diffuse, dans les zones définies par le masque. |
| <b>Base color</b> | Effectue des opérations de réglage sur la couche de Base color, dans les zones définies par le masque. |
| <b>Normal</b> |  |
| <b>Intensité</b> <i>0.0 - 1.0</i> | Atténue l’intensité normale |
| <b>Specular</b> | Effectue des opérations de réglage sur la couche de Specular, dans les zones définies par le masque. |
| <b>Emissive</b> | Effectue des opérations de réglage sur la couche émissive, dans les zones définies par le masque. |
| <b>Brillance</b> | Effectue des opérations de réglage sur la couche de Brillance, dans les zones définies par le masque. |
| <b>Rugosité</b> | Effectue des opérations de réglage sur la couche de Rugosité, dans les zones définies par le masque. |
| <b>Métallique</b> | Effectue des opérations de réglage sur la couche Métallique, dans les zones définies par le masque. |
| <b>Specular level</b> | Effectue des opérations de réglage sur la couche de Specular level, dans les zones définies par le masque. |
| <b>Ambient occlusion</b> | Effectue des opérations de réglage sur la couche Ambient occlusion, dans les zones définies par le masque. |
| <b>Height</b> | Effectue des opérations de réglage sur la couche Height, dans les zones définies par le masque. |
| <b>Opacité</b> | Effectue des opérations de réglage sur la couche d’opacité, dans les zones définies par le masque. |
| <b>Masque d&#39;identifiant de couleur</b> <i>Faux/Vrai</i> | Définissez pour utiliser le Masque d&#39;identifiant de couleur au lieu du masque en niveaux de gris. |
| <b>Flou</b> <i>0.01 - 1.0</i> | Si l’option Masque d&#39;identifiant de couleur est activée, elle détermine l’étendue de la couleur de sélection de l’ID couleur. |
| <b>Couleur</b> <i>(valeur de couleur)</i> | Définit la couleur à utiliser dans le Map id de couleurs et le masque. |
| <b>Remplissage</b> <i>0.0 - 1.0</i> | Détermine le contraste de fusion/les transitions du masquage Color ID. |
