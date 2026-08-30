---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud altération de la mousse pour ajouter des motifs de croissance de mousse aux matériaux en fonction de la courbure et de la position du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération De La Mousse
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 7%

---


# Altération De La Mousse

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](moss-weathering.resources/moss-weathering.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Altération

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s’agit d’un effet matériel qui fonctionne sur plusieurs canaux à la fois. Il génère un effet de mousse sur-développée, avec un seul contrôle pour la propagation.

Cet effet fonctionne mieux avec une carte de position de l&#39;espace universel et une carte de hauteur supplémentaire. Bien que ce ne soit pas une exigence exacte, cela confère à l&#39;effet un placement plus crédible.

Assurez-vous de bien comprendre les [modes de création de liens](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) lorsque vous travaillez avec des matériaux complets.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Position</b> <i>Entrée couleur</i> | Baking World Space Position. |
| <b>Height</b> <i>Entrée en niveaux de gris</i> | Entrée Heightmap supplémentaire. |
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
| <b>Propagation de la mousse</b> <i>0.0 - 1.0</i> | Définit la propagation de la mousse. Pousse par étapes, d&#39;une couverture légère à une mousse épaisse, épaisse et foncée. |
| <b>Fusion</b> |  |
| <b>Intensité de Diffuse</b> <i>0.0 - 1.0</i> | Intensité de fusion du diffus. |
| <b>Intensité de la Base color</b> <i>0.0 - 1.0</i> | Intensité de fusion de la couleur de base. |
| <b>Intensité normale</b> <i>0.0 - 1.0</i> | Intensité de fusion de la normale. |
| <b>Intensité du Specular</b> <i>0.0 - 1.0</i> | Intensité de fusion du Specular. |
| <b>Intensité de la Brillance</b> <i>0.0 - 1.0</i> | Intensité de fusion du brillant. |
| <b>Intensité de la Rugosité</b> <i>0.0 - 1.0</i> | Intensité de fusion de la rugosité. |
| <b>Intensité de l&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Intensité de fusion de l&#39;Occlusion ambiante. |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> | Intensité de fusion de l&#39;Height. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="moss-weathering.resources/moss-ex.gif" />
        </td>
    </tr>
</table>
