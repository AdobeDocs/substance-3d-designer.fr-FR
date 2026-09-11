---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Utilisez le nœud Flood Fill vers dégradé pour remplir les régions avec des valeurs de dégradé afin de créer des transitions de couleur lisses.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill au dégradé
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# Flood Fill au dégradé

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-gradient.resources/floodfill-to-gradient.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Transforme une base [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) en dégradés (orientés de manière aléatoire). Très utile pour créer une carte de hauteur où les carreaux sont inclinés et inclinés de manière aléatoire.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Entrée couleur</i> | Données du Flood Fill de base. |
| <b>Entrée d&#39;angle</b> <i>Entrée en niveaux de gris</i> | Carte facultative pour déterminer l’angle par cellule avec une carte externe. |
| <b>Entrée Pente</b> <i>Entrée en niveaux de gris</i> | Mappage facultatif pour déterminer la pente-force du dégradé par cellule. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Angle</b> <i>0.0 - 1.0</i> | Définit un angle/une direction uniforme et global pour toutes les mosaïques. |
| <b>Variation d&#39;angle</b> <i>0.0 - 1.0</i> | Rend aléatoire l’angle de chaque carreau individuellement. C&#39;est le paramètre le plus utile et le plus puissant ! |
| <b>Multiplier par la taille du cadre de sélection</b> <i>0.0 - 1.0</i> | Met à l’échelle l’ensemble de l’effet linéaire en fonction de la taille de chaque cadre de sélection. Cela signifie que les carreaux plus petits finiront par être plus sombres que les plus grands. |
| <b>Multiplicateur d&#39;entrée d&#39;image d&#39;angle</b> <i>0.0 - 1.0</i> | Définir l&#39;influence de la Map d&#39;entrée angulaire facultative sur les directions de dégradé générées |
| <b>Multiplicateur d&#39;entrée d&#39;image de Pente</b> <i>0.0 - 1.0</i> | Définissez l’influence de la Map d&#39;entrée de Pente facultative sur la force de pente de dégradé générée. |
| <b>Multiplier par l&#39;intensité de la Pente</b> <i>0.0 - 1.0</i> |  |
| <b>Couleur de Pente plate</b> <i>(valeur Niveaux de gris)</i> | Permet de définir la valeur solide pour les pentes plates. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex1.png" />
        </td>
    </tr>
</table>
