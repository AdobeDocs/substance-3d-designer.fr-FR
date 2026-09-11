---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: Utilisez le nœud de Fusion d’Height de Matériau pour fusionner plusieurs matériaux en fonction de maps height de création d’effets de matériau multicalque.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusion Height matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# Fusion Height matériau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-height-blend.resources/material-height-blend.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud est une version plus avancée de la [Fusion d&#39;Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) qui fusionne deux matériaux en fonction de leurs images de hauteur. Il n’existe pas de masque défini par l’utilisateur. Vous devez donc avoir deux cartes de hauteur, une pour chaque matériau, dont au moins une n’est pas une valeur uniforme.

Cela peut être utile pour combiner deux matériaux différents de haute qualité sans un blending mask de haute qualité.

Si vous souhaitez vous fondre dans l&#39;eau ou la neige, les nœuds [Couverture Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) et [Niveau d&#39;eau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) sont disponibles à la place.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/Brillance au lieu de cartes Métallique/Rugosité. |
| <b>Décalage Height</b> <i>0.0 - 1.0</i> | Décale les cartes de hauteur de sorte que le niveau de fusion soit déplacé le long de l’axe height. Il s’agit du contrôle principal de la fusion. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste de la fusion et accentue la netteté des transitions. |
| <b>Mode</b> <i>height équilibré, priorité d&#39;height inférieure</i> |  |
| <b>Opacité</b> <i>0.0 - 1.0</i> | Fusion de l’opacité de l’height de premier plan, avec fondu en entrée ou en sortie. |
| <b>Correspondance Albédo</b> <i>0.0 - 1.0</i> | Quantité de correspondance de couleurs internes à effectuer entre les couleurs Albédos. |
