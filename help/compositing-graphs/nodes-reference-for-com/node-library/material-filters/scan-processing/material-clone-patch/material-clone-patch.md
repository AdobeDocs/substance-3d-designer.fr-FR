---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: Utilisez le nœud Pièce de duplication de matériau pour cloner et corriger des régions de texture afin de corriger des artefacts dans des matériaux numérisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch de duplication de matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# Patch de duplication de matériau

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-clone-patch.resources/clone-patch-material.png){width="128px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s&#39;agit de la version matérielle multicanaux complète de [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Il effectue un patch de duplication sur tous les canaux d’un matériau. [Voir la version d&#39;origine pour plus d&#39;informations !](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Cette fonction est très utile si vous souhaitez supprimer un détail de toutes les couches d’un matériau. Génère des images de débogage pour plusieurs canaux afin de voir à quoi ressemble exactement la zone de correctif dynamique.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité. |
| <b>Forme</b> <i>Carré, Disque</i> | Définit la forme du tampon. Utilisé uniquement comme base. |
| <b>Edge</b> |  |
| <b>Seuil (pour plusieurs canaux)</b> <i>0.0 - 1.0</i> | Définit l’étendue de la zone de fusion. Cette action se développe par paliers, le long des formes dans la zone cible, de sorte qu’elle a très peu d’effet avec des arrière-plans uniformes. Veillez à ne pas trop modifier ce paramètre entre les canaux, car cela pourrait entraîner des différences visuelles. |
| <b>Flou</b> <i>0.0 - 2.0</i> | Atténue les bords de la zone de tampon au cas où une transition plus douce serait nécessaire. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arrondit les bords de la forme du tampon pour créer des contours plus fluides. |
| <b>Résolution de Grille</b> <i>1 - 11</i> | Définit la résolution de la qualité de l’analyse de fusion. Plus la valeur est élevée, plus la fusion est précise. |
| <b>Transformations</b> |  |
| <b>Matrice source</b> <i>(Matrice de transformation)</i> | Transforme la source (échelle et rotation). Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres. |
| <b>Décalage source</b> <i>-0.5 - 0.5</i> | Translate l’emplacement source. Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres. *Ce paramètre est probablement le principal que vous souhaitez modifier !* |
| <b>Matrice cible</b> <i>(Matrice de transformation)</i> | Transforme l’emplacement cible (échelle et rotation). Peut également être effectué via le widget sur la zone de travail. |
| <b>Décalage cible</b> <i>-0.5 - 0.5</i> | Translate l’emplacement cible. Peut également être effectué via le widget sur la zone de travail. |
