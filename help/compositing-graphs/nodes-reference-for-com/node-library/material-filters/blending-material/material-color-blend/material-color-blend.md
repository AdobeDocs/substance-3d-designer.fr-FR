---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion de couleur de Matériau pour fusionner des couches de couleur entre des matériaux afin de créer des effets de matériau composites.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion de couleur de matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# Fusion de couleur de matériau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Fusion

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud permet d’effectuer des réglages dans un Matériau multicanal en mélangeant des couleurs unies par-dessus. C&#39;est la principale différence avec la [Fusion de réglage de Matériau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), qui n&#39;autorise que les réglages de type [Niveaux](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) des couches, tandis que ce nœud utilise des réglages de type [Fusion](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) avec une couleur unie.

Ce nœud est particulièrement utile lorsque vous souhaitez introduire un indice de couleur plat dans la Diffuse ou la Base color, ou que vous voulez « aplatir » d’autres couches à l’aide d’une valeur de couleur unie définie.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>ColorID</b> <i>Entrée couleur</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Masque de niveaux de gris</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité, par exemple. |
| <b>Diffuse</b> |  |
| <b>Couleur</b> <i>(valeur de couleur)</i> | Valeur de couleur à fusionner au-dessus de la couche Diffuse. |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Opacité de fusion entre le premier plan et l’arrière-plan. |
| <b>Mode de fusion</b> <i>Normal, Ajouter, Subtract, Multiplier, Ajouter/Sub, Max, Min, Commuter</i> | Mode de fusion à utiliser dans l’opération. |
| <b>Base color</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Normal</b> |  |
| <b>Source</b> <i>Height, Masque</i> |  |
| <b>Mode de fusion</b> <i>Combiner, Fusion</i> |  |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> |  |
| <b>Opacité de l&#39;Height</b> <i>0.0 - 1.0</i> |  |
| <b>Format</b> <i>DirectX, OpenGL</i> |  |
| <b>Specular</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Émissif</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Lustre</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Rugosité</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Métallique</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Specular level</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Occlusion ambiante</b> | Fusionne une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Height</b> | Fusion une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Opacité</b> | Fusion une couleur unie au-dessus de cette couche avec des options comme dans le groupe Diffuse. |
| <b>Masque d&#39;identifiant de couleur</b> <i>Faux/Vrai</i> | Utilisez le Masque d&#39;identifiant de couleur au lieu du masque en niveaux de gris. Gardez à l&#39;esprit qu&#39;il ne s&#39;agit que d&#39;une seule couleur !<br><br>Active toutes les options ci-dessous. |
| <b>Couleur</b> <i>(valeur de couleur)</i> | Quelle couleur choisir et convertir en blanc. |
| <b>Flou</b> <i>0.01 - 1.0</i> | Degré de fusion de la couleur sélectionnée avec ses voisines. |
| <b>Remplissage</b> <i>0.0 - 1.0</i> | Contraste de transition de la couleur sélectionnée. |
