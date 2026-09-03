---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Recadrage de matière

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-crop.resources/material-crop-01.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud est la version multicanal et matérielle complète de [Recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Il vous permet d’effectuer une opération de recadrage sur tous les canaux Matériau en parallèle.

>[!NOTE]
>
> [Voir le recadrage d&#39;origine](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [2&rbrace;pour plus d&#39;informations](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md).[&#128279;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les couches de matériau dans ce groupe, lors de l’utilisation de cartes de Specular/brillance au lieu de cartes de métal/rugosité, par exemple. |
| <b>Taille d&#39;entrée</b> <i>0 - 8192</i> | Résolution et proportions de l&#39;Image d&#39;entrée. Très important pour les images non carrées. |
| <b>Arrière-plan</b> <i>(Valeur de couleur) / (Valeur de niveaux de gris)</i> | Valeur uniforme de base pour les superficies non couvertes par le recadrage. |
| <b>Transformation</b> <i>(Matrice de transformation)</i> | Fait pivoter et met à l’échelle le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
