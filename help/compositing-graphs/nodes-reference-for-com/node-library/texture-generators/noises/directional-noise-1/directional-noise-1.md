---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit directionnel 1 pour générer des motifs de bruit directionnel afin de créer des variations de texture anisotrope.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BRUIT DIRECTIONNEL 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 1%

---


# BRUIT DIRECTIONNEL 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Bruit directionnel 1 - Icône](directional-noise-1.resources/directional-noise-1-01.png "Bruit directionnel 1 - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Variante des bruits de <b>Bruit directionnel</b>.

Voir aussi : [Bruit directionnel 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Bruit directionnel 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md), [Bruit directionnel 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| <b>Désorganiser l&#39;anisotropy angle</b> <i>Flotter</i> | Contrôle la direction du displacement appliqué par le paramètre <b>Disorder</b>, lorsque le paramètre « Disorder anisotropie » n&#39;est pas nul. |
| <b>Angle</b> <i>Flotter</i> | Angle utilisé pour définir la direction du bruit, en nombre de tours et à partir de l’horizontale vers la droite. |
| <b>Angle aléatoire</b> <i>Flotter</i> | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Décalage de mosaïque</b> <i>Float2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 1](directional-noise-1.resources/directional-noise-1-02.png "Bruit directionnel 1 - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 2](directional-noise-1.resources/directional-noise-1-03.gif "Bruit directionnel 1 - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 3](directional-noise-1.resources/directional-noise-1-04.gif "Bruit directionnel 1 - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Bruit directionnel 1 - Exemple 4](directional-noise-1.resources/directional-noise-1-05.gif "Bruit directionnel 1 - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>
