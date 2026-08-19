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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Correctif Multi-Clones

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## Pièce de duplication multiple (niveaux de gris)

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud est la version multi-entrée de [Correctif de duplication](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Il relie jusqu’à huit entrées et effectue exactement la même opération de Pièce de duplication sur chacune d’elles. Il est principalement destiné à être utilisé avec des photos multi-angles, qui sont ensuite combinées avec [Multi-angle à l&#39;Albédo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Multi-angle à la normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Voir [Patch de duplication](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) pour plus d&#39;informations, voir [Patch de duplication de matériau](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) pour la version de matériau.

## Paramètres

### Paramètres

* **Nombre d&#39;entrées** : *1 - 8* définit le nombre d&#39;entrées qui recevront la même opération de correctif.
* **Est normal (uniquement pour la couleur)** : **Faux/Vrai** Définit si l&#39;entrée est une carte normale et si la fusion doit être traitée comme telle.
* **Forme** : **Carré, disque** définit la forme du tampon. Utilisé uniquement comme base.
* **Edge**
  * **Seuil** : *0.0 - 1.0* Définit la distance que doit atteindre la zone fusionnée. Cette action se développe par paliers le long des formes dans la zone cible ; elle a très peu d’effet avec des arrière-plans uniformes*.*
  * **Flou** :*0.0 - 2.0* Atténue les bords de la zone de tampon, au cas où une transition plus douce serait nécessaire.
  * **Smoothness** :*0.0 - 2.0* Arrondit les bords de la forme du tampon, ce qui permet d&#39;obtenir des contours plus fluides.
  * **Résolution de la grille** : *1 - 11* définit la résolution de qualité de l’analyse de fusion. Plus la valeur est élevée, plus la fusion est précise.
* **Transformations**
  * **Matrice source** : *(Matrice de transformation)*Transforme la source (Échelle et rotation). Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres.
  * **Décalage source** : *-0.5 - 0.5* Traduit l&#39;emplacement de la source. Ne peut pas être effectué sur la zone de travail, modifiez uniquement via ces paramètres. *Ce paramètre est probablement le principal que vous souhaitez modifier !*
  * **Matrice cible** : *(Matrice de transformation)*Transforme l&#39;emplacement cible (Échelle et rotation). Peut également être effectué via le widget sur la zone de travail.
  * **Décalage cible** : *-0.5 - 0.5* Traduit l&#39;emplacement cible. Peut également être effectué via le widget sur la zone de travail.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
