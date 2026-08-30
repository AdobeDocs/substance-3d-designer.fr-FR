---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Utilisez le nœud Seuil pour convertir les textures en niveaux de gris en noir et blanc en fonction d’une valeur de seuil de création de masque.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seuil
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# Seuil

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](threshold.resources/threshold-2.png){width="200px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Renvoie une valeur blanche si les *critères de comparaison* définis dans le paramètre **Mode** sont respectés pour la valeur de pixel d&#39;entrée par rapport à la valeur **Seuil**.\
Similaire à l&#39;[Histogramme numérisé](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), mais avec un contraste toujours au niveau maximal. Permet d’obtenir plus rapidement et avec plus de précision des résultats similaires à ceux de l’histogramme.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Seuil</b> <i>0.0 - 1.0</i> | Valeur de luminance par rapport à laquelle la valeur du pixel d’entrée est comparée. |
| <b>Mode</b> | Critère selon lequel la valeur du pixel d&#39;entrée doit être comparée à la valeur **Seuil** :<br><br>- *Supérieur*<br>- *Supérieur ou égal*<br>- *Inférieur*<br>- *Inférieur ou égal* |
