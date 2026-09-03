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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 3%

---


# Recadrer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](crop.resources/crop-01.png){width="128px"}

![](crop.resources/crop-02.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le recadrage est une version paramétrique et non destructive de l’outil de recadrage que vous connaissez bien. Vous sélectionnez une zone d’une image et le résultat est renvoyé avec les zones non sélectionnées supprimées.

Elle peut être utile de plusieurs façons, car effectuer une opération de recadrage avec des nœuds atomiques n&#39;est pas si simple. Ce nœud est particulièrement utile pour la conversion d’images non carrées. Dans ce cas, assurez-vous de définir correctement la résolution d’entrée.

Il est très important de comprendre que pour utiliser facilement ce nœud, vous devez bien utiliser la possibilité de prévisualiser un nœud différent de celui dont vous modifiez les paramètres !\
En bref : **double-cliquez** sur le nœud que vous utilisez comme entrée pour celui-ci (l&#39;image d&#39;origine, non recadrée), puis **cliquez une fois** sur le nœud de recadrage qui suit immédiatement. Vous pouvez ensuite modifier le widget de recadrage pour l’adapter à la zone de recadrage.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Taille d&#39;entrée</b> <i>0 - 8192</i> | Résolution et proportions de l&#39;Image d&#39;entrée. Très important pour les images non carrées. |
| <b>Arrière-plan</b> <i>(Valeur de couleur) / (Valeur de niveaux de gris)</i> | Valeur uniforme de base pour les superficies non couvertes par le recadrage. |
| <b>Transformation</b> <i>(Matrice de transformation)</i> | Fait pivoter et met à l’échelle le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Est normal (uniquement pour la version couleur)</b> <i>Faux/Vrai</i> | Indique si l&#39;entrée doit être traitée ou non comme un mappage normal. |
