---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: Utilisez le nœud Recadrage de matériau pour recadrer des zones de texture à partir de matériaux numérisés afin d’isoler des zones spécifiques d’intérêt.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recadrage de matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# Recadrage de matière

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

## Recadrage de matière

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud est la version multicanal et matérielle complète de [Recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Il vous permet d’effectuer une opération de recadrage sur tous les canaux Matériau en parallèle.

>[!NOTE]
>
> [Voir le recadrage d&#39;origine](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[2}pour plus d&#39;informations](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md).](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[

## Paramètres

### Paramètres

* **Canaux**
  * Activez et désactivez les couches de matériau dans ce groupe, lors de l’utilisation de cartes de Specular/brillance au lieu de cartes de métal/rugosité, par exemple.
* **Taille d&#39;entrée** : *0 - 8192* Résolution et proportions de l&#39;image d&#39;entrée. Très important pour les images non carrées.
* **Arrière-plan** : *(Valeur de couleur) / (Valeur de niveaux de gris)*Valeur uniforme d&#39;arrière-plan pour les zones non couvertes par le recadrage.
* **Transformation** : *(Matrice De Transformation)*\
  Fait pivoter et met à l’échelle le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.
* **Décalage** : *0,0 - 1,0*\
  Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
