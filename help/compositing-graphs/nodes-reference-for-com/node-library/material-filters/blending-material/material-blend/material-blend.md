---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion de matériau pour fusionner des matériaux entiers à l'aide de masques pour créer des effets de matériau composite.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion de matériaux
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# Fusion de matériaux

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Fusion de matériaux est l&#39;équivalent de matériau complet multicanal de [le nœud de fusion atomique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Il se mélange entre deux matières complètes (toutes les couches possibles) à partir d’un masque de niveaux de gris, ou éventuellement à partir d’une seule couleur d’un Masque d&#39;identifiant de couleur.

Ce nœud est utile si vous souhaitez fusionner deux matériaux et avoir une texture en niveaux de gris, mais pas d’ID de couleur complet. Si vous avez un biscuit avec ID de couleur et que vous souhaitez fusionner plus de deux matériaux, nous vous suggérons d&#39;utiliser le [mélange de matériaux multiples](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>ColorID</b> <i>Entrée couleur</i> | Mappage d’ID de couleur cuit facultatif. |
| <b>Masque de niveaux de gris</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les couches de matériau dans ce groupe, lors de l’utilisation de cartes de Specular/brillance au lieu de cartes de métal/rugosité, par exemple. |
| <b>Diffus</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Couleur de base</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Normal</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Specular</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Émissif</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Lustre</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Rugosité</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Métallique</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Specular level</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Occlusion ambiante</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Height</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Opacité</b> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> |  |
| <b>Masque d&#39;identifiant de couleur</b> <i>Faux/Vrai</i> | Utilisez le Masque d&#39;identifiant de couleur au lieu du masque en niveaux de gris. Gardez à l’esprit qu’il ne s’agit que d’une seule couleur ! |
| <b>Couleur</b> <i>(valeur de couleur)</i> | Quelle couleur choisir et convertir en blanc. |
| <b>Flou</b> <i>0.01 - 1.0</i> | Degré de fusion de la couleur sélectionnée avec ses voisines. |
| <b>Remplissage</b> <i>0.0 - 1.0</i> | Contraste de transition de la couleur sélectionnée. |
