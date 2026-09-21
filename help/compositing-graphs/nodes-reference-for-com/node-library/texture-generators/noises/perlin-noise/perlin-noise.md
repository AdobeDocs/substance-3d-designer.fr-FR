---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/perlin-noise.html"
breadcrumb-title: ""
description: Utilisez le nœud de Bruit Perlin pour générer des motifs de bruit lisses et naturels afin de créer des textures et des variations organiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Perlin noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bruit Perlin
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%
---

# Bruit Perlin

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![bruit Perlin - Icône](perlin-noise.resources/perlin_noise.png "bruit Perlin - Icône"){width="200px"}

<b>Entrée :</b> générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un bruit de Perlin, une distribution lissée des valeurs de niveaux de gris largement utilisée.

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
| <b>Décalage de mosaïque</b> <i>Flottant 2</i> | Définit la position de la partie du plan infini utilisée pour le rendu du bruit. |
| <b>Expansion non carrée</b> <i>Booléen</i> | Dans les images non carrées, la mosaïque générée reste carrée et étend la génération de bruit aux limites de l’image. |

## Exemples

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="perlin-noise.resources/perlin_noise_1.png" class="modal-image" alt="Bruit Perlin - Exemple 1" />
        </td>
        <td style="border: 0;">
            <img src="perlin-noise.resources/noise_perlin_noise_v2_speed0.6_aniso0.gif" class="modal-image" alt="Bruit Perlin - Exemple 2" />
        </td>
        <td style="border: 0;"></td>
    </tr>
</table>
