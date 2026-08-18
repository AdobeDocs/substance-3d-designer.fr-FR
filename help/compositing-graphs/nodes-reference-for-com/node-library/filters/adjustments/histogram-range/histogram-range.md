---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
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
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# Plage d’histogrammes

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-range-1.png){width="128px"}

## Plage d’histogrammes

**Entrée :** *Filtres/Réglages*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Réduire et/ou déplacer la plage d’une entrée en niveaux de gris. Peut être utilisé pour remapper les transitions, comme la [luminosité du contraste](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md), mais avec des commandes différentes qui pourraient être plus logiques dans certaines situations.\
Voir également [Analyse de l&#39;histogramme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) pour trouver un autre moyen plus utile de remapper la plage.

[Cliquez ici pour visionner une vidéo de Substance Academy sur la gamme d&#39;histogrammes.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

## Paramètres

* **Plage** : *0,0 - 1,0* Jusqu&#39;à quel point réduire la plage. Cela revient à déplacer les curseurs Niveaux min et Max vers l’intérieur.
* **Position** : *0,0 - 1,0* décalage pour la réduction de la plage, en définissant un point médian différent pour la réduction de la plage.

## Exemples d’images

![](../../../../../../assets/histogram-range.gif)

</td>
</tr>
</table>
