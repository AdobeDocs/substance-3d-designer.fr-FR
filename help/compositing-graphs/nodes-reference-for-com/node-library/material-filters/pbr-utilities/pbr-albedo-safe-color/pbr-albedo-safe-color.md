---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: Utilisez le nœud Couleur admissible pour l'Albédo PBR pour vous assurer que les couleurs de l'albédo se trouvent dans des plages physiquement plausibles pour les matériaux PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur sécurisée pour l’Albédo PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Couleur sécurisée pour l’Albédo PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-albedo-safe-color.resources/pbr-albedo-safe-color-01.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Utilitaires PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s’agit d’un nœud utilitaire qui effectue des corrections si la couleur de base ou les valeurs de Diffuse se trouvent en dehors d’une plage acceptable et PBR. Lorsqu’il est défini sur Métallique, le nœud tente également de corriger les valeurs de couleur de base en fonction de l’intensité Métallique.

Voir également [Couleur de base PBR / Validation Métallique](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) pour obtenir un retour visuel sur les zones qui pourraient être erronées.

C&#39;est utile comme outil de correction rapide, surtout quand on apprend encore PBR, mais pas comme mesure absolue qui est toujours censée être correcte.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Workflow PBR</b> <i>Base color - Métallique, Diffuse - Specular</i> | Bascule entre deux workflows PBR différents. |
| <b>Tolérance</b> <i>0.0 - 1.0</i> | Quantité de tolérance pour les valeurs qui sont hors limites. |
