---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Utilisez le nœud Éclaboussure pour dispersion des formes entre les textures afin de créer des motifs aléatoires et des détails de texture organique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---


# Éclaboussure

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter.resources/splatter-01.png)

![](splatter.resources/splatter-02.png)

<b>Entrée :</b> Générateurs de textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Splatter est un générateur de motif destiné au placement aléatoire d&#39;une entrée de carte. Il dispose de nombreuses commandes pour le placement à motifs géométriques et est plus simple d&#39;utilisation que le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Cette dernière solution peut donner des résultats similaires, mais elle est beaucoup plus complexe.

Splatter fonctionne bien pour tamponner rapidement certaines formes, sans avoir besoin de trop de retouches.

Gardez à l’esprit que les paramètres par défaut Éclaboussure ne semblent pas du tout aléatoires : vous devez en régler quelques-uns pour obtenir une randomisation (principalement les paramètres Trouble). Gardez également à l’esprit que Splatter nécessite une entrée de mappage pour fonctionner.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Largeur de la taille du motif</b> <i>0.0 - 1000.0</i> | Nombre de motifs à utiliser sur l&#39;axe X. |
| <b>Height de la taille du motif</b> <i>0.0 - 1000.0</i> | Nombre de motifs à utiliser sur l’axe Y. |
| <b>Rotation</b> <i>-360.0 - 360.0</i> | Fait pivoter chaque motif selon une valeur définie. |
| <b>Variation de rotation</b> <i>0.0 - 360.0</i> | Introduit une rotation aléatoire pour chaque forme distincte. |
| <b>Zoom</b> <i>100.0 - 10000.0</i> | Augmente l’échelle du résultat final. Gardez à l’esprit que cela casse la répétition ! |
| <b>Gain</b> <i>0.0 - 10.0</i> | Ajuste le gain de fusion de chaque motif. Les fait ressortir davantage. |
| <b>Panoramique X</b> <i>-100.0 - 100.0</i> | Résultat de l’ensemble des panoramas à l’axe X. |
| <b>Panoramique Y</b> <i>-100.0 - 100.0</i> | Résultat de l’ensemble du panoramique sur l’axe Y. |
| <b>Désordre</b> <i>0.0 - 100.0</i> | Décale les formes de manière aléatoire. |
| <b>Numéro De Grille</b> <i>0 - 8</i> | Permet de parcourir différentes tailles de grille pour ajuster l’échelle des résultats. Conserve la répétition. |
| <b>Angle de désordre</b> <i>0.0 - 360.0</i> | Contrôle le déplacement de l’angle de la perturbation. |
| <b>Désordre aléatoire</b> <i>Faux/Vrai</i> | Aléatoire l&#39;angle du trouble, ajoutant beaucoup plus de chaos. |
| <b>Taille du motif</b> <i>5 - 12</i> |  |
| <b>Variation de taille</b> <i>0.0 - 100.0</i> | Introduit une mise à l’échelle aléatoire pour chaque forme. |
| <b>Filtrage d’entrée d’image (Moteur > v4 uniquement)</b> <i>Bilinéaire + Mipmaps, Bilinéaire, Nearest</i> | Quel filtrage appliquer à l’image d&#39;entrée ? |
| <b>Niveau De Sortie Min</b> <i>0.0 - 1.0</i> | Ajustement du niveau minimum de sortie. |
| <b>Niveau De Sortie Max</b> <i>0.0 - 1.0</i> | Ajustement du niveau maximal. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur Niveaux de gris)</i> | Définit la couleur d’arrière-plan unie. |
| <b>Variation de Luminance</b> <i>0.0 - 1.0 (version en niveaux de gris uniquement)</i> | Introduit la variation de luminance. |
| <b>Variation de couleur</b> <i>0.0 - 1.0 (Version En Couleur Uniquement)</i> | Introduit la variation de couleur. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter.resources/splatter-03.gif" />
        </td>
    </tr>
</table>
