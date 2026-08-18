---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Utilisez le nœud Recadrage multiple pour recadrer simultanément plusieurs couches de texture afin de traiter efficacement les matériaux numérisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recadrage multiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Recadrage multiple

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

## Recadrage multiple (niveaux de gris)

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Il s’agit de la version multicanal de Recadrage. Il rogne une zone d&#39;une image et est principalement destiné à être utilisé avec des photos à plusieurs angles, qui sont ensuite associées à [Plusieurs angles pour obtenir l&#39;Albédo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou à [Plusieurs angles pour obtenir une normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Voir le [recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) d&#39;origine pour plus d&#39;informations.

## Paramètres

### Paramètres

* **Nombre d&#39;entrées** : *1 - 8* Définit le nombre d&#39;entrées à traiter en parallèle.
* **Taille d&#39;entrée** : *0 - 8192* résolution et proportions des images d&#39;entrée. Très important pour les images non carrées.
* **Arrière-plan** : *(Valeur de couleur) / (Valeur de niveaux de gris)*Valeur uniforme d&#39;arrière-plan pour les zones non couvertes par le recadrage.
* **Transformation** : *(Matrice De Transformation)*\
  Fait pivoter et met à l’échelle le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.
* **Décalage** : *0,0 - 1,0*\
  Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.
* **Est normal (uniquement pour la version en couleurs)** : *Faux/Vrai* Indique si l’entrée doit être traitée ou non comme une carte normale.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
