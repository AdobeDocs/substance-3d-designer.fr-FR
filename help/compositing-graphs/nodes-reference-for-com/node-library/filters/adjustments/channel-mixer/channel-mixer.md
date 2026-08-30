---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/channel-mixer.html"
breadcrumb-title: ''
description: Utilisez le nœud Mélangeur de couches pour mélanger les couches de couleur afin de créer des effets de couleur et de convertir les espaces colorimétriques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Channel Mixer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mélangeur de couches
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---


# Mélangeur de couches

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](channel-mixer.resources/channel-mixer.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Permet de mélanger, d’échanger et de fusionner des couches de RGB. Peut être utilisé pour agrandir les canaux, effectuer des conversions en niveaux de gris plus précises et différents types de packing.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canal Rouge</b> <i>-200.0 - 200.0</i> | Détermine la proportion des canaux du RGB d’entrée qui passe dans le canal Rouge de sortie. |
| <b>Canal Vert</b> <i>-200.0 - 200.0</i> | Détermine la proportion des canaux du RGB d’entrée qui passe dans le canal vert de sortie. |
| <b>Canal bleu</b> <i>-200.0 - 200.0</i> | Détermine la proportion des canaux du RGB d’entrée qui passe dans le canal Bleu en sortie. |
| <b>Monochrome</b> <i>Faux/Vrai</i> | Sortie en monochrome. Permet une conversion plus précise des niveaux de gris. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="channel-mixer.resources/channelmixer.gif" />
        </td>
    </tr>
</table>
