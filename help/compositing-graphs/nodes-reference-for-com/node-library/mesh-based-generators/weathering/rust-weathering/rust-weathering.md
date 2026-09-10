---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rust-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Altération de Rouille pour générer des motifs de rouille en fonction de la géométrie du maillage afin de créer des effets de corrosion métallique réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rust Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération De La rouille
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 14%

---


# Altération De La rouille

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rust-weathering.resources/rust-weathering.png){width="128px"}

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
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Position</b> <i>Entrée couleur</i> |  |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité. |
| <b>Avancé</b> |  |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Masquer</b> <i>Faux/Vrai</i> | Active ou désactive l&#39;utilisation de la carte de masque. |
| <b>Effet</b> |  |
| <b>Répartition des Rouilles</b> <i>0.0 - 1.0</i> |  |
| <b>Répartition du Smoothness</b> <i>0.0 - 1.0</i> |  |
| <b>Échelle de dégâts de Vernish</b> <i>0.0 - 1.0</i> |  |
| <b>Intensité des gouttes</b> <i>0.0 - 1.0</i> |  |
| <b>Quantité D&#39;Échantillons Goutte</b> <i>0 - 32</i> |  |
| <b>Smoothness gouttes</b> <i>0.0 - 1.0</i> |  |
| <b>Fusion</b> |  |
| <b>Intensité de Diffuse</b> <i>0.0 - 1.0</i> | Force de fusion du Diffuse. |
| <b>Intensité de la Base color</b> <i>0.0 - 1.0</i> | Force de fusion de la Base color. |
| <b>Intensité normale</b> <i>0.0 - 32.0</i> | Force de fusion de la normale. |
| <b>Intensité du Specular</b> <i>0.0 - 1.0</i> | Force de fusion du Specular. |
| <b>Intensité de la Brillance</b> <i>0.0 - 1.0</i> | Force de fusion de la Brillance. |
| <b>Intensité de la Rugosité</b> <i>0.0 - 1.0</i> | Force de fusion de la Rugosité. |
| <b>Intensité Métallique</b> <i>0.0 - 1.0</i> | Force de fusion du Métallique. |
| <b>Intensité de l&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Force de fusion de l’Ambient occlusion. |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> | Intensité de fusion de l&#39;Height. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rust-weathering.resources/rust-ex.gif" />
        </td>
    </tr>
</table>
