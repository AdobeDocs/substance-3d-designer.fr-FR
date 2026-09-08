---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Utilisez le nœud Remplacer la gamme de couleurs pour remplacer les couleurs d’une gamme spécifiée par de nouvelles couleurs pour la correction colorimétrique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Remplacer la gamme de couleurs
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# Remplacer la gamme de couleurs

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Remplace la couleur source par la couleur cible, à l’aide de commandes supplémentaires. Peut, par exemple, être utilisé pour recolorer des parties d’un Map id de Matériau (baking).

Pour une version plus avancée, voir [Correspondance des couleurs.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Couleur source</b> <i>(valeur de couleur)</i> | Couleur à remplacer. |
| <b>Couleur cible</b> <i>(valeur de couleur)</i> | Couleur de remplacement. |
| <b>Plage source</b> <i>0.0 - 1.0</i> | Plage ou tolérance de la source sélectionnée. Peut être augmenté pour que les couleurs voisines aient également une teinte décalée. |
| <b>Seuil</b> <i>0.0 - 1.0</i> | Atténuation/contraste pour la plage. Réglez l’option Basse pour remplacer uniquement la couleur source, l’option Haute pour remplacer également les couleurs fusionnées dans la source. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/replace-color-range-example.png" />
        </td>
    </tr>
</table>
