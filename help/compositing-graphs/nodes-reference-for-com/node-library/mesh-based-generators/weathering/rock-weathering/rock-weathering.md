---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Altération de roche pour générer des motifs d'altération sur les surfaces rocheuses en fonction de la géométrie du maillage pour obtenir des effets d'érosion réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération de roche
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 16%

---


# Altération de roche

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rock-weathering.resources/rock-weathering.png){width="128px"}

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
| <b>Ambient occlusion</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>WS normal</b> <i>Entrée couleur</i> | Espace monde baké Normalmap utilisé pour les effets internes et le masquage. |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité. |
| <b>Avancé</b> |  |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Masquer</b> <i>Faux/Vrai</i> | Active ou désactive l&#39;utilisation de la carte de masque. |
| <b>Effet</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>Sale</b> <i>0.0 - 1.0</i> |  |
| <b>Usure Des Bords</b> <i>0.0 - 1.0</i> |  |
| <b>Roche usagée</b> <i>0.0 - 1.0</i> |  |
| <b>Échelle des Fissures</b> <i>1.0 - 60.0</i> |  |
| <b>Intensité des Fissures</b> <i>0.0 - 1.0</i> |  |
| <b>Âge</b> <i>0.0 - 1.0</i> |  |
| <b>Seuil d&#39;âge</b> <i>0.0 - 1.0</i> |  |
| <b>Échelle Scratches Des Contours Nets</b> <i>1.0 - 32.0</i> |  |
| <b>Intensité de déformation Scratches des contours nets</b> <i>0.0 - 1.0</i> |  |
| <b>Désaturation De La Roche Utilisée</b> <i>0.0 - 1.0</i> |  |
| <b>Luminosité rocheuse utilisée</b> <i>0.0 - 1.0</i> |  |
| <b>Fusion</b> |  |
| <b>Intensité de Diffuse</b> <i>0.0 - 1.0</i> | Intensité de fusion du diffus. |
| <b>Intensité de la Base color</b> <i>0.0 - 1.0</i> | Intensité de fusion de la couleur de base. |
| <b>Intensité normale</b> <i>0.0 - 64.0</i> | Intensité de fusion de la normale. |
| <b>Intensité du Specular</b> <i>0.0 - 1.0</i> | Intensité de fusion du Specular. |
| <b>Intensité de la Brillance</b> <i>0.0 - 1.0</i> | Intensité de fusion du brillant. |
| <b>Intensité de la Rugosité</b> <i>0.0 - 1.0</i> | Force de fusion de la Rugosité. |
| <b>Intensité de l&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Force de fusion de l’Ambient occlusion. |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> | Force de fusion de l’Height. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rock-weathering.resources/rock-ex.gif" />
        </td>
    </tr>
</table>
