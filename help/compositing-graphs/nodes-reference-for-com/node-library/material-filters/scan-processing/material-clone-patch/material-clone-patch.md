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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# Patch de duplication de matériau

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## Patch de duplication de matériau

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Il s&#39;agit de la version matérielle multicanaux complète de [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Il effectue un patch de duplication sur tous les canaux d’un matériau. [Voir la version d&#39;origine pour plus d&#39;informations !](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Cette fonction est très utile si vous souhaitez supprimer un détail de toutes les couches d’un matériau. Génère des images de débogage pour plusieurs canaux afin de voir à quoi ressemble exactement la zone de correctif dynamique.

## Paramètres

### Entrées

* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ».

### Paramètres

* **Canaux**
  * Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Forme** : *Carré, disque* définit la forme du tampon. Utilisé uniquement comme base.
* **Edge**
  * **Seuil (pour plusieurs canaux)** : *0.0 - 1.0* Définit la distance que doit atteindre la zone fusionnée. Ce phénomène se développe par paliers, le long des formes dans la zone cible, de sorte qu’il a très peu d’effet avec des arrière-plans uniformes*.*Faites attention lorsque vous modifiez trop cette valeur entre les couches, car cela pourrait entraîner des différences visuelles !
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
