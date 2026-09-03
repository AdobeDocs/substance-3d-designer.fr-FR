---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: Utilisez le nœud Analyse des histogrammes non uniforme pour effectuer une analyse des histogrammes non uniforme afin d’effectuer une correction colorimétrique avancée.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Analyse d'histogramme non uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Analyse d&#39;histogramme non uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform-01.png){width="128px"}

<b>Entrée :</b> Filtres > Réglages

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Version avancée de l&#39;[Histogramme des numérisations](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), avec des commandes et des entrées supplémentaires pour piloter l&#39;effet à un niveau par pixel, plutôt qu&#39;uniformément sur l&#39;ensemble de l&#39;image. Peut être utilisé pour obtenir un contraste et des transitions encore plus complexes dans les masques.

Son utilisation est beaucoup plus complexe que celle de l&#39;[histogramme des couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) standard. Veillez donc à vous en familiariser avant d&#39;essayer d&#39;utiliser la version non uniforme.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Entrée en niveaux de gris</i> | Résultat source à modifier. |
| <b>Mappage de position</b> <i>Entrée en niveaux de gris</i> | Emplacement d&#39;entrée pour le paramètre Position du lecteur. Activé lorsque l’option « Utiliser l’entrée de position » est définie sur Vrai. La plage de valeurs effective est petite et dépend de la courbe de contraste et du paramètre. |
| <b>Carte de contraste</b> <i>Entrée en niveaux de gris</i> | Emplacement d&#39;entrée pour piloter le paramètre de contraste. Activé lorsque l’option « Utiliser l’entrée de contraste » est définie sur True. La plage de valeurs effectives est petite. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Utiliser l&#39;entrée de position</b> <i>Faux/Vrai</i> | Activez/désactivez l&#39;emplacement d&#39;entrée Mappage de position. |
| <b>position</b> <i>0.0 - 1.0</i> | Contrôle ou modifie les résultats de mappage pour piloter le paramètre de position. |
| <b>Utiliser l&#39;entrée de contraste</b> <i>Faux/Vrai</i> | Activez/désactivez l’emplacement d’entrée Mappage de contraste. |
| <b>contraste</b> <i>0.0 - 1.0</i> | Contrôle ou modifie les résultats de mappage pour piloter le paramètre de contraste. |
