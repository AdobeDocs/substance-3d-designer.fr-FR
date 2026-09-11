---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Utilisez le nœud Polygone 1 pour générer des motifs polygonaux de base avec des côtés et des propriétés personnalisables pour les textures géométriques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Polygone 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# Polygone 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](polygon-1.resources/polygon-1-1.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une forme polygonale avec de nombreuses options de réglage. Voir [Polygone 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md) pour une version plus simple.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Côtés</b> <i>3 - 32</i> | Définit le nombre de côtés que le polygone doit avoir. |
| <b>Exploser</b> <i>0.0 - 1.0</i> | Éloigne le polygone des « tranches ». |
| <b>Taille du triangle</b> <i>0.0 - 1.0</i> | Ajuste la taille des tranches/triangles. Tout réglage peut décomposer la forme, seulement 1,1. est parfaitement connecté ! |
| <b>Échelle</b> <i>0.0 - 1.0</i> | Met à l’échelle l’ensemble de la forme. |
| <b>Mise à l&#39;échelle automatique</b> <i>Faux/Vrai</i> | Ajuste les échelles pour que l’ensemble du polygone s’affiche, avec les paramètres par défaut. |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Fait pivoter la forme entière. |
| <b>Dégradé</b> <i>Faux/Vrai</i> | Génère des tranches/triangles dégradés au lieu de tranches unies. Remarque : devient similaire à Polygone 2 lorsque ce paramètre est activé. |
| <b>Inversion de dégradé</b> <i>Faux/Vrai</i> | Inverse la direction du dégradé si l’option Dégradé est activée. |
| <b>Répétition</b> <i>1 - 16</i> | Définit le nombre de fois où le résultat doit se produire. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Active la compensation de la courbure et de la étire avec des proportions non carrées. |
| <b>Répétition Non Carrée</b> <i>Faux/Vrai</i> | Lorsque l’Extension non carrée est activée, la forme est mosaïque sans être écrasée. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="polygon-1.resources/polygon-1-ex.gif" />
        </td>
    </tr>
</table>
