---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Fissures Weathering pour ajouter des motifs de fissures aux matériaux en fonction de la courbure du maillage et des points de contrainte.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fissures Weathering
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Fissures Weathering

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cracks-weathering.resources/cracks-weathering.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Altération

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s’agit d’un effet matériel qui fonctionne sur plusieurs canaux à la fois. Il ajoute un motif de fissure aléatoire, avec un contrôle sur l’étendue et la profondeur.

Assurez-vous de bien comprendre les [modes de création de liens](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) lorsque vous travaillez avec des matériaux complets.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> | Mappage cuit ou généré utilisé pour les effets internes et le masquage. |
| <b>Height</b> <i>Entrée en niveaux de gris</i> | Mappage cuit ou généré utilisé pour les effets internes et le masquage. |
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
| <b>Propagation des Fissures</b> <i>0.0 - 1.0</i> | La distance sur laquelle les fissures doivent s’étendre. Il s’agit de la commande principale de cet effet. |
| <b>Profondeur Fissures</b> <i>0.0 - 1.0</i> | Profondeur de l’effet de fissure. Cela affecte principalement l’height et affecte légèrement le thickness visuel. |
| <b>Fusion</b> | Contrôle la force de fusion de l’effet dans chaque couche obtenue. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cracks-weathering.resources/cracks-ex.gif" />
        </td>
    </tr>
</table>
