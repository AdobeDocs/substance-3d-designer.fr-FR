---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: Utilisez le nœud Masque de volume 3D pour créer des masques volumiques basés sur la position 3D pour des effets de matériau avancés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Masque de volume 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# Masque de volume 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-volume-mask.resources/3d-volume-mask-01.png){width="256px"}

<b>Entrée :</b> Générateur > Motif

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud **Masque de volume 3D** génère une représentation d&#39;une *forme primitive* basée sur le mappage d&#39;entrée **Position**.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Position</b> <i>Couleur</i> | La carte décrivant les *coordonnées de l&#39;espace 3D* dans laquelle la primitive est représentée.<br><br>Les coordonnées **X/Y/Z** sont mappées aux canaux **R/G/B** respectivement. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Forme</b> <i>Nombre entier</i> | La forme primitive qui doit être représentée :<br><br>- *Cube*<br>- *Cylindre*<br>- *Sphère* |
| <b>Échelle</b> <i>Flotter</i> | Définit l&#39;échelle *globale* de la primitive, appliquée *uniformément* sur tous les axes. |
| <b>Taille</b> <i>Float3</i> | Définit la taille de la forme sur chaque axe. |
| <b>Entrée de position</b> <i>Nombre entier</i> | Méthode de *représentation de l&#39;espace* via l&#39;entrée **Position** :<br><br>- *UV* : utilisez un *UV map*. Les coordonnées X/Y (U/V) sont respectivement mappées aux canaux R/G. L&#39;axe Z est supposé être le vecteur *avant orthogonal*.<br>-*Position de l&#39;Espace monde* : utilisez une *carte de position* pour mapper la primitive dans l&#39;espace 3D. Les coordonnées X/Y/Z sont respectivement mappées sur les canaux R/G/B. |
| <b>UV de position</b> <i>Float2</i> | Position de la primitive dans l&#39;espace UV.<br><br>*Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Entrée de position** est défini sur *UV*. |
| <b>Position</b> <i>Float3</i> | Position de la primitive dans l&#39;espace monde.<br><br>*Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Entrée de position** est défini sur *Position de l&#39;Espace monde*. |
| <b>Rotation</b> <i>Float3</i> | Définit la rotation de la forme dans l’espace univers. |
| <b>Largeur du contour progressif</b> <i>Flotter</i> | Ajuste la largeur du *dégradé de fondu* de la surface de la primitive vers l&#39;intérieur. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3d-volume-mask-05.jpg" />
        </td>
    </tr>
</table>
