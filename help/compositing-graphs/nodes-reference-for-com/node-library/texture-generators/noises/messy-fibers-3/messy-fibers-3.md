---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-3.html"
breadcrumb-title: ''
description: Utilisez le nœud Messy Fibres 3 pour générer des motifs de fibres complexes afin de créer des effets de texture de tissu.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fibres désordonnées 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5a6c28b9acabf15714a1fd8bb4e7593192555fa2
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# Fibres désordonnées 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fibres désordonnées 3 - Icône](messy-fibers-3.resources/messy_fibers_3.png "Fibres désordonnées 3 - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Une variante des bruits structurés <b>fibres désordonnées</b>.

Voir aussi : [Fibres désordonnées 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Fibres désordonnées 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est un bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle</b> <i>Entier</i> | Subdivision de la grille utilisée pour générer les éléments de bruit.    Plus la valeur est élevée, plus le nombre de carreaux dessinés est élevé et plus le bruit est dense. |
| <b>Désordre</b> <i>Flottant</i> | Déplace les ingrédients du bruit.    Cela permet d’animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flottant</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Désorganiser l&#39;anisotropie</b> <i>Flottant</i> | Contrôle l&#39;étendue des directions du displacement appliqué par le paramètre <b>Désordre</b>, où une valeur plus élevée entraîne une direction plus étroite et plus définie.    La direction est contrôlée par le paramètre <b>anisotropy angle de désordre</b>. |
| <b>Désorganiser l&#39;anisotropy angle</b> <i>Flottant</i> | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre « Disorder anisotropie » n&#39;est pas nul. |
| <b>Angle</b> <i>Flottant</i> | Angle utilisé pour définir la direction des filetages, en nombre de tours et à partir de l&#39;horizontale droite. |
| <b>Angle aléatoire</b> <i>Flottant</i> | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Luminance aléatoire</b> <i>Flottant</i> | Plage de luminance soustraite de manière aléatoire des filetages, où 1 représente la plage complète. |
| <b>Décalage de mosaïque</b> <i>Flottant 2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibres désordonnées 3 - Exemple 1](messy-fibers-3.resources/messy_fibers_3_1.png "Fibres désordonnées 3 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibres désordonnées 3 - Exemple 2](messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso0.gif "Fibres désordonnées 3 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibres désordonnées 3 - Exemple 3](messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso1.gif "Fibres désordonnées 3 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibres désordonnées 3 - Exemple 4](messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso0.6.gif "Fibres désordonnées 3 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
