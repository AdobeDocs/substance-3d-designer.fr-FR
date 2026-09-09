---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: Utilisez le noeud de filtrage Ombres pour générer des effets d’ombre à partir de textures de saisie afin d’ajouter de la profondeur et du réalisme aux matériaux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tons foncés (nœud de filtre)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# Tons foncés (nœud de filtre)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shadows-filter-node.resources/shadows-1.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Version brute en niveaux de gris uniquement du nœud [Shape Drop Shadow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md). Il prend uniquement une forme binaire en noir et blanc comme entrée et renvoie uniquement l’ombre.

Peut être utile si vous êtes juste après l&#39;ombre et que vous ne souhaitez pas travailler avec un nœud plus complet, par exemple lors de la construction de votre propre matériau ou de l&#39;éclairage baké.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Distance de l&#39;ombre</b> <i>0.0 - 1.0</i> | Détermine la distance sur laquelle l’ombre doit tomber. |
| <b>Angle de la lumière</b> <i>0.0 - 1.0</i> | Contrôle l’angle d’incidence de la lumière. |
| <b>Lissage Des Bords</b> <i>0.0 - 1.0</i> | Détermine la dureté ou la douceur des contours des ombres. |
| <b>Exemples</b> <i>1 - 16</i> | Définit la qualité du paramètre Lissage des contours. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shadows-filter-node.resources/shadow-ex.png" />
        </td>
    </tr>
</table>
