---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Utilisez le nœud Couverture Snow pour ajouter des effets d'accumulation de neige aux matériaux en fonction de l'angle de la surface et de la position.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couverture de Snow
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---


# Couverture de Snow

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](snow-cover.resources/snow-cover.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Effet tout-en-un pour ajouter de la neige sur un matériau complet. Repose fortement sur une bonne carte de hauteur de haute qualité, comme celle d’un photoscan. Le résultat est censé être correct pour le PBR.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité. |
| <b>Nouveau Snow</b> <i>0.0 - 1.0</i> | Définit la quantité de neige dans les zones surélevées. Le résultat est lié au paramètre Snow fondu. |
| <b>Snow fondu</b> <i>0.0 - 1.0</i> | Définit la quantité de neige fondue dans les coins les plus bas. |
| <b>Cumul</b> <i>0.0 - 1.0</i> | Affecte principalement la sortie d’Height, détermine l’effet d’empilement d’heights. |
| <b>Smoothness</b> <i>0.0 - 1.0</i> | Permet de lisser les détails de l’height en fonction de l’accumulation de neige. |
| <b>Intensité des flocons</b> <i>0.0 - 1.0</i> | Affecte principalement Normalmap, intensité des détails du flocon. |
