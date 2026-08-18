---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: Utilisez le nœud Recadrer pour recadrer les sorties de matériau vers des zones spécifiques afin de traiter les matériaux et les textures numérisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recadrer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# Recadrer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-10.png){width="128px"}

![](../../../../../../assets/crop-grayscale.png){width="128px"}

## Recadrage (niveaux de gris)

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Le recadrage est une version paramétrique et non destructive de l’outil de recadrage que vous connaissez bien. Vous sélectionnez une zone d’une image et le résultat est renvoyé avec les zones non sélectionnées supprimées.

Elle peut être utile de plusieurs façons, car effectuer une opération de recadrage avec des nœuds atomiques n&#39;est pas si simple. Ce nœud est particulièrement utile pour la conversion d’images non carrées. Dans ce cas, assurez-vous de définir correctement la résolution d’entrée.

Il est très important de comprendre que pour utiliser facilement ce nœud, vous devez bien utiliser la possibilité de prévisualiser un nœud différent de celui dont vous modifiez les paramètres !\
En bref : **double-cliquez** sur le nœud que vous utilisez comme entrée pour celui-ci (l&#39;image d&#39;origine, non recadrée), puis **cliquez une fois** sur le nœud de recadrage qui suit immédiatement. Vous pouvez ensuite modifier le widget de recadrage pour l’adapter à la zone de recadrage.

## Paramètres

* **Taille d&#39;entrée** : *0 - 8192* Résolution et proportions de l&#39;image d&#39;entrée. Très important pour les images non carrées.
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
