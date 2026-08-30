---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: Utilisez le nœud de Bruit Perlin 3D pour générer des motifs de bruit Perlin lisses dans l’espace 3D afin de créer des textures volumiques naturelles.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: bruit Perlin 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# bruit Perlin 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise.resources/3dperlinnoise.png){width="200px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud <b>Bruit Perlin 3D</b> génère un bruit Perlin dans l&#39;espace 3D en fonction de l&#39;entrée <b>Carte de position</b>.

Ce nœud peut être testé avec [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) en entrée au lieu d&#39;une map bakée réelle (comme illustré dans l&#39;exemple ci-dessous).

</td>
</tr>
</table>

>[!WARNING]
>
> Ce bruit est destiné à être utilisé avec le <i>moteur GPU uniquement</i> (c&#39;est-à-dire <b>Direct3D</b> ou <b>OpenGL</b>). Accédez à <b>Outils > Changer de moteur...</b> ou appuyez sur la touche <b>F9</b> pour sélectionner le moteur souhaité.

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Inverser</b> <i>Booléen</i> | Inverse l’image de sortie. |
| <b>Échelle</b> <i>Flotter</i> | Contrôle l’échelle du bruit Perlin 3D. |
| <b>Taille</b> <i>Float3</i> | Contrôle la taille du bruit Perlin 3D dans les axes <b>X</b>, <b>Y</b> et <b>Z</b>. Les valeurs non uniformes entraînent un effet d&#39;<i>étirement ou de compression</i>. |
| <b>Décalage</b> <i>Float3</i> | Applique un décalage à la <i>position</i> du bruit Perlin 3D dans les axes <b>X</b>, <b>Y</b> et <b>Z</b>. |
| <b>Intensité de la Distorsion</b> <i>Flotter</i> | Contrôle l&#39;intensité d&#39;un <i>effet de déformation</i> appliqué sur le bruit Perlin 3D. |
| <b>Multiplicateur d&#39;échelle de Distorsion</b> <i>Flotter</i> | Contrôle l&#39;échelle du <i>motif de déformation</i> utilisé dans l&#39;effet de déformation contrôlé par l&#39;<b>intensité de la Distorsion</b>. |
| <b>Ligne de base</b> <i>Flotter</i> | Applique un <i>décalage</i> à la valeur de ligne de base <i>luminance</i> pour la distribution des valeurs de bruit Perlin 3D. |
| <b>Contraste</b> <i>Flotter</i> | Règle le contraste du bruit Perlin 3D. |
| <b>Absolu</b> <i>Booléen</i> | Utilise les valeurs absolues du bruit Perlin 3D. Cela <i>inverse</i> la distribution des valeurs <i>inférieures à 0,5</i>. |
| <b>Activer la Répétition</b> <i>Booléen</i> | Ajuste le bruit Perlin 3D de sorte que son motif résultant <i>se répète</i> dans les axes X, Y et Z. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlin.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant.jpg" />
        </td>
    </tr>
</table>
