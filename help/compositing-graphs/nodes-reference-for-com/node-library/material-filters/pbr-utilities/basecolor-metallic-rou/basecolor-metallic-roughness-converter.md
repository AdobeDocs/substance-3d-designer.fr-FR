---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Convertisseur couleur de base/métallique/rugosité

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

## Convertisseur couleur de base/métallique/rugosité

**Entrée :** *Filtres de matériaux/Utilitaires PBR*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud convertit les cartes de couleur de base, de métal et de rugosité en différentes sorties de modèle PBR, telles que le modèle de Specular/brillance. Certaines des cibles de sortie incluses sont des moteurs de rendu bien connus tels que Vray, Corona, Redshift, Renderman et Arnold.

Ceci est utile si vous avez des graphiques ou des matériaux qui sont réalisés avec un modèle de PBR, alors que votre cible nécessite un modèle différent.

## Paramètres

* **Utiliser l&#39;entrée SpecularLevel** : *Faux/Vrai* Expose un emplacement d&#39;entrée supplémentaire à l&#39;entrée SpecularLevel. Ceci est également pris en compte lors de la conversion.
* ***Cible** : *PBR Diffuse/Specular/Gloss, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)**définit le modèle cible de conversion.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
