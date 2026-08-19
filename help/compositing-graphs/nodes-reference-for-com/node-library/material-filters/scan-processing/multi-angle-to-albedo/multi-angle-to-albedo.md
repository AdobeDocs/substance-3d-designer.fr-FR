---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: Utilisez le nœud Multi-angle pour l'Albédo pour extraire des cartes d'albédo à partir d'images numérisées multi-angle pour obtenir des couleurs de matériau propres.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Plusieurs angles par rapport à l’Albédo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Plusieurs angles par rapport à l’Albédo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-albedo.png){width="128px"}

## Plusieurs angles par rapport à l’Albédo

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud tente de supprimer toutes les informations d&#39;éclairage d&#39;un ensemble de photographies/scans d&#39;entrée qui ont été prises sous différents angles d&#39;éclairage. Il combine tous les échantillons dans une seule image qui devrait être aussi neutre que possible en lumière, et donc PBR-correct.

Gardez à l’esprit que plus vous avez d’échantillons et plus la différence d’angle d’éclairage est importante, plus vous obtiendrez de résultats. À partir de quatre échantillons, il devrait être possible d&#39;obtenir des résultats presque parfaits, en fonction de vos images d&#39;entrée. Les images d’entrée doivent être prises avec un trépied et présenter peu ou pas de différences, idéalement, sauf pour l’éclairage sous un angle différent !

>[!NOTE]
>
> Voir [Multi-Angle à Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) pour la version Normalmap de ce nœud. Si vous souhaitez prétraiter vos entrées, [Multi-Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi-recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) et [Multi-correctif de duplication](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) peuvent être utiles, car ils sont destinés à être associés à ces nœuds.
> 
> [L’article de blog « Your Smartphone is a Material Scanner » illustre un peu mieux ce processus.](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

## Paramètres

### Entrées

* **Entrée 1-8** :*Entrée couleur* Le nombre d&#39;entrées est déterminé par le paramètre Quantité d&#39;échantillons.

### Paramètres

* **Quantité d&#39;échantillons** : *2 - 8* définit le nombre d&#39;échantillons (entrées) à utiliser dans le traitement.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
