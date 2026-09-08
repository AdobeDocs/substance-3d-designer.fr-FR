---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Utilisez le nœud Hald CLUT pour appliquer des tables de correspondance de couleur à l'aide du format Hald CLUT pour l'étalonnage et la correction des couleurs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique une table LUT à l’image d’entrée. Le LUT doit être au format Hald en résolution 4096\*4096. Voir <http://www.quelsolaar.com/technology/clut.html> pour plus d&#39;informations.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>entrée</b> <i>Entrée couleur</i> | Image sur laquelle appliquer le LUT. |
| <b>lut</b> <i>Entrée couleur</i> | Emplacement d’entrée Lut. Doit être 4096x4096. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Intensité LUT par Alpha</b> <i>Faux/Vrai</i> | Définit si l’effet LUT est pondéré par le canal Alpha. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/content-hald-clut.jpg" />
        </td>
    </tr>
</table>
