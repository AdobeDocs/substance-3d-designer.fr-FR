---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Utilisez le nœud Pièce à plusieurs clones pour cloner et corriger plusieurs couches de texture afin de corriger les artefacts de matière numérisée.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Correctif Multi-Clones
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# Correctif Multi-Clones

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/clone-patch-multi.png){width="128px"}

![](multi-clone-patch.resources/clone-patch-multi-grayscale.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Ce nœud est la version multi-entrée de [Correctif de duplication](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Il relie jusqu’à huit entrées et effectue exactement la même opération de Pièce de duplication sur chacune d’elles. Il est principalement destiné à être utilisé avec des photos multi-angles, qui sont ensuite combinées avec [Multi-angle à l&#39;Albédo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Multi-angle à la normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Voir [Patch de duplication](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) pour plus d&#39;informations, voir [Patch de duplication de matériau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) pour la version de matériau.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Nombre d&#39;entrées</b> <i>1 - 8</i> | Définit la quantité d&#39;entrées qui recevront la même opération de patch. |
| <b>Est normal (uniquement pour la couleur)</b> <i>Faux/Vrai</i> | Définit si l&#39;entrée est une carte normale et si la fusion doit être traitée comme telle. |
| <b>Forme</b> <i>Carré, Disque</i> | Définit la forme du tampon. Utilisé uniquement comme base. |
| <b>Edge</b> |  |
| <b>Seuil</b> <i>0.0 - 1.0</i> | Définit l’étendue de la zone de fusion. Cette action se développe par paliers le long des formes dans la zone cible ; elle a très peu d’effet avec des arrière-plans uniformes. |
| <b>Flou</b> <i>0.0 - 2.0</i> | Atténue les bords de la zone de tampon, au cas où une transition plus douce serait nécessaire. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arrondit les bords de la forme du tampon pour créer des contours plus fluides. |
| <b>Résolution de Grille</b> <i>1 - 11</i> | Définit la résolution de la qualité de l’analyse de fusion. Plus la valeur est élevée, plus la fusion est précise. |
| <b>Transformations</b> |  |
| <b>Matrice source</b> <i>(Matrice de transformation)</i> | Transforme la source (échelle et rotation). Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres. |
| <b>Décalage source</b> <i>-0.5 - 0.5</i> | Translate l’emplacement source. Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres. *Ce paramètre est probablement le principal que vous souhaitez modifier !* |
| <b>Matrice cible</b> <i>(Matrice de transformation)</i> | Transforme l’emplacement cible (échelle et rotation). Peut également être effectué via le widget sur la zone de travail. |
| <b>Décalage cible</b> <i>-0.5 - 0.5</i> | Translate l’emplacement cible. Peut également être effectué via le widget sur la zone de travail. |
