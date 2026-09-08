---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: Utilisez le nœud Quantifier les niveaux de gris pour réduire le nombre de niveaux de gris des effets de postérisation.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quantifier les niveaux de gris
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Quantifier les niveaux de gris

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône Quantifier les niveaux de gris](../../../../../../assets/quantize-grayscale.png "Icône Quantifier les niveaux de gris"){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une spline unique en forme de cercle.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Étapes</b> *Nombre entier* | Nombre de valeurs séparées auxquelles la plage d&#39;entrée doit être approximée. |
| <b>Décalage</b> *Flotter* | Applique un décalage à la plage d&#39;entrée, ce qui *décale* les résultats le long de la plage. |
| <b>Pente</b> *Flotter* | Applique un dégradé de pente aux *transitions* entre des valeurs approximatives, jusqu&#39;à la *plage complète d&#39;une étape*. |
| <b>Courbe De Pente</b> *Nombre entier* | Définit la méthode d&#39;acquisition de la courbe pour la pente définie par le paramètre <b>Pente</b> :<ul data-preserve-html="true"> <li data-preserve-html="true">*Linéaire* : applique une courbe linéaire, ce qui donne une pente droite</li> <li data-preserve-html="true">*Pas en douceur* : applique une courbe à pas lisse, ce qui produit une pente lisse</li> <li data-preserve-html="true">*Entrée courbe* : applique la courbe décrite par la map d&#39;entrée <b>Entrée courbe</b>. Vous pouvez utiliser un nœud [Courbe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) pour décrire cette courbe avec beaucoup de contrôle.</li> </ul> |

## Exemples

![Exemple 1](../../../../../../assets/quantizegrayscale.gif "Exemple 1")

![Exemple 2](../../../../../../assets/quantizegrayscale.png "Exemple 2")
