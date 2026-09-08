---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise-fractal.html"
breadcrumb-title: ''
description: Utilisez le nœud fractal du Bruit Perlin 3D pour générer des motifs de bruit Perlin fractal dans l’espace 3D afin de créer des textures volumiques détaillées.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: bruit Perlin 3D fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---


# bruit Perlin 3D fractal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal.png){width="200px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud <b>Fractal de Bruit Perlin 3D</b> génère un bruit Perlin <i>fractal</i> dans l&#39;espace 3D en fonction de l&#39;entrée <b>Carte de position</b>.

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
| <b>Échelle</b> <i>Flottant</i> | Contrôle l’échelle du bruit de Perlin 3D fractal. |
| <b>Taille</b> <i>Flottant3</i> | Contrôle la taille du bruit de Perlin 3D fractal dans les axes <b>X</b>, <b>Y</b> et <b>Z</b>. Les valeurs non uniformes entraînent un effet de <i>étiré ou de réduction</i>. |
| <b>Décalage</b> <i>Flottant3</i> | Applique un décalage à la <i>position</i> du bruit de Perlin 3D fractal dans les axes <b>X</b>, <b>Y</b> et <b>Z</b>. |
| <b>Intensité de la Distorsion</b> <i>Flottant</i> | Contrôle l&#39;intensité d&#39;un <i>effet de déformation</i> appliqué sur le bruit de Perlin 3D fractal. |
| <b>Multiplicateur d&#39;échelle de Distorsion</b> <i>Flotter</i> | Contrôle l&#39;échelle du <i>motif de déformation</i> utilisé dans l&#39;effet de déformation contrôlé par l&#39;<b>intensité de la Distorsion</b>. |
| <b>Niveau Min</b> <i>Nombre entier</i> | <i>niveau minimum de répétition</i> utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif <i>plus riche</i> avec une variation sur davantage de plages de fréquences. |
| <b>Niveau Max</b> <i>Nombre entier</i> | <i>niveau de répétition</i> maximum utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif <i>plus riche</i> avec une variation sur davantage de plages de fréquences. |
| <b>Rugosité</b> <i>Flotter</i> | Contrôle l&#39;<i>équilibre</i> entre les <i>niveaux de répétition</i> bas et élevés dans le motif fractal.<br><br><i>Remarque</i> : une valeur de <b>0</b> entraîne une sortie <i>non alignée</i> avec d&#39;autres valeurs faibles qui la suivent. C&#39;est ce qui est attendu. |
| <b>Lacunarité</b> <i>Flotter</i> | Contrôle la façon dont le motif fractal appliqué <i>remplit l&#39;espace</i>. Une valeur <i>plus élevée</i> entraîne <i>moins d&#39;espaces</i> dans le motif et un bruit <i>plus dense</i>. |
| <b>Opacité globale</b> <i>Flotter</i> | Contrôle la <i>plage</i> des valeurs du bruit de Perlin 3D fractal <i>autour</i> de la <b>valeur de base</b>. |
| <b>Ligne de base</b> <i>Flotter</i> | Applique un <i>décalage</i> à la valeur de ligne de base <i>luminance</i> pour la distribution des valeurs de bruit Perlin 3D. |
| <b>Contraste</b> <i>Flottant</i> | Règle le contraste du bruit Perlin 3D. |
| <b>Absolu</b> <i>Booléen</i> | Utilise les valeurs absolues du bruit Perlin 3D. Cela <i>inverse</i> la distribution des valeurs <i>inférieures à 0,5</i>. |
| <b>Activer la Répétition</b> <i>Booléen</i> | Ajuste le bruit Perlin 3D de sorte que son motif résultant <i>se répète</i> dans les axes X, Y et Z. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dfractal.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dperlinnoisefractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dperlinnoisefractal-variant2.jpg" />
        </td>
    </tr>
</table>
