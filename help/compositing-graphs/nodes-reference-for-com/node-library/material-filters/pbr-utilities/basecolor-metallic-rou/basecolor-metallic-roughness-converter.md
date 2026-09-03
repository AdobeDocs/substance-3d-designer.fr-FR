---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: Utilisez le nœud Convertisseur de rugosité métallique de couleur de base pour convertir entre différents formats de matériau et workflows PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Convertisseur de rugosité métallique de couleur de base
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# Convertisseur couleur de base/métallique/rugosité

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](basecolor-metallic-roughness-converter.resources/basecolor-metallic-roughness-converter-01.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Utilitaires PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud convertit les cartes de couleur de base, de métal et de rugosité en différentes sorties de modèle PBR, telles que le modèle de Specular/brillance. Certaines des cibles de sortie incluses sont des moteurs de rendu bien connus tels que Vray, Corona, Redshift, Renderman et Arnold.

Ceci est utile si vous avez des graphiques ou des matériaux qui sont réalisés avec un modèle de PBR, alors que votre cible nécessite un modèle différent.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Utiliser l&#39;entrée SpecularLevel</b> <i>Faux/Vrai</i> | Expose un emplacement d&#39;entrée supplémentaire à l&#39;entrée SpecularLevel. Ceci est également pris en compte lors de la conversion. |
| <b>Cible</b> <i>PBR Diffuse/Specular/Gloss, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)</i> | Définit le modèle cible de conversion. |
