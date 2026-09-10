---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Altération de métal pour ajouter des effets de rouille et de corrosion réalistes aux matériaux métalliques en fonction de la géométrie du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération métallique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 14%

---


# Altération métallique

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-weathering.resources/metal-weathering.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Altération

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>WS normal</b> <i>Entrée couleur</i> | Espace monde baké Normalmap utilisé pour les effets internes et le masquage. |
| <b>Ambient occlusion</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité. |
| <b>Avancé</b> |  |
| <b>Format normal</b> <i>Direct X, ouvrir GL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Masquer</b> <i>Faux/Vrai</i> | Active ou désactive l&#39;utilisation de la carte de masque. |
| <b>Effet</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>Sale</b> <i>0.0 - 1.0</i> |  |
| <b>Usure Des Bords</b> <i>0.0 - 1.0</i> |  |
| <b>Décollement De La Peinture</b> <i>0.0 - 1.0</i> |  |
| <b>Rouille</b> <i>0.0 - 1.0</i> |  |
| <b>Décollement De La Rouille</b> <i>0.0 - 1.0</i> |  |
| <b>Rouille Verdigris</b> <i>Rouille, Verdigris</i> |  |
| <b>Échelle des Fissures de Peinture</b> <i>1.0 - 16.0</i> |  |
| <b>Intensité de déformation des Fissures de Peinture</b> <i>0.0 - 1.0</i> |  |
| <b>Échelle Scratches Des Contours Nets</b> <i>1.0 - 32.0</i> |  |
| <b>Intensité de déformation Scratches des contours nets</b> <i>0.0 - 1.0</i> |  |
| <b>Couleur du métal brut</b> <i>(valeur de couleur)</i> |  |
| <b>Couleur Specular Du Métal Brut</b> <i>(valeur de couleur)</i> |  |
| <b>Valeur De La Brillance Raw Metal</b> <i>(valeur Niveaux de gris)</i> |  |
| <b>Valeur De La Rugosité Raw Metal</b> <i>(valeur Niveaux de gris)</i> |  |
| <b>Fusion</b> |  |
| <b>Intensité de Diffuse</b> <i>0.0 - 1.0</i> | Intensité de fusion du diffus. |
| <b>Intensité de la Base color</b> <i>0.0 - 1.0</i> | Intensité de fusion de la couleur de base. |
| <b>Intensité normale</b> <i>0.0 - 64.0</i> | Force de fusion de la normale. |
| <b>Intensité du Specular</b> <i>0.0 - 1.0</i> | Force de fusion du Specular. |
| <b>Intensité de la Brillance</b> <i>0.0 - 1.0</i> | Force de fusion de la Brillance. |
| <b>Intensité de la Rugosité</b> <i>0.0 - 1.0</i> | Force de fusion de la Rugosité. |
| <b>Intensité Métallique</b> <i>0.0 - 1.0</i> | Force de fusion du Métallique. |
| <b>Intensité de l&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Force de fusion de l’Ambient occlusion. |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> | Force de fusion de l’Height. |
