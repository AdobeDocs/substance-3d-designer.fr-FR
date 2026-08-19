---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Utilisez le nœud Annulation AO pour supprimer l'occlusion ambiante des matériaux numérisés pour un traitement de texture propre.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Annulation d’AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# Annulation d’AO

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## Annulation d’AO

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud tente de supprimer toutes les informations d&#39;éclairage de l&#39;Occlusion ambiante de votre mappage d&#39;Albédo (couleur de base), en fonction d&#39;une entrée de mappage AO distincte. Il peut être utilisé pour s&#39;assurer que les informations de votre Albédo sont correctes et généralement dépourvues d&#39;informations d&#39;éclairage (fort).

Un nœud utile pour lorsque vous avez une carte AO d&#39;un maillage numérisé, ou même une carte AO générée à partir d&#39;informations d&#39;Height ou Normal.

## Paramètres

* **Annulation de l&#39;AO** : *0.0 - 1.0* Intensité avec laquelle supprimer les informations d&#39;éclairage.
* **Saturation AO** : *0.0 - 1.0*(Désaturation) pour les zones où l’éclairage est supprimé. Cela permet de corriger toute perte de couleur dans les zones plus sombres.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
