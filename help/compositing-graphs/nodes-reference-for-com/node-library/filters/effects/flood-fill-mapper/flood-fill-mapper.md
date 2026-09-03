---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Utilisez le nœud Mappeur de Flood Fill pour mapper les valeurs sur les régions connectées à l’aide d’algorithmes de remplissage par diffusion pour le traitement de la texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappeur de mots de Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# Mappeur de mots de Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-mapper.resources/flood-fill-mapper-01.png)![](flood-fill-mapper.resources/flood-fill-mapper-02.png)

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le mappeur de Flood Fill permet de remapper un motif ou une texture existants sur chaque cellule à partir d&#39;un [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Elle se distingue des autres conversions Flood Fill comme les [niveaux de gris aléatoires](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) ou les [dégradés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) en ce sens qu&#39;elle ne génère pas de couleurs ou de valeurs unies, mais vous permet d&#39;utiliser vos propres cartes d&#39;entrée. Il peut être considéré comme une sorte de combinaison de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) et de [Mosaïque Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) ou de [Mappeur de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md), car il fournit un certain nombre de contrôles et d&#39;interfaces similaires.

La version Couleur dispose de commandes supplémentaires pour travailler avec les cartes de normales, où elle peut [compenser les rotations des cartes de normales de l&#39;espace tangent](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Boîte de Flood Fill</b> <i>Entrée couleur</i> | Saisie Flood Fill standard, obligatoire. |
| <b>Entrée de motif 1-8</b> <i>Entrée Niveaux de gris/Couleur</i> | Entrée d’image de motif personnalisée. |
| <b>Carte de distribution de motif</b> <i>Entrée en niveaux de gris</i> | Map id pour déterminer quel motif va à quelle cellule. Peut provenir d’un autre mappage de Flood Fill, tel que Flood Fill vers index. |
| <b>Mappage d&#39;échelle</b> <i>Entrée en niveaux de gris</i> | Mappage pour déterminer l’échelle par cellule. |
| <b>Map rotation</b> <i>Entrée en niveaux de gris</i> | Faire correspondre pour déterminer la rotation par cellule. |
| <b>Mappage de décalage de Luminance</b> <i>Entrée en niveaux de gris</i> | Mapper pour définir la Luminance par cellule |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode mosaïque</b> <i>Pas De Répétition, H+V</i> | Indiquez si vous souhaitez utiliser la Répétition ou non. Visible uniquement si la taille ou l’échelle est inférieure à 1. |
| <b>Motif</b> |  |
| <b>Numéro d&#39;entrée de motif</b> <i>1 - 8</i> | Définissez la quantité d’entrées de motif personnalisé à utiliser. |
| <b>Mode de distribution des motifs</b> <i>Aléatoire, Taille De Forme, Entrée De Mappage De Distribution</i> | Définir la méthode pour déterminer quel motif est affiché dans une cellule. |
| <b>Variation de la distribution des motifs</b> <i>0.0 - 1.0</i> | Permet une légère variation ou un décalage de la distribution Motif sans tout modifier par le biais de l’option Générateur aléatoire. |
| <b>Taille</b> |  |
| <b>Mode Taille</b> <i>Par rapport à la Texture, par rapport à la forme BSphere, par rapport à la plus grande forme, par rapport à la plus petite forme, ajuster la forme BBox</i> | Définit la façon dont la taille du motif dans chaque cellule est déterminée. |
| <b>Taille</b> <i>0.0 - 1.0</i> | Permet une mise à l’échelle non uniforme du motif. |
| <b>Échelle</b> <i>0.0 - 1.0</i> | Définissez l’échelle globale (uniforme) de l’effet. |
| <b>Multiplicateur de mappage d&#39;échelle</b> <i>0.0 - 1.0</i> | Définissez l’influence de la carte d’échelle facultative. |
| <b>Échelle aléatoire</b> <i>-1.0 - 1.0</i> | Définissez la quantité de variation aléatoire dans l’échelle du motif. |
| <b>Rotation</b> |  |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Définissez une rotation globale et uniforme pour chaque cellule. |
| <b>Multiplicateur de Maps rotation</b> <i>0.0 - 1.0</i> | Définissez l’influence de la Map rotation facultative. |
| <b>Rotation aléatoire</b> <i>0.0 - 1.0</i> | Définissez le degré de rotation aléatoire de chaque cellule. |
| <b>Mise À L&#39;Échelle Automatique De Rotation</b> <i>Faux/Vrai</i> | Définit si un motif doit ajuster son échelle pour s’adapter à l’intérieur d’une cellule lors de la rotation. |
| <b>Position</b> |  |
| <b>Décalage de position</b> <i>0.0 - 1.0</i> | Définissez le décalage de position global pour chaque cellule. |
| <b>Alignement du décalage de position</b> <i>Texture, motif</i> | Définissez cette option pour aligner le point de décalage 0 sur la cellule Motif ou sur la texture. |
| <b>Décalage de position aléatoire</b> <i>0.0 - 1.0</i> | Définissez le degré de randomisation du décalage de position par cellule. |
| <b>Couleur (uniquement pour la version en niveaux de gris)</b> |  |
| <b>Plage de Luminances</b> <i>0.0 - 1.0</i> | Définit le contraste global sur la texture, où 0 devient gris moyen. |
| <b>Plage De Luminances Aléatoire</b> <i>0.0 - 1.0</i> | Définit le degré de randomisation pour la plage de Luminances. |
| <b>Décalage de Luminance</b> <i>-1.0 - 1.0</i> | Définit le décalage de la Luminance, en tant que contrôle de la luminosité. |
| <b>Décalage de Luminance aléatoire</b> <i>0.0 - 1.0</i> | Définit le degré de sélection aléatoire du décalage de Luminance. |
| <b>Multiplicateur de mappage de décalage de Luminance</b> <i>0.0 - 1.0</i> | Définit l’influence de la courbe de décalage de Luminance facultative. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur Niveaux de gris)</i> | Définit la couleur d’arrière-plan sur laquelle les textures sont fusionnées. |
| <b>Couleur (uniquement pour la version Color)</b> |  |
| <b>La Map normal</b> <i>Faux/Vrai</i> | Définit pour interpréter l’entrée de motif comme une Map normal. Permet de compenser et de corriger la rotation de l’espace tangente normale. |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Basculer entre différents Formats de map normaux (inverse la couche verte). Actif uniquement lorsque l’option Est mappage normal a la valeur True. |
| <b>Réglage TSL</b> <i>-1.0 - 1.0</i> | Ajustez la TSL globalement. |
| <b>TSL aléatoire</b> <i>-1.0 - 1.0</i> | Définissez la randomisation TSL par cellule. |
| <b>Réglage de l&#39;Alpha</b> <i>-1.0 - 1.0</i> | Définissez le réglage global de l&#39;Alpha, réduit le contraste de l&#39;Alpha. |
| <b>Alpha aléatoire</b> <i>-1.0 - 1.0</i> | Définissez le paramétrage aléatoire des réglages d&#39;Alpha par cellule. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Définit la couleur d’arrière-plan sur laquelle les textures sont fusionnées. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/flood-fill-mapper-04.jpg" />
        </td>
    </tr>
</table>
