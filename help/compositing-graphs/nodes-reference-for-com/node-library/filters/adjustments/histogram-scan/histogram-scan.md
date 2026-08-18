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
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 5%

---


# Numérisation de l’histogramme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

## Numérisation de l’histogramme

**Entrée :** *Filtres/Réglages*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud très simple mais utile qui fournit un moyen intuitif de remapper le contraste et la luminosité des images en niveaux de gris en entrée. Peut être utilisé pour « agrandir » et « rétrécir » les masques de manière dynamique.

[Cliquez ici pour visionner une vidéo de Substance Academy sur les opérations d&#39;histogramme.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

## Paramètres

* **Position** :*0.0 - 1.0* Comme pour une commande de luminosité, décale le milieu du résultat. Lorsqu’il est utilisé sur une entrée de dégradé, le point de transition est développé et réduit.\
  Important : une valeur par défaut de 0 signifie que le résultat final est toujours noir. Commencez par 0,5 !
* **Contraste** : *0,0 - 1,0*\
  Règle le contraste du résultat. Permet de définir la dureté de la transition.
* **Inverser la position** :*Faux/Vrai* Inverse le résultat final.

## Exemples d’images

![](../../../../../../assets/histogram-scan.gif)

![](../../../../../../assets/histogram-scan2.gif)

![](../../../../../../assets/histogram-scan3.gif)

</td>
</tr>
</table>
