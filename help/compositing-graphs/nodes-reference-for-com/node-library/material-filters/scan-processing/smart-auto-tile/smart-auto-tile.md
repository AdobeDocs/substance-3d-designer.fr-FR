---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: Utilisez le nœud Mosaïque automatique dynamique pour créer automatiquement des mosaïques homogènes à partir de matériaux numérisés à l’aide de la détection intelligente de motif.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque automatique dynamique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# Mosaïque automatique dynamique

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

## Mosaïque automatique dynamique

**Entrée :** *Filtres de matière/Traitement de la numérisation*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud transforme un ensemble sans mosaïque de couleurs de base, de normales et de hauteurs en une version de mosaïque en fonction de l’analyse intelligente des entrées. Il est similaire à [Make It Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), mais beaucoup plus avancé car il utilise des informations de tous les canaux pour fusionner les éléments de la manière la plus intelligente (similaire à ce que fait [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)). Il possède également une fonction interne [Recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) pour déterminer la zone à utiliser lors de la juxtaposition. Pour bien comprendre cette fonction, [en savoir plus sur le nœud Recadrage](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md).

Pour utiliser ce nœud, commencez par définir votre zone recadrée, puis utilisez les paramètres Contour pour déterminer la manière dont les contours carrelés sont fusionnés au centre. Les paramètres Seuil sont d&#39;une importance capitale pour cela ! Gardez à l’esprit que les zones grandes et uniformes ne fonctionnent pas très bien avec cet effet ; plus il y a de détails et de formes, plus cela doit fonctionner.

## Paramètres

### Entrées

* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Utiliser le masque ».

### Paramètres

* **Recadrer**
  * **Taille d&#39;entrée** : *0 - 8192* résolution et proportions des images d&#39;entrée. Très important pour les images non carrées.
  * **Transformation** : *(Matrice De Transformation)*\
    Fait pivoter et met à l’échelle le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.
  * **Décalage** : *0,0 - 1,0*\
    Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail.
* **Edge**
  * **Détecter les contours** :*Faux/Vrai* active ou désactive la fusion spéciale détectée de contour.
  * **Utiliser le seuil par canal** : *Faux/Vrai* bascule entre une valeur de seuil globale ou un pour chaque canal.
  * **Seuil** : *0.0 - 1.0*
  * **Couleur de base du seuil** : *0.0 - 1.0*
  * **Seuil Normal** : *0.0 - 1.0*
  * **Height du seuil** : *0.0 - 1.0*
  * **Décalage de coupe** : *0,0 - 0,5* Contrôle principal pour déplacer la coupe, les axes X et Y sont séparés.
  * **Flou** :*0.0 - 2.0* Floute la transition de fusion.
  * **Smoothness** : *0.0 - 2.0* contrôle le décalage des résultats de l&#39;analyse des contours.
  * **Résolution de la grille** : *1 - 11* Résolution de qualité de l’analyse des contours.
  * **Utiliser la couleur de base** : *Faux/Vrai* Active/désactive le traitement de la couleur de base (entrée et sortie).
  * **Utiliser la normale** : *Faux/Vrai* Active/désactive le traitement normal (entrée et sortie).
  * **Utiliser l&#39;Height** : *Faux/Vrai* Active/désactive le traitement normal (entrée et sortie).
  * **Utiliser le masque** : *Faux/Vrai*\
    Active ou désactive l’utilisation de la carte de masque pour les formes de masque de tampon personnalisées.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
