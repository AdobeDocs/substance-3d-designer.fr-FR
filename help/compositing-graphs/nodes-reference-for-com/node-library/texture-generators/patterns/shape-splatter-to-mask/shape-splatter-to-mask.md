---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: Utilisez le nœud Éclaboussure de forme en masque pour convertir les motifs d’éclaboussure de forme en masques pour un mélange de matériaux et des effets.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure de forme en masque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---


# Éclaboussure de forme en masque

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Convertit les données d&#39;[éclaboussure de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) en noir et masque blanc en fonction de l&#39;ID de motif. Permet, par exemple, de créer un masque d’un certain type de motif uniquement. Propose des options supplémentaires pour sélectionner une plage d’ID de motif et masquer de manière aléatoire certaines formes.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Plage de début de l&#39;ID de motif</b> <i>1 - 8</i> | Définissez le premier ID de motif dans la plage à sélectionner. |
| <b>Plage de fin d’ID de motif</b> <i>1 - 8</i> | Définissez le dernier ID de motif dans la plage à sélectionner. |
| <b>Masque Aléatoire</b> <i>0.0 - 1.0</i> | Définissez la proportion de motifs pour qu’ils soient masqués de manière aléatoire. |
| <b>Sortie</b> <i>Masque Binaire, Masque D’Entier, Valeurs De Niveaux De Gris</i> | Déterminer le type de valeurs de sortie. Le masque binaire renvoie uniquement des valeurs de 0 ou 1 en noir et blanc. Le masque Entier code les valeurs supérieures jusqu’à 8 pour chaque motif au format HDR. Les valeurs de niveaux de gris répartissent la plage de manière proportionnelle entre 0 et 1. |
