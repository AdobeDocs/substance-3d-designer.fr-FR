---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Utilisez le nœud Seuil pour convertir les textures en niveaux de gris en noir et blanc en fonction d’une valeur de seuil pour la création de masques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seuil
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# Seuil

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## Seuil

**Entrée :** *Filtres/Réglages*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Renvoie une valeur blanche si les *critères de comparaison* définis dans le paramètre **Mode** sont respectés pour la valeur de pixel d&#39;entrée par rapport à la valeur **Seuil**.\
Similaire à l&#39;[Histogramme numérisé](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), mais avec un contraste toujours au niveau maximal. Permet d’obtenir plus rapidement et avec plus de précision des résultats similaires à ceux de l’histogramme.

### Paramètres

* **Seuil** : *0.0 - 1.0*\
  Valeur de luminance à laquelle la valeur du pixel d’entrée est comparée.
* **Mode** :\
  Critère par lequel la valeur du pixel d&#39;entrée doit être comparée à la valeur **Seuil** :
  * *Supérieur*
  * *Supérieur ou égal*
  * *Inférieur*
  * *Inférieur ou égal*

## Exemples d’images

</td>
</tr>
</table>
