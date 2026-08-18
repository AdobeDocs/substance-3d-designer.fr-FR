---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# Analyse d&#39;histogramme non uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

## Analyse d&#39;histogramme non uniforme

**Entrée :** *Filtres/Réglages*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Version avancée de l&#39;[Histogramme des numérisations](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), avec des commandes et des entrées supplémentaires pour piloter l&#39;effet à un niveau par pixel, plutôt qu&#39;uniformément sur l&#39;ensemble de l&#39;image. Peut être utilisé pour obtenir un contraste et des transitions encore plus complexes dans les masques.

Son utilisation est beaucoup plus complexe que celle de l&#39;[histogramme des couleurs](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) standard. Veillez donc à vous en familiariser avant d&#39;essayer d&#39;utiliser la version non uniforme.

## Paramètres

### Entrées

* **Entrée** : *Entrée en niveaux de gris* Résultat source à modifier.
* **Mappage de position** : emplacement d&#39;entrée *Niveaux de gris* pour piloter le paramètre Position. Activé lorsque l’option « Utiliser l’entrée de position » est définie sur Vrai. La plage de valeurs effective est petite et dépend de la courbe de contraste et du paramètre.
* **Carte de contraste** : emplacement d&#39;entrée *Niveaux de gris* pour piloter le paramètre de contraste. Activé lorsque l’option « Utiliser l’entrée de contraste » est définie sur True. La plage de valeurs effectives est petite.

### Paramètres

* **Utiliser l&#39;entrée de position** : *Faux/Vrai* Activer/désactiver l&#39;utilisation de l&#39;emplacement d&#39;entrée du mappage de position.
* **position** : *0.0 - 1.0* contrôle ou modifie les résultats du mappage pour piloter le paramètre de position.
* **Utiliser l&#39;entrée de contraste** : *Faux/Vrai* Activer/désactiver l&#39;emplacement d&#39;entrée de la carte de contraste.
* **contraste** : *0.0 - 1.0* contrôle ou modifie les résultats de mappage pour piloter le paramètre de contraste.

## Exemples d’images

</td>
</tr>
</table>
