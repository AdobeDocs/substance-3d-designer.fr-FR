---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Utilisez le Noeud de filtrage Saison pour appliquer des effets de saison aux matériaux afin de créer des variations printanières, estivales, automnales et hivernales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtre de saison
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# Filtre de saison

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/default-icon.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud ajoute des effets tels qu’un niveau d’eau animé, de la neige, de la glace et/ou de la mousse.

Gardez à l’esprit qu’il s’agit d’un filtre plus ancien qui n’est pas destiné à être entièrement PBR-correct. Il est généralement conservé pour des raisons liées à l’héritage/à la compatibilité, même s’il peut être utile dans certains cas. Des versions correctes PBR plus récentes se trouvent dans [Couverture de Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) et [Niveau d&#39;eau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

Le nœud nécessite un ensemble approprié d&#39;entrées de matériau, principalement avec une carte de hauteur ou une carte de normales récemment détaillée.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité. |
| <b>Avancé</b> |  |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Masquer</b> <i>Faux/Vrai</i> | Active ou désactive l&#39;utilisation de la carte de masque. |
| <b>Intensité de la lumière</b> <i>0.0 - 1.0</i> | Intensité de la lumière (simulée). |
| <b>Angle de la lumière</b> <i>0.0 - 1.0</i> | Angle d’incidence de la lumière (simulée) |
| <b>Effet</b> |  |
| <b>Effet de l&#39;Height ou de la normale</b> <i>Height, Normal</i> | Choisit la map d&#39;entrée qui pilote les effets. |
| <b>Niveau d&#39;eau</b> <i>0.0 - 1.0</i> | Augmente ou diminue le niveau d&#39;eau en fonction des informations d&#39;Height/Normal. |
| <b>Détails de l&#39;eau</b> <i>0.0 - 1.0</i> | Définit la quantité de détails dans l’eau. |
| <b>Réfraction</b> <i>0.0 - 1.0</i> | Définit la quantité de fausse réfraction dans l’effet. |
| <b>Réflexion</b> <i>0.0 - 1.0</i> | Définit la quantité de faux reflet dans l’effet. |
| <b>Distance de réflexion</b> <i>0.0 - 1.0</i> | Contrôle les visuels de réflexion. |
| <b>Angle De Réflexion</b> <i>0.0 - 1.0</i> | Contrôle les visuels de réflexion. |
| <b>Direction du flux</b> <i>0.0 - 1.0</i> | Contrôle le flux de l’animation (utiliser la Substance Player pour la visualisation). |
| <b>Glace</b> <i>0.0 - 1.0</i> | Définit le degré de gel de l’eau. |
| <b>Détails De La Glace</b> <i>0.0 - 1.0</i> | Définit la quantité de détails dans la glace. |
| <b>Snow</b> <i>0.0 - 1.0</i> | Définit la quantité de neige couverte. |
| <b>Mousse</b> <i>0.0 - 1.0</i> | Définit la quantité de couverture de mousse. |
| <b>Échelle de mousse</b> <i>1 - 4</i> | Définit l’échelle de la texture de mousse générée. |
| <b>Couleur de la mousse</b> <i>(valeur de couleur)</i> | Définit la couleur de la mousse. |
| <b>Aquarelle</b> <i>(valeur de couleur)</i> | Définit la couleur de l’eau, y compris l’alpha/opacité. |
| <b>Fusion</b> |  |
| <b>Intensité de Diffuse</b> <i>0.0 - 1.0</i> | Force de fusion du Diffuse. |
| <b>Intensité de la Base color</b> <i>0.0 - 1.0</i> | Force de fusion de la Base color. |
| <b>Intensité normale</b> <i>0.0 - 1.0</i> | Force de fusion de la normale. |
| <b>Intensité du Specular</b> <i>0.0 - 1.0</i> | Force de fusion du Specular. |
| <b>Intensité de la Brillance</b> <i>0.0 - 1.0</i> | Force de fusion de la Brillance. |
| <b>Intensité de la Rugosité</b> <i>0.0 - 1.0</i> | Force de fusion de la Rugosité. |
| <b>Intensité de l&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Force de fusion de l’Ambient occlusion. |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> | Force de fusion de l’Height. |
