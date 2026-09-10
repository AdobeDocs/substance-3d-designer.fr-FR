---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud Fusion Height pour fusionner des textures en fonction de cartes d'height afin de créer des transitions de matériau réalistes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé de formes Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Dégradé de formes Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-blend.resources/height-blend.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Combine deux cartes de hauteur en fonction de leurs informations d&#39;height. Génère une carte de hauteur fusionnée, mais également un masque noir et blanc qui peut être utilisé ailleurs.

Cela est utile lorsque vous avez deux cartes de hauteur de haute qualité à combiner, mais pas nécessairement un matériau complet, comme c&#39;est le cas pour le [mélange d&#39;Height de matériau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Height en haut</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Height bas</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Décalage Height</b> <i>0.0 - 1.0</i> | Décale les cartes de hauteur de sorte que le niveau de fusion soit déplacé le long de l’axe height. Il s’agit du contrôle principal de la fusion. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste de la fusion et accentue la netteté des transitions. |
| <b>Mode</b> <i>height équilibré, priorité d&#39;height inférieure</i> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Fusion de l’opacité de l’height de premier plan, avec fondu en entrée ou en sortie. |
