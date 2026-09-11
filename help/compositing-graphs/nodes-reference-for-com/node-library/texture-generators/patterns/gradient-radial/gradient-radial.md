---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: Utilisez le nœud Dégradé radial pour créer des dégradés radiaux rayonnant à partir d’un point central pour des transitions de couleur circulaires.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dégradé radial
user-guide-description: ''
user-guide-title: ''
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# Dégradé radial

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Similaire à [Circulaire de dégradé](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md), cette option crée une transition de dégradé en niveaux de gris définie par deux points personnalisés de manière radiale. La transition va de a à b, définie par le centre et le rayon. Gardez à l’esprit que les résultats ne seront pas toujours affichés en mosaïque.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Forme</b> <i>Cône, Hémisphère</i> | Détermine le profil de transition. Le cône est une transition nette et linéaire, l’hémisphère est doux et arrondi au centre. |
| <b>Point 1</b> | Point central du dégradé. Commence en blanc. |
| <b>Point 2</b> | Point du rayon pour déterminer l’étendue du dégradé. Se termine en noir. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Activer la compensation de la courbure et du étire avec des rapports non carrés. |
