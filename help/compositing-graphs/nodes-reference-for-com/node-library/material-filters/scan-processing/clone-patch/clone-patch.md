---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Pièce de duplication

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

## Pièce dupliquée/Pièce dupliquée en niveaux de gris

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Complexe**

</td>
<td style="border: 0;" valign="top">

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

## Paramètres

* **Est normal (uniquement pour la couleur)** : *Faux/Vrai*\
  Définit si l&#39;entrée est une carte normale et si la fusion doit être traitée comme telle.
* **Forme** : *Carré, disque* définit la forme du tampon. Utilisé uniquement comme base.
* **Edge**
  * **Seuil** : *0.0 - 1.0* Définit la distance que doit atteindre la zone fusionnée. Cette technique se développe par paliers le long des formes dans la zone cible et a très peu d’effet avec des arrière-plans uniformes*.*
  * **Flou** :*0.0 - 2.0* Atténue les bords de la zone de tampon au cas où une transition plus douce serait nécessaire.
  * **Smoothness** :*0.0 - 2.0* Arrondit les bords de la forme du tampon, ce qui permet d&#39;obtenir des contours plus fluides.
  * **Résolution de la grille** : *1 - 11* définit la résolution de la qualité de l’analyse de fusion. Plus la valeur est élevée, plus la fusion est précise.
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
