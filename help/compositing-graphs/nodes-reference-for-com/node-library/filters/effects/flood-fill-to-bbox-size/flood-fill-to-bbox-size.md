---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Utilisez le nœud Taille du Flood Fill à la zone pour remplir les zones avec des valeurs de taille de cadre de sélection pour les effets de mise à l’échelle procédural.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill à la taille de la boîte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---


# Flood Fill à la taille de la boîte

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-bbox-size.resources/floodfill-to-bbox-size.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un mappage en niveaux de gris à partir d&#39;un [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md), avec des valeurs liées à la taille individuelle de chaque vignette.

Les valeurs sont calculées par rapport à la taille totale de la zone de travail (un carreau blanc intégral étire toute la zone de travail). Le contraste est donc souvent faible.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Sortie</b> <i>max(X, Y), X, Y</i> | Définit la mesure sur laquelle la valeur est basée : la largeur, la longueur ou les deux. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-bbox-size.resources/floodbbox-ex1.png" />
        </td>
    </tr>
</table>
