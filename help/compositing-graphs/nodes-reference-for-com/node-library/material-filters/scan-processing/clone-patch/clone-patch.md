---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: Utilisez le nœud Pièce de duplication pour cloner et corriger des zones dans des matériaux numérisés afin de supprimer des artefacts et des imperfections.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pièce de duplication
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# Pièce de duplication

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-patch.resources/clone-patch-01.png){width="128px"}

![](clone-patch.resources/clone-patch-02.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le patch de duplication est un nœud paramétrique procédural « Clone Stamp ». Il duplique une zone d’une entrée vers une autre, masquant ainsi les détails potentiellement indésirables. Bien qu&#39;il ne soit pas aussi rapide et facile que d&#39;utiliser un outil familier dans une application à base de pinceaux, il offre l&#39;avantage clé d&#39;être non destructif et de travailler dans un workflow basé sur les nœuds. En outre, ce nœud effectue une analyse intelligente de la zone cible et de la zone source, et tente de fusionner les éléments aussi bien que possible en fonction du contraste, des valeurs et des formes.

Cette fonctionnalité est principalement destinée aux rares moments où vous souhaitez effectuer une correction manuelle d’une zone spécifique, au cas où il y aurait un détail indésirable quelque part.

Gardez à l’esprit qu’il ne fonctionne pas comme un pinceau « Tampon » standard et simple. La forme de votre zone fusionnée est basée sur les formes et les valeurs des zones avec lesquelles vous travaillez, ce qui signifie qu&#39;il s&#39;agit d&#39;un nœud assez lourd qui nécessite de la patience, mais qui offre d&#39;excellents résultats.

Il est également important de comprendre que vous pouvez déplacer la zone cible avec un gadget, mais que la zone source doit être définie en modifiant les paramètres de la « matrice source ».

>[!NOTE]
>
> Si vous le souhaitez pour un matériau complet (comme c&#39;est le plus souvent le cas), consultez [Pièce de duplication de matériau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md).
> 
> Pour les cas où vous souhaitez effectuer cette opération sur plusieurs entrées en même temps (sans qu&#39;il s&#39;agisse d&#39;un matériau), consultez [Pièce à plusieurs clones](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Est normal (uniquement pour la couleur)</b> <i>Faux/Vrai</i> | Définit si l&#39;entrée est une carte normale et si la fusion doit être traitée comme telle. |
| <b>Forme</b> <i>Carré, Disque</i> | Définit la forme du tampon. Utilisé uniquement comme base. |
| <b>Edge</b> |  |
| <b>Seuil</b> <i>0.0 - 1.0</i> | Définit l’étendue de la zone de fusion. Cette technique se développe par étapes, le long des formes dans la zone cible, et a très peu d&#39;effet avec des arrière-plans uniformes<i>.</i> |
| <b>Flou</b> <i>0.0 - 2.0</i> | Atténue les bords de la zone de tampon au cas où une transition plus douce serait nécessaire. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arrondit les bords de la forme du tampon pour créer des contours plus fluides. |
| <b>Résolution de Grille</b> <i>1 - 11</i> | Définit la résolution de la qualité de l’analyse de fusion. Plus la valeur est élevée, plus la fusion est précise. |
| <b>Transformations</b> |  |
| <b>Matrice source</b> <i>(Matrice de transformation)</i> | Transforme la source (échelle et rotation). Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres. |
| <b>Décalage source</b> <i>-0.5 - 0.5</i> | Translate l’emplacement source. Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres. <i>Ce paramètre est probablement le principal que vous souhaitez modifier !</i> |
| <b>Matrice cible</b> <i>(Matrice de transformation)</i> | Transforme l’emplacement cible (échelle et rotation). Peut également être effectué via le widget sur la zone de travail. |
| <b>Décalage cible</b> <i>-0.5 - 0.5</i> | Translate l’emplacement cible. Peut également être effectué via le widget sur la zone de travail. |
