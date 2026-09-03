---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# Recadrage multiple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-crop.resources/multi-crop-01.png){width="128px"}

![](multi-crop.resources/multi-crop-02.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s’agit de la version multicanal de Recadrage. Il rogne une zone d&#39;une image et est principalement destiné à être utilisé avec des photos à plusieurs angles, qui sont ensuite associées à [Plusieurs angles pour obtenir l&#39;Albédo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou à [Plusieurs angles pour obtenir une normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Voir le [recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) d&#39;origine pour plus d&#39;informations.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Nombre d&#39;entrées</b> <i>1 - 8</i> | Définit le nombre d’entrées à traiter en parallèle. |
| <b>Taille d&#39;entrée</b> <i>0 - 8192</i> | Résolution et proportions des Images d&#39;entrée. Très important pour les images non carrées. |
| <b>Arrière-plan</b> <i>(Valeur de couleur) / (Valeur de niveaux de gris)</i> | Valeur uniforme de base pour les superficies non couvertes par le recadrage. |
| <b>Transformation</b> <i>(Matrice de transformation)</i> | Fait pivoter et met à l’échelle le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Est normal (uniquement pour la version couleur)</b> <i>Faux/Vrai</i> | Indique si l&#39;entrée doit être traitée ou non comme un mappage normal. |
