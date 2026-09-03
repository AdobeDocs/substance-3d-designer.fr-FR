---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Utilisez l’nœud Height Extrude pour extruder des formes basées sur des cartes d’height afin de créer des effets de profondeur de type 3D dans des textures.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height Extrude
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# Height Extrude

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-extrude.resources/height-extrude-01.png){width="200px"}

<b>Entrée :</b> Générateurs de textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Height Extrude restitue la Profondeur Z 3D à partir d’une carte d’Height d’entrée. Tout comme l&#39;[extrusion de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) et le [cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), elle vous permet de faire tourner une caméra dans la vue 2D. Son objectif principal est de servir de générateur pour créer des formes pivotées en 3D à partir d’une carte de hauteur plate. Ces formes peuvent ensuite être utilisées avec l&#39;[éclaboussure de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md).

La principale différence avec l&#39;[extrusion de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) est que la carte d&#39;entrée ne doit pas nécessairement être une carte de type « alpha » binaire, mais une carte en niveaux de gris à plage complète. Cela signifie que vous avez plus de contrôle sur l’height d’extrusion (formes organiques complexes), mais aucun contrôle sur les profils de biseautage (surfaces dures, formes plus simples).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Angle De Caméra</b> | Angles d’Euler de la caméra, en demi-tours. Veuillez noter que la rotation horizontale et l&#39;échelle sont appliquées directement à l&#39;entrée. |
| <b>Échelle De Caméra</b> <i>0.001 - 3.0</i> | Échelle globale appliquée à la sortie. |
| <b>Échelle d&#39;Height</b> <i>0.0 - 2.0</i> | Applique un facteur global aux valeurs d&#39;height d&#39;entrée. |
| <b>Décalage vertical</b> <i>-1.0 - 1.0</i> | Déplace la sortie finale vers le haut ou vers le bas. |
| <b>Sol</b> <i>Désactivé/Activé</i> | Si l’option Masse est désactivée, un arrière-plan noir s’affiche, dans lequel l’entrée est définie sur 0 plutôt qu’un plan semblable à la masse. |
| <b>Format normal</b> <i>DirectX/OpenGL</i> | Le paramètre <b>Format normal</b> inverse la coordonnée y de la carte normale. |
| <b>Intensité normale</b> <i>0.0 - 256.0</i> | Identique au paramètre <b>Intensité</b> du nœud <b>Normal</b>. Réglez-le sur 256 pour obtenir une normale sans cisaillement lors de la rotation. |
