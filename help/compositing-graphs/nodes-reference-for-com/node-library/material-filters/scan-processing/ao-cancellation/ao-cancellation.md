---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Utilisez le nœud d'annulation AO pour supprimer l'ambient occlusion des matériaux numérisés pour un traitement de texture propre.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Annulation d’AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# Annulation d’AO

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud tente de supprimer toutes les informations d&#39;éclairage d&#39;Ambient occlusion de votre mappage d&#39;Albédo (de Base color), en fonction d&#39;une entrée de mappage AO distincte. Il peut être utilisé pour s&#39;assurer que les informations de votre Albédo sont correctes et généralement dépourvues d&#39;informations d&#39;éclairage (fort).

Un nœud utile pour lorsque vous avez un mappage AO baké à partir d&#39;un maillage numérisé, ou même un mappage AO généré à partir d&#39;informations d&#39;Height ou Normal.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Annulation de l&#39;AO</b> <i>0.0 - 1.0</i> | Force de suppression des informations d’éclairage. |
| <b>Saturation AO</b> <i>0.0 - 1.0</i> | Compensation de la saturation pour les zones où l’éclairage est supprimé. Cela permet de corriger toute perte de couleur dans les zones plus sombres. |
