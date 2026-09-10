---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Utilisez le nœud Bruit Worley 3D pour générer un bruit Worley en fonction de la position 3D afin de créer des effets de texture volumique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: bruit 3D Worley
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 7%

---


# bruit 3D Worley

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-worley-noise.resources/3d-worley.png){width="128px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s’agit de l’un des bruits les plus polyvalents et avancés de la bibliothèque. Il génère un bruit Worley dans l’espace 3D, à partir d’un mappage de position d’entrée. Propose de nombreuses options qui la rendent beaucoup plus puissante que les bruits standard basés sur les [Cellules](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)ou la [distance](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Échelle</b> <i>1 - 64</i> | Définissez l’échelle globale de l’effet. |
| <b>Taille</b> <i>0.0 - 1.0</i> | Effectuez une mise à l’échelle non uniforme sur les axes X, Y et Z séparément. |
| <b>Mode</b> <i>Euclidean, Manhattan, Chebyshev, Minkowski</i> | Modifiez la mesure de distance. Permet d’utiliser des types de bruits très différents. |
| <b>Nombre de Minkowski</b> <i>0.0 - 20.0</i> | Seulement avec la mesure de distance de Minkowski. Fusions entre différents types de mesures. |
| <b>Style</b> <i>F1, F2, F2-F1, Bordure, Couleur aléatoire</i> | Définissez les valeurs mathématiques de la combinaison Métrique. Permet de nombreuses autres combinaisons. |
| <b>Largeur de la bordure</b> <i>0.0 - 1.0</i> | Lorsque la combinaison de bordures mathématiques est active, contrôle la largeur de la bordure. |
| <b>Arrondi</b> <i>0.0 - 1.0</i> | Disponible uniquement avec les modes F1, F2 et F2-F1. Définit la position médiane du niveau. |
| <b>Inverser</b> <i>Faux/Vrai</i> | Inverse le résultat. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex04.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex01.png" />
        </td>
    </tr>
</table>
