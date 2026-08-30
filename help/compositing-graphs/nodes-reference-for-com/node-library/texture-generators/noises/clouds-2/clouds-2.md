---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/clouds-2.html"
breadcrumb-title: ''
description: Utilisez le nœud Nuages 2 pour générer des motifs de nuages intermédiaires afin de créer des effets de texture atmosphérique et volumétrique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Clouds 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nuages 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Nuages 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nuages 2 - Icône](clouds-2.resources/clouds_2.png "Nuages 2 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des <b>nuages</b> rugueux bruits.

Voir aussi : [Nuages 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-1/clouds-1.md), [Nuages 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-3/clouds-3.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Niveaux de gris</i> | Le bruit généré est une image bitmap en niveaux de gris. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle</b> <i>Nombre entier</i> | Subdivision de la grille utilisée pour générer les carreaux de bruit.    Plus la valeur est élevée, plus le nombre de carreaux dessinés est important et plus le bruit est dense. |
| <b>Désordre</b> <i>Flotter</i> | Déplace les ingrédients du bruit.    Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> <i>Flotter</i> | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Désorganiser l&#39;anisotropie</b> <i>Flotter</i> | Contrôle l&#39;étendue des directions du displacement appliqué par le paramètre <b>Désordre</b>, où une valeur plus élevée entraîne une direction plus étroite et plus définie.    La direction est contrôlée par le paramètre <b>Désorganiser l&#39;angle d&#39;anisotropie</b>. |
| <b>Désorganiser l&#39;anisotropy angle</b> <i>Flotter</i> | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre <b>Disorder anisotropie</b> n&#39;est pas nul. |
| <b>Décalage de mosaïque</b> <i>Float2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nuages 2 - Exemple 1](clouds-2.resources/clouds_2_1.png "Nuages 2 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Nuages 2 - Exemple 2](clouds-2.resources/noise_clouds_2_v2_speed0.6_aniso0.gif "Nuages 2 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nuages 2 - Exemple 3](clouds-2.resources/noise_clouds_2_v2_speed0.6_aniso1.gif "Nuages 2 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Nuages 2 - Exemple 4](clouds-2.resources/noise_clouds_2_v2_speed0.3_aniso0.6.gif "Nuages 2 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
