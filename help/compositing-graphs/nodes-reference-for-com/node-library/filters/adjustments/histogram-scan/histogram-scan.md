---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: Utilisez le nœud de numérisation Histogramme pour numériser et analyser les histogrammes de texture à des fins de correction et de réglage des couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Numérisation de l’histogramme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# Numérisation de l’histogramme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan.resources/histogram-scan-01.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud très simple mais utile qui fournit un moyen intuitif de remapper le contraste et la luminosité des images en niveaux de gris en entrée. Peut être utilisé pour « agrandir » et « rétrécir » les masques de manière dynamique.

[Cliquez ici pour visionner une vidéo de Substance Academy sur les opérations d&#39;histogramme.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Position</b> <i>0.0 - 1.0</i> | Comme pour une commande de luminosité, décale le milieu du résultat. Lorsqu&#39;il est utilisé sur une entrée de dégradé, ce paramètre étend et réduit le point de transition.<br><br>Important : une valeur par défaut de 0 signifie que le résultat final est toujours noir, alors essayez de commencer par 0,5 ! |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. Permet de définir la dureté de la transition. |
| <b>Inverser la position</b> <i>Faux/Vrai</i> | Inverse le résultat final. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan-04.gif" />
        </td>
    </tr>
</table>
