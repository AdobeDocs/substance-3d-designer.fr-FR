---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/dirt-4.html"
breadcrumb-title: ''
description: Utilisez le nœud Dirt 4 pour générer des motifs de dirt intermédiaires afin de créer des détails de surface altérés et des effets d’accumulation.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Dirt 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: DIRT 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---


# DIRT 4

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Dirt 4 - Icône](../../../../../../assets/dirt_4.png "Dirt 4 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits granuleux du <b>Dirt</b>.

Voir aussi : [Dirt 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-1/dirt-1.md), [Dirt 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-2/dirt-2.md), [Dirt 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-3/dirt-3.md), [Dirt 5](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-5/dirt-5.md), [Dégradé de Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-gradient/dirt-gradient.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Sorties

</td>
<td style="border: 0;" valign="top">

### Paramètres

</td>
<td style="border: 0;" valign="top">

### Exemples

</td>
</tr>
</table>

## Sorties

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris* | Le bruit généré est une image bitmap en niveaux de gris. |

## Paramètres

|  |  |
| --- | --- |
| Entier <b>Échelle</b> | Subdivision de la grille utilisée pour générer les carreaux de bruit.    Plus la valeur est élevée, plus le nombre de carreaux dessinés est important et plus le bruit est dense. |
| <b>Désordre</b> Flottant | Déplace les ingrédients du bruit.    Cela peut être utilisé pour animer le bruit. |
| <b>Désorganiser la vitesse</b> Flotter | Ajuste la distance de displacement appliquée par le paramètre <b>Désordre</b>.    Cela permet de contrôler la vitesse du displacement lors de l’animation du bruit. |
| <b>Désordre anisotropie</b> Flottant | Contrôle l&#39;étendue des directions du displacement appliqué par le paramètre <b>Désordre</b>, où une valeur plus élevée entraîne une direction plus étroite et plus définie.    La direction est contrôlée par le paramètre <b>Désorganiser l&#39;angle d&#39;anisotropie</b>. |
| <b>Modification de l&#39;angle d&#39;anisotropie</b> Flottant | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre <b>Disorder anisotropie</b> n&#39;est pas nul. |
| <b>Décalage de mosaïque</b> Float2 | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> booléenne | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 4 - Exemple 1](../../../../../../assets/dirt_4_1.png "Dirt 4 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 4 - Exemple 2](../../../../../../assets/noise_dirt_4_v2_speed0.6_aniso0.gif "Dirt 4 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 4 - Exemple 3](../../../../../../assets/noise_dirt_4_v2_speed0.6_aniso1.gif "Dirt 4 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 4 - Exemple 4](../../../../../../assets/noise_dirt_4_v2_speed0.3_aniso0.6.gif "Dirt 4 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
