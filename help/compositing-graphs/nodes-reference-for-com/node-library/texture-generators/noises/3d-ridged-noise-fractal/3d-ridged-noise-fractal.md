---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
breadcrumb-title: ''
description: Utilisez le nœud fractal de Bruit strié 3D pour générer des motifs de bruit fractal strié dans l’espace 3D afin de créer des textures de type montagne.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Ridged Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: bruit 3D à arête fractale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# bruit 3D à arête fractale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-ridged-noise-fractal.resources/3dridgednoisefractal.png){width="200px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud Fractal de Bruit strié <b>3D</b> génère un bruit strié <i>fractal</i> dans l&#39;espace 3D en fonction de l&#39;entrée de <b>carte de position</b>.

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
| <b>Échelle</b> <i>Flotter</i> | Contrôle l’échelle du bruit fractal 3D avec arête. |
| <b>Taille</b> <i>Float3</i> | Contrôle la taille du bruit fractal 3D avec arête dans les axes <b>X</b>, <b>Y</b> et <b>Z</b>. Les valeurs non uniformes entraînent un effet d&#39;<i>étirement ou de compression</i>. |
| <b>Décalage</b> <i>Float3</i> | Applique un décalage à la <i>position</i> du bruit fractal à arête 3D dans les axes <b>X</b>, <b>Y</b> et <b>Z</b>. |
| <b>Intensité de la Distorsion</b> <i>Flotter</i> | Contrôle l&#39;intensité d&#39;un <i>effet de déformation</i> appliqué sur le bruit fractal à arête 3D. |
| <b>Multiplicateur d&#39;échelle de Distorsion</b> <i>Flotter</i> | Contrôle l&#39;échelle du <i>motif de déformation</i> utilisé dans l&#39;effet de déformation contrôlé par l&#39;<b>intensité de la Distorsion</b>. |
| <b>Niveau Min</b> <i>Nombre entier</i> | <i>niveau minimum de répétition</i> utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif <i>plus riche</i> avec une variation sur davantage de plages de fréquences. |
| <b>Niveau Max</b> <i>Nombre entier</i> | <i>niveau de répétition</i> maximum utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif <i>plus riche</i> avec une variation sur davantage de plages de fréquences. |
| <b>Rugosité</b> <i>Flotter</i> | Contrôle l&#39;<i>équilibre</i> entre les <i>niveaux de répétition</i> bas et élevés dans le motif fractal.<br><br><i>Remarque</i> : une valeur de <b>0</b> entraîne une sortie <i>non alignée</i> avec d&#39;autres valeurs faibles qui la suivent. C&#39;est ce qui est attendu. |
| <b>Lacunarité</b> <i>Flotter</i> | Contrôle la façon dont le motif fractal appliqué <i>remplit l&#39;espace</i>. Une valeur <i>plus élevée</i> entraîne <i>moins d&#39;espaces</i> dans le motif et un bruit <i>plus dense</i>. |
| <b>Opacité globale</b> <i>Flotter</i> | Contrôle la <i>plage</i> des valeurs de bruit fractal 3D avec arête <i>autour</i> de la <b>valeur de base</b>. |
| <b>Ligne de base</b> <i>Flotter</i> | Applique un <i>décalage</i> à la valeur de base de <i>luminance</i> pour la distribution de la valeur de bruit 3D Ridged. |
| <b>Contraste</b> <i>Flotter</i> | Règle le contraste du bruit 3D avec arête. |
| <b>Activer la Répétition</b> <i>Booléen</i> | Règle le bruit 3D avec arête de sorte que le motif résultant <i>se répète</i> sur les axes X, Y et Z. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3dridgednoisefractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3dridgednoisefractal-variant2.jpg" />
        </td>
    </tr>
</table>
