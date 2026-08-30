---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
breadcrumb-title: ''
description: Utilisez le nœud Plage d’histogrammes pour remapper les valeurs de texture en fonction des plages d’histogrammes pour la correction et les réglages des couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Plage d’histogrammes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# Plage d’histogrammes

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-range.resources/histogram-range-1.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Réduire et/ou déplacer la plage d’une entrée en niveaux de gris. Peut être utilisé pour remapper les transitions, comme la [luminosité du contraste](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md), mais avec des commandes différentes qui pourraient être plus logiques dans certaines situations.\
Voir également [Analyse de l&#39;histogramme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) pour trouver un autre moyen plus utile de remapper la plage.

[Cliquez ici pour visionner une vidéo de Substance Academy sur la gamme d&#39;histogrammes.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Plage</b> <i>0.0 - 1.0</i> | Valeur de réduction de la plage. Cela revient à déplacer les curseurs Niveaux min et Max vers l’intérieur. |
| <b>Position</b> <i>0.0 - 1.0</i> | Décalage pour la réduction de la plage, en définissant un point médian différent pour la réduction de la plage. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-range.resources/histogram-range.gif" />
        </td>
    </tr>
</table>
