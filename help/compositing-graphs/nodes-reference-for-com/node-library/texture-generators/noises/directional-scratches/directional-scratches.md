---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: Utilisez le nœud Scratches directionnels pour créer des motifs de rayures directionnels afin d'ajouter des effets d'usure et d'endommagement aux matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rayures directionnelles
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Rayures directionnelles

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rayures directionnelles - Icône](../../../../../../assets/directional_scratches.png "Rayures directionnelles - Icône"){width="200px"}

<b>Entrée :</b> Générateurs de textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Diffusion aléatoire de motifs de rayures avec un angle et une taille réglables.

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
| <b>Angle</b> Flottant | Angle utilisé pour définir la direction des rayures, en nombre de tours et en partant de l’horizontale vers la droite. |
| <b>Angle aléatoire</b> Flottant | Quantité maximale de variation aléatoire appliquée à la valeur <b>Angle</b>, en nombre de tours. |
| <b>Quantité du motif</b> flottante | Multiplicateur de la quantité de motifs de travail diffusés. |
| <b>Taille du motif</b> Float2 | Taille du cadre de sélection du motif de travail.    La valeur Y contrôle la longueur maximale des rayures. |
| <b>Taille aléatoire du motif</b> Float2 | Multiplicateur de la réduction aléatoire d’échelle appliquée aux rayures.    La valeur Y l’applique à la longueur des rayures. |
| <b>Décalage de mosaïque</b> Float2 | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> booléenne | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 1](../../../../../../assets/directional_scratches_1.png "Égratignures directionnelles - Exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 2](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.gif "Égratignures directionnelles - Exemple 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 3](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.6.gif "Égratignures directionnelles - Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 4](../../../../../../assets/noise-directional-scrat-1.gif "Égratignures directionnelles - Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Égratignures directionnelles - Exemple 5](../../../../../../assets/noise-directional-scrat-2.gif "Égratignures directionnelles - Exemple 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



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
